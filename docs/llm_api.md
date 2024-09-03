## LLM API Overview

The CAPITOL.ai LLM API provides powerful tools for creating and managing stories. You can:

1. **Initiate Report Generation:** Create reports with custom configurations.
2. **Remix Existing Content:** Modify existing stories with new inputs.
3. **Cancel Processes:** Stop ongoing content generation tasks.
4. **Convert Content:** Transform stories into different formats.
5. **Manage Events:** Create, retrieve, and reorder story-related events.

For a complete list of endpoints and detailed documentation, visit the [Swagger API Documentation](http://acc8d77969e5b4abe95601e23fa5e6b0-1147549537.us-east-1.elb.amazonaws.com/docs).


## LLM API Endpoints

### 1. `/llm`

- **Method:** `POST`
- **Summary:** Initiate Report Generation
- **Description:** Starts the process of generating a report using the LLM based on the given parameters.
- **Request Body:**
  - `params`: General parameters for the report.
  - `llm_params`: Specific LLM configuration settings.
- **Responses:**
  - `200`: Report generation initiated successfully.
  - `422`: Validation error.

### 2. `/remix`

- **Method:** `POST`
- **Summary:** Remix Content
- **Description:** Allows remixing of an existing story with new parameters and returns the result immediately.
- **Request Body:**
  - `external_id`: ID of the story to remix.
  - `user_prompt`: Remix instructions.
  - `story_plan`: Current story plan.
- **Responses:**
  - `200`: Remix operation completed successfully.
  - `422`: Validation error.

### 3. `/cancel`

- **Method:** `POST`
- **Summary:** Cancel Content Generation
- **Description:** Cancels an ongoing content generation process.
- **Request Body:**
  - `external_id`: ID of the content generation process to cancel.
- **Responses:**
  - `200`: Cancelation successful.
  - `422`: Validation error.

### 4. `/turn_into`

- **Method:** `POST`
- **Summary:** Convert Content
- **Description:** Converts existing content into another form or type.
- **Request Body:**
  - `external_id`: ID of the content to convert.
  - `draft_id`: ID of the draft being edited.
  - `output_type`: Desired output type.
- **Responses:**
  - `200`: Conversion successful.
  - `422`: Validation error.

### 5. `/events`

- **Method:** `GET`
- **Summary:** Retrieve Events
- **Description:** Fetches events related to a specific external ID.
- **Parameters:**
  - `external_id`: Query parameter for the ID to retrieve events.
- **Responses:**
  - `200`: Events retrieved successfully.
  - `422`: Validation error.

- **Method:** `POST`
- **Summary:** Create Event
- **Description:** Creates a new event related to content generation.
- **Request Body:** 
  - Event creation parameters.
- **Responses:**
  - `200`: Event creation successful.
  - `422`: Validation error.

### 6. `/reorder/{external_id}`

- **Method:** `PUT`
- **Summary:** Reorder Events
- **Description:** Reorders events associated with a specific external ID.
- **Request Body:**
  - `events`: List of event IDs in the desired order.
- **Responses:**
  - `200`: Events reordered successfully.
  - `422`: Validation error.
