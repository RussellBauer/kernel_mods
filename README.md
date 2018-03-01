# kernel_mods
# To apply the modifications needed to the kernel:
#./openbmc$ 
#nano meta-openbmc-machines/meta-openpower/meta-ibm/meta-witherspoon/recipes-kernel/linux/linux-obmc/witherspoon.cfg
#CONFIG_I2C_SLAVE=y
#CONFIG_I2C_SLAVE_EEPROM=y

# Apply patches:
#cd ./openbmc/meta-phosphor/common/recipes-kernel/linux/
#git clone https://github.com/RussellBauer/kernel_mods.git
#cp kernel_mods/0001-i2c_salve-eeprom_octl.patch  linux-obmc/.
#cp kernel_mods/0001-DTS-Patches.patch linux-obmc/.

#git add linux-obmc/0001-i2c_salve-eeprom_octl.patch 
#git add linux-obmc/0001-DTS-Patches.patch
#nano linux-obmc.inc
#	Add: 
#		SRC_URI += "file://0001-i2c_salve-eeprom_octl.patch"
#		SRC_URI += "file://0001-DTS-Patches.patch"

#git add linux-obmc.inc
#git commit -vs -m "Kernel Patched"
