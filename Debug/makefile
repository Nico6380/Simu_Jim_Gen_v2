################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
Simu_Jim_Gen_v2.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Simu_Jim_Gen_v2.list \


# All Target
all: Simu_Jim_Gen_v2.elf secondary-outputs

# Tool invocations
Simu_Jim_Gen_v2.elf: $(OBJS) $(USER_OBJS) /home/nicolas/STM32CubeIDE/workspace_1.0.0/Simu_Jim_Gen_v2/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Simu_Jim_Gen_v2.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/nicolas/STM32CubeIDE/workspace_1.0.0/Simu_Jim_Gen_v2/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Simu_Jim_Gen_v2.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Simu_Jim_Gen_v2.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Simu_Jim_Gen_v2.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
