################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/HID/Src/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
usb_hid_snes_gamepad.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
usb_hid_snes_gamepad.list \

OBJCOPY_BIN += \
usb_hid_snes_gamepad.bin \


# All Target
all: usb_hid_snes_gamepad.elf secondary-outputs

# Tool invocations
usb_hid_snes_gamepad.elf: $(OBJS) $(USER_OBJS) C:\Users\Marcel\STM32CubeIDE\workspace_1.0.2\usb_hid_snes_gamepad\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "usb_hid_snes_gamepad.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Marcel\STM32CubeIDE\workspace_1.0.2\usb_hid_snes_gamepad\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="usb_hid_snes_gamepad.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

usb_hid_snes_gamepad.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "usb_hid_snes_gamepad.list"
	@echo 'Finished building: $@'
	@echo ' '

usb_hid_snes_gamepad.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "usb_hid_snes_gamepad.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
