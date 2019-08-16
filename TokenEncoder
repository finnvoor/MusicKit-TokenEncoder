#!/usr/bin/env ruby

require 'jwt'

unless ARGV.length == 3
  puts "Usage: ./TokenEncoder <AuthKey>.p8 <Key ID> <Team ID>\n"
  exit
end

payload = {
  :iss => "#{ARGV[2]}",
  :iat => Time.now.to_i,
  :exp => Time.now.to_i + 15777000
}

key = OpenSSL::PKey::EC.new(`openssl pkcs8 -nocrypt -in #{ARGV[0]}`)

header = {
  :alg => "ES256",
  :kid => "#{ARGV[1]}"
}

token = JWT.encode payload, key, "ES256", header
puts "\n#{token}"