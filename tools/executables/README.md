# README for ExifTool Executable

## Credits

Full credits to Phil Harvey, the creator of ExifTool. You can find more information and download ExifTool from the official website: [ExifTool by Phil Harvey](https://exiftool.org/).

## Usage Information

Our tooling was programmed using Python on Windows. If you are using a different operating system, you will need to change the ExifTool executable to the appropriate version for your operating system. You can download the appropriate version from the [ExifTool website](https://exiftool.org/).

### Important Notes

- This tooling has been tested and developed on Windows. Usage on other operating systems is untested and unsupported.
- Ensure that you replace the `exiftool.exe` reference in the scripts with the correct path and executable name for your operating system.

### Example Of Usage On Different Operating Systems

#### macOS
Replace the ExifTool path in the scripts with:
```python
subprocess.run(
    [
        "/usr/local/bin/exiftool"
    ]
)
```

#### Linux
Replace the ExifTool path in the scripts with:
```python
subprocess.run(
    [
        "/usr/bin/exiftool"
    ]
)
```

For further information on using ExifTool, please refer to the [Official Documentation](https://exiftool.org/#links).

## Disclaimer
This repository does not own ExifTool, and full credit goes to Phil Harvey for his work. Any issues related to the ExifTool executable should be referred to the ExifTool support channels.