use reqwest::Client;

fn main() -> Result<(), Box<dyn std::error::Error>> {
    // Create a new HTTP client
    let client = Client::new();

    // Define the SIEM API endpoint URL
    let url = "https://siem-api.example.com/events";

    // Send an HTTP GET request to the SIEM API endpoint
    let response = client.get(url).send()?;

    // Check if the request was successful
    if response.status().is_success() {
        // Read the response body as a string
        let response_body = response.text()?;

        // Log the response to the console
        println!("SIEM API response: {}", response_body);
    } else {
        // Log an error message if the request was not successful
        eprintln!("Error: SIEM API returned status code {}", response.status());
    }

    Ok(())
}
