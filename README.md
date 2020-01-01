# Patching DSDT/SSDT on Asus ROG GL552VW

Applying various patches to DSDT/SSDT on Asus ROG GL552VW for my hackintosh.

## Disassemble DSDT/SSDT

```bash
# Get iasl
wget https://bitbucket.org/RehabMan/acpica/downloads/iasl.zip
unzip iasl.zip
sudo cp iasl /usr/bin/
rm iasl iasl.zip

# Run iasl on the ACPI files
iasl -da -dl -fe refs.txt DSDT.aml SSDT*.aml
```