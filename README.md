# Record2JSON
_Parse and convert stringified Java records into JSON._

## Background
With the introduction of Java records in Java 16, the default `toString()` implementation provides a more human-readable string representation of objects.This improved format, e.g. `ExampleRecord(field1=value1, field2=value2)`, is useful for debugging and logging. However, this string representation should **not** be mistaken for serialization, as it is not intended for data exchange or persistence.

## Purpose
There may be scenarios where a record has been stringified, _e.g. in logs_, and needs to be recovered and serialized into a JSON for further processing. Record2JSON parses the string and converts it into a valid JSON string.

## Features
(Draft Roadmap)
1. Validate Input String
    - Ensure that the input string is a valid stringified record.
2. Validate Record Structure
    - Support providing a JSON Schema for the expected structure.
    - Support providing field names and `Class<?>` arguments for the expected structure.
3. Further Configurations
    - Support additional customizations.
      - Prettify, for example
4. Return a Valid JSON String
    - Convert the parsed object into a JSON string.
