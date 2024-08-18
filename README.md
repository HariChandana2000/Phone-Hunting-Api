# Phone Search Application

This project is a simple phone search application that allows users to search for phones by name and view their details. The application fetches data from an external API and displays the results dynamically.

## Features

- **Search Functionality**: Users can search for phones by entering a search term.
- **Loading Indicator**: A loading spinner is displayed while data is being fetched.
- **Show All Button**: If more than 12 phones are found, a "Show All" button is displayed to load all results.
- **Phone Details**: Users can view detailed information about a phone by clicking the "Show Details" button.

## Code Overview

### Variables

- `searchText`: Stores the search term entered by the user.

### Functions

- `searchHandler(isShowAll)`: Handles the search functionality. It fetches the search term from the input field and calls `loadPhone` to fetch and display the results.
- `loading(isLoading)`: Shows or hides the loading spinner based on the `isLoading` parameter.
- `loadPhone(searchText, isShowAll)`: Fetches phone data from the API based on the search term and calls `displayPhones` to display the results.
- `displayPhones(phones, isShowAll)`: Displays the list of phones. If more than 12 phones are found and `isShowAll` is false, it shows the "Show All" button and displays only the first 12 phones.
- `showBtn()`: Calls `searchHandler` with `true` to display all search results.
- `showDetailsHandler(id)`: Fetches detailed information about a phone based on its ID and calls `showPhoneDetails` to display the details.
- `showPhoneDetails(details)`: Displays detailed information about a phone in a modal.

### HTML Structure

- **Search Field**: An input field with the ID `searchField` where users enter their search term.
- **Loading Spinner**: An element with the ID `loading` that shows a loading spinner.
- **Phone Container**: A container with the ID `phone-container` where the search results are displayed.
- **Show All Button**: A button with the ID `showALLBtn` that shows all search results when clicked.
- **Modal**: A modal that displays detailed information about a phone.

## Usage

1. **Search for Phones**: Enter a search term in the search field and click the search button.
2. **View Search Results**: The search results will be displayed in the phone container.
3. **Show All Results**: If more than 12 phones are found, click the "Show All" button to view all results.
4. **View Phone Details**: Click the "Show Details" button on a phone card to view detailed information about the phone.

## Dependencies

- **API**: The application fetches data from https://openapi.programming-hero.com/

