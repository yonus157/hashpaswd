# hashpaswd
storing a password in hexadecimal string
import hashlib
def hash_password(password):
    # Encode the password as bytes
    password_bytes = password.encode('utf-8')

    # Use SHA-256 hash function to create a hash object
    hash_object = hashlib.sha256(password_bytes)
    # Get the hexadecimal representation of the hash
    password_hash = hash_object.hexdigest()
    return password_hash
password = input("Input your password: ")
hashed_password = hash_password(password)
print(f"Your hashed password is: {hashed_password}")
