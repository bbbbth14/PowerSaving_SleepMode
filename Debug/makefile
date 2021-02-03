################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
PowerSaving_SleepMode_.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
PowerSaving_SleepMode_.list \

OBJCOPY_BIN += \
PowerSaving_SleepMode_.bin \


# All Target
all: PowerSaving_SleepMode_.elf secondary-outputs

# Tool invocations
PowerSaving_SleepMode_.elf: $(OBJS) $(USER_OBJS) D:\STM32\Workspace\PowerSaving_SleepMode_\STM32F411VETX_FLASH.ld
	arm-none-eabi-gcc -o "PowerSaving_SleepMode_.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\STM32\Workspace\PowerSaving_SleepMode_\STM32F411VETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="PowerSaving_SleepMode_.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

PowerSaving_SleepMode_.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "PowerSaving_SleepMode_.list"
	@echo 'Finished building: $@'
	@echo ' '

PowerSaving_SleepMode_.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "PowerSaving_SleepMode_.bin"
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
