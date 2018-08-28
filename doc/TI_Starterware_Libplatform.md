 The following is the list of routines that are in the TI starterware lib
 platform.

libplatform.a

board.o:
00000000 T BoardInfoCheck
         U strcmp

cpsw.o:
00000000 T CPSWClkEnable
00000000 T CPSWPinMuxSetup
00000000 T EVMMACAddrGet
00000000 T EVMPortMIIModeSelect

ctlregcontext.o:
00000000 T ControlRegContextRestore
00000000 T ControlRegContextSave
00000000 T IOPadConfigure
00000000 T IOPadContextRestore
00000000 T IOPadContextSave
00000000 T IOPadSel
00000000 T IOPadSelConfigure

dmtimer.o:
00000000 T DMTimer1msModuleClkConfig
00000000 T DMTimer2ModuleClkConfig
00000000 T DMTimer3ModuleClkConfig
00000000 T DMTimer4ModuleClkConfig
00000000 T DMTimer6ModuleClkConfig
00000000 T DMTimer7ModuleClkConfig

edma.o:
00000000 T EDMA3CrossBarChannelMap
00000000 T EDMAModuleClkConfig
00000000 T EDMAVersionGet

eeprom.o:
00000000 T BoardInfoRead
00000000 T EEPROMI2CRead
00000000 T EEPROMI2CSetUp
         U I2C0ModuleClkConfig
00000000 t I2C0PinMux
         U I2CMasterBusBusy
         U I2CMasterControl
         U I2CMasterDataGet
         U I2CMasterDataPut
         U I2CMasterDisable
         U I2CMasterEnable
         U I2CMasterInitExpClk
         U I2CMasterIntClearEx
         U I2CMasterIntDisableEx
         U I2CMasterIntRawStatus
         U I2CMasterIntRawStatusEx
         U I2CMasterSlaveAddrSet
         U I2CMasterStart
         U I2CMasterStop
         U I2CSetDataCount
         U I2CSoftReset
         U I2CSystemStatusGet
00000000 t StatusClear

gpio.o:
00000000 T GPIO0ModuleClkConfig
00000000 T GPIO1ModuleClkConfig
00000000 T GPIO1Pin23PinMuxSetup
00000000 T GPIO1PinMuxSetup
00000000 T GpioPinMuxSetup

hs_mmcsd.o:
00000000 T HSMMCSDModuleClkConfig
00000000 T HSMMCSDPinMuxSetup

hsi2c.o:
00000000 T I2C0ModuleClkConfig
00000000 T I2C1ModuleClkConfig
00000000 T I2CPinMuxSetup

rtc.o:
00000000 T RTCModuleClkConfig
00000000 T RtcVersionGet

sysdelay.o:
         U DMTimer7ModuleClkConfig
         U DMTimerCounterSet
         U DMTimerDisable
         U DMTimerEnable
         U DMTimerIntDisable
         U DMTimerIntEnable
         U DMTimerIntStatusClear
00000000 t DMTimerIsr
         U DMTimerModeConfigure
00000000 d flagIsr
         U IntPrioritySet
         U IntRegister
         U IntSystemEnable
00000000 T Sysdelay
00000000 T SysDelayTimerSetup
00000000 T SysIsTimerElapsed
00000000 T SysStartTimer
00000000 T SysStopTimer

sysperf.o:
         U DMTimer7ModuleClkConfig
         U DMTimerCounterGet
         U DMTimerCounterSet
         U DMTimerDisable
         U DMTimerEnable
00000000 d flagIsr
00000000 T SysPerfTimerConfig
00000000 T SysPerfTimerSetup

timertick.o:
00000000 T TimerTickConfigure
00000000 T TimerTickDisable
00000000 T TimerTickEnable
00000000 T TimerTickPeriodSet

uart.o:
00000000 T UART0ModuleClkConfig
00000000 T UARTPinMuxSetup

uartConsole.o:
         U UART0ModuleClkConfig
00000000 t UartBaudRateSet
         U UARTBreakCtl
         U UARTCharGet
         U UARTCharPut
00000000 T UARTConsoleGetc
00000000 T UARTConsoleInit
00000000 T UARTConsolePutc
         U UARTDivisorLatchDisable
         U UARTDivisorLatchWrite
         U UARTDivisorValCompute
         U UARTFIFOConfig
00000000 t UartFIFOConfigure
         U UARTLineCharacConfig
         U UARTModuleReset
         U UARTOperatingModeSelect
         U UARTPinMuxSetup
         U UARTRegConfigModeEnable
00000000 t UARTStdioInitExpClk

usb.o:
00000000 T USB0ModuleClkConfig
00000000 T USBClearInt
00000000 T USBEnableInt
00000000 T USBModuleClkDisable
00000000 T USBModuleClkEnable
00000000 T USBVersionGet

watchdog.o:
00000000 T WatchdogTimer1ModuleClkConfig
