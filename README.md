# ytz - YouTube Terminal Zapper

A command-line tool to search and play YouTube videos using `fzf` and `mpv`.

## Prerequisites

-   **curl:** For making HTTP requests.
-   **grep:** For pattern matching.
-   **jq:** For processing JSON data.
-   **fzf:** For fuzzy finding and selection.
-   **mpv:** For playing videos.
-   **chafa:** For displaying image previews (optional, but recommended).

## Installation

1.  Make sure you have all the prerequisites installed. On Debian/Ubuntu, you can install them using:

    ```bash
    sudo apt update
    sudo apt install curl grep jq fzf mpv chafa
    ```

    On macOS, you can use Homebrew:

    ```bash
    brew install curl jq fzf mpv chafa
    ```

2.  Download or clone this repository.
3.  Make the `ytz` script executable:

    ```bash
    chmod +x ytz
    ```

4.  (Optional) Add the script to your `$PATH` for easy access from any directory.  For example, you can move it to `/usr/local/bin`:

    ```bash
    sudo mv ytz /usr/local/bin/
    ```

## Usage

```
ytz [-a] [search_query]
```

-   `-a`:  Audio only mode (disables video).
-   `[search_query]`:  The YouTube search query. If omitted, you will be prompted to enter a search query.

### Examples

1.  Search and play a video:

    ```bash
    ytz "epic sax guy"
    ```

2.  Search and play audio only:

    ```bash
    ytz -a "lofi hip hop radio"
    ```

3.  Search with a prompt:

    ```bash
    ytz
    ```

    (You will be prompted to enter a search query.)

## Configuration

-   The script uses `mpv` with the following default options: `--volume=50`.
-   Image previews in `fzf` depend on your terminal's capabilities and the `chafa` command.

## Notes

-   If you encounter errors, ensure that all prerequisites are installed correctly and that your network connection is working.
-   If YouTube changes its page structure, the script may break.  Please report any issues.