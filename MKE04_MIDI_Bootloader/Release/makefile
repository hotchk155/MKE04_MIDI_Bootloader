################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include source/subdir.mk
-include device/subdir.mk
-include board/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: MKE04_MIDI_Bootloader.axf

# Tool invocations
MKE04_MIDI_Bootloader.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -Xlinker -Map="MKE04_MIDI_Bootloader.map" -Xlinker --gc-sections -Xlinker -print-memory-usage -Xlinker --sort-section=alignment -mcpu=cortex-m0plus -mthumb -T "MKE04_MIDI_Bootloader_Release.ld" -o "MKE04_MIDI_Bootloader.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) MKE04_MIDI_Bootloader.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "MKE04_MIDI_Bootloader.axf"; # arm-none-eabi-objcopy -v -O binary "MKE04_MIDI_Bootloader.axf" "MKE04_MIDI_Bootloader.bin" ; # checksum -p MKE04Z128xxx4 -d "MKE04_MIDI_Bootloader.bin";
	-@echo ' '

.PHONY: all clean dependents post-build

-include ../makefile.targets
