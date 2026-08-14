# ==============================================
#              MY GYM MANAGEMENT
# ==============================================

import os
import time


# Store all gym members
members = []


# Clear the terminal screen
def clear():
    os.system("cls" if os.name == "nt" else "clear")


# Add a new member
def add_member():

    clear()

    print("==============================================")
    print("              ADD NEW MEMBER")
    print("==============================================")

    first_name = input("First name: ")
    last_name = input("Last name: ")
    member_id = input("Member ID: ")

    # Press Enter for Active
    # Write "no" for Inactive
    status = input(
        "Is the member active? "
        "(Press Enter = Yes / type no = No): "
    ).lower()

    if status == "no":
        status = "Inactive"
    else:
        status = "Active"

    # Create a dictionary for the new member
    member = {
        "first_name": first_name,
        "last_name": last_name,
        "id": member_id,
        "status": status
    }

    # Add the member to the list
    members.append(member)

    print()
    print("----------------------------------------------")
    print("Member added successfully!")
    print("----------------------------------------------")
    print("Name:", first_name, last_name)
    print("ID:", member_id)
    print("Status:", status)

    time.sleep(3)


# Show all members
def show_members():

    clear()

    print("==============================================")
    print("                GYM MEMBERS")
    print("==============================================")

    if len(members) == 0:

        print()
        print("There are no members yet.")

    else:

        # Display every member
        for member in members:

            print()
            print("----------------------------------------------")
            print("ID:", member["id"])
            print(
                "Name:",
                member["first_name"],
                member["last_name"]
            )
            print("Status:", member["status"])

    print()
    print("----------------------------------------------")
    print("Returning to the main menu in 10 seconds...")
    time.sleep(10)


# Search for a member
def search_member():

    clear()

    print("==============================================")
    print("                SEARCH MEMBER")
    print("==============================================")

    search = input("Enter member name or ID: ").lower()

    found = False

    # Search through all members
    for member in members:

        full_name = (
            member["first_name"]
            + " "
            + member["last_name"]
        ).lower()

        if search == member["id"].lower() or search in full_name:

            print()
            print("Member found!")
            print("----------------------------------------------")
            print("Name:", member["first_name"], member["last_name"])
            print("ID:", member["id"])
            print("Status:", member["status"])
            print("----------------------------------------------")

            found = True

    if found == False:

        print()
        print("Sorry, no member was found.")

    print()
    print("Returning to the main menu in 10 seconds...")
    time.sleep(10)


# Main program
while True:

    clear()

    print("==============================================")
    print("             MY GYM MANAGEMENT")
    print("==============================================")
    print()
    print("1 - Add a new member")
    print("2 - Show all members")
    print("3 - Search for a member")
    print("0 - Exit")
    print()
    print("==============================================")

    choice = input("Choose an option: ")

    # Add member
    if choice == "1":

        add_member()

    # Show members
    elif choice == "2":

        show_members()

    # Search member
    elif choice == "3":

        search_member()

    # Exit
    elif choice == "0":

        clear()

        print("==============================================")
        print("          THANK YOU FOR USING MY GYM")
        print("==============================================")
        print()
        print("See you next time!")
        break

    # Wrong choice
    else:

        print()
        print("Invalid choice.")
        print("Please choose 1, 2, 3 or 0.")

        time.sleep(2)
      
