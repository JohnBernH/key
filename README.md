from cryptography.fernet import Fernet

# Generate a random key
key = Fernet.generate_key()

# Create a Fernet object instance using the key
f = Fernet(key)

# Encrypt the message
message = b"Hello, World!"
encrypted_message = f.encrypt(message)

# Decrypt the message
decrypted_message = f.decrypt(encrypted_message)

# Print the results
print("Key: ", key)
print("Encrypted message: ", encrypted_message)
print("Decrypted message: ", decrypted_message)
