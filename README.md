# Class OverNetworkAuthentication

class OverNetworkAuthentication:

    def __init__(self):
        # Initialize the database to store user profiles
        self.user_database = {}

    def create_account(self, username, param2):
        # Check if the username already exists in the database
        if username in self.user_database:
            return "Username already exists. Please choose a different one."

        # Create a new user profile
        user_profile = {
            "username": username,
            "param2": param2,
        }

        # Store the user profile in the database
        self.user_database[username] = user_profile

        return f"Account for {username} created and user logged in."

# Example usage:
auth_system = OverNetworkAuthentication()
username = "joe_shmoe"
param2 = "Joe"

result = auth_system.create_account(username, param2)
print(result)
