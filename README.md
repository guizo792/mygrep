## Prerequisites

Before running MyGrep, make sure you have the following tools installed on your system:

1. **Rust:**
   - MyGrep is a Rust project, and you need the Rust programming language installed. You can install Rust by following the instructions on the [official Rust website](https://www.rust-lang.org/tools/install).

2. **Cargo:**
   - Cargo is the official package manager and build tool for Rust. It is usually included with the Rust installation.

## Usage

To use MyGrep, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/mygrep.git
2. **Navigate to the project directory:**

   ```bash
   cd mygrep
3. **Build the project:**

   ```bash
   cargo build --release
4. Run MyGrep with the desired `query` and `file path`:
   ```bash
   ./target/release/mygrep query file_path
   ```
   
    You can also set the IGNORE_CASE environment variable to perform a case-insensitive search:
      ```bash
      IGNORE_CASE=1 ./target/release/mygrep query file_path
## Example
Suppose you have a file named `example.txt` with the following content:

  ```plaintext
  Rust:
  safe, fast, productive.
  Pick three.
  Duct tape.
  ```
  To search for the query "duct" in a case-sensitive manner, run the following command:
  ```bash
  ./target/release/mygrep duct example.txt
  ```

  To perform a case-insensitive search, set the IGNORE_CASE environment variable:

  ```bash
  IGNORE_CASE=1 ./target/release/mygrep duct example.txt
  ```

  This will output:
  ```plaintext
  Duct tape.
  ```
  
