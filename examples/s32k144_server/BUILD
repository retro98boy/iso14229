load("//toolchain:objcopy.bzl", "objcopy")

cc_binary(
    name = "main",
    srcs = [
        "main.c",
        "bsp.c",
        "bsp.h",
        "//:iso14229.c",
        "//:iso14229.h",
    ],
    deps = [
        ":runtime",
    ],
    defines = [
        "UDS_CUSTOM_MILLIS",
    ]
)

objcopy(
    src = "main",
    out = "main.hex",
    args = "-O ihex",
)

cc_library(
    name = "runtime",
    srcs = [
        "@s32k_sdk//:platform/devices/S32K144/startup/system_S32K144.c",
        "@s32k_sdk//:platform/devices/S32K144/startup/system_S32K144.h",
        "@s32k_sdk//:platform/devices/S32K144/include/S32K144.h",
        "@s32k_sdk//:platform/devices/S32K144/include/S32K144_features.h",
        "@s32k_sdk//:platform/devices/callbacks.h",
        "@s32k_sdk//:platform/devices/device_registers.h",
        "@s32k_sdk//:platform/devices/devassert.h",
        "@s32k_sdk//:platform/devices/startup.h",
        "@s32k_sdk//:platform/devices/startup.c",
        "@s32k_sdk//:platform/devices/status.h",
        "@s32k_sdk//:platform/devices/common/s32_core_cm4.h",
        "@s32k_sdk//:rtos/osif/osif.h",
        "@s32k_sdk//:rtos/osif/osif_baremetal.c",

        "@s32k_sdk//:platform/drivers/inc/adc_driver.h",
        "@s32k_sdk//:platform/drivers/inc/clock.h",
        "@s32k_sdk//:platform/drivers/inc/clock_manager.h",
        "@s32k_sdk//:platform/drivers/inc/cmp_driver.h",
        "@s32k_sdk//:platform/drivers/inc/crc_driver.h",
        "@s32k_sdk//:platform/drivers/inc/csec_driver.h",
        "@s32k_sdk//:platform/drivers/inc/edma_driver.h",
        "@s32k_sdk//:platform/drivers/inc/eim_driver.h",
        # "@s32k_sdk//:platform/drivers/inc/enet_driver.h",
        "@s32k_sdk//:platform/drivers/inc/erm_driver.h",
        "@s32k_sdk//:platform/drivers/inc/ewm_driver.h",
        "@s32k_sdk//:platform/drivers/inc/flash_driver.h",
        # "@s32k_sdk//:platform/drivers/inc/flash_mx25l6433f_driver.h",
        "@s32k_sdk//:platform/drivers/inc/flexcan_driver.h",
        "@s32k_sdk//:platform/drivers/inc/flexio.h",
        "@s32k_sdk//:platform/drivers/inc/flexio_i2c_driver.h",
        "@s32k_sdk//:platform/drivers/inc/flexio_i2s_driver.h",
        "@s32k_sdk//:platform/drivers/inc/flexio_spi_driver.h",
        "@s32k_sdk//:platform/drivers/inc/flexio_uart_driver.h",
        "@s32k_sdk//:platform/drivers/inc/ftm_common.h",
        "@s32k_sdk//:platform/drivers/inc/ftm_ic_driver.h",
        "@s32k_sdk//:platform/drivers/inc/ftm_mc_driver.h",
        "@s32k_sdk//:platform/drivers/inc/ftm_oc_driver.h",
        "@s32k_sdk//:platform/drivers/inc/ftm_pwm_driver.h",
        "@s32k_sdk//:platform/drivers/inc/ftm_qd_driver.h",
        "@s32k_sdk//:platform/drivers/inc/interrupt_manager.h",
        "@s32k_sdk//:platform/drivers/inc/lin_driver.h",
        "@s32k_sdk//:platform/drivers/inc/lpi2c_driver.h",
        "@s32k_sdk//:platform/drivers/inc/lpit_driver.h",
        "@s32k_sdk//:platform/drivers/inc/lpspi_master_driver.h",
        "@s32k_sdk//:platform/drivers/inc/lpspi_shared_function.h",
        "@s32k_sdk//:platform/drivers/inc/lpspi_slave_driver.h",
        "@s32k_sdk//:platform/drivers/inc/lptmr_driver.h",
        "@s32k_sdk//:platform/drivers/inc/lpuart_driver.h",
        "@s32k_sdk//:platform/drivers/inc/mpu_driver.h",
        "@s32k_sdk//:platform/drivers/inc/pdb_driver.h",
        "@s32k_sdk//:platform/drivers/inc/pins_driver.h",
        "@s32k_sdk//:platform/drivers/inc/power_manager.h",
        # "@s32k_sdk//:platform/drivers/inc/quadspi_driver.h",
        "@s32k_sdk//:platform/drivers/inc/rtc_driver.h",
        # "@s32k_sdk//:platform/drivers/inc/sai_driver.h",
        "@s32k_sdk//:platform/drivers/inc/trgmux_driver.h",
        "@s32k_sdk//:platform/drivers/inc/wdog_driver.h",

    # s32k144 has no phy
        # "@s32k_sdk//:platform/drivers/src/phy/phy_enet_access.c",
        # "@s32k_sdk//:platform/drivers/src/phy/phy_generic.c",
        # "@s32k_sdk//:platform/drivers/src/phy/phy_shared.h",
        # "@s32k_sdk//:platform/drivers/src/phy/phy_hw_access.h",
        # "@s32k_sdk//:platform/drivers/src/phy/phy_tja110x.c",
        # "@s32k_sdk//:platform/drivers/src/phy/phy.c",
        # "@s32k_sdk//:platform/drivers/src/phy/phy_shared.c",

        "@s32k_sdk//:platform/drivers/src/lpuart/lpuart_irq.c",
        "@s32k_sdk//:platform/drivers/src/lpuart/lpuart_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/lpuart/lin_lpuart_driver.h",
        "@s32k_sdk//:platform/drivers/src/lpuart/lpuart_irq.h",
        "@s32k_sdk//:platform/drivers/src/lpuart/lpuart_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/lpuart/lpuart_driver.c",
        "@s32k_sdk//:platform/drivers/src/lpuart/lin_lpuart_driver.c",
        "@s32k_sdk//:platform/drivers/src/clock/S32K1xx/clock_S32K1xx.c",
        "@s32k_sdk//:platform/drivers/src/clock/S32K1xx/scg_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/clock/S32K1xx/smc_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/clock/S32K1xx/pmc_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/clock/S32K1xx/pcc_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/clock/S32K1xx/clock_S32K1xx.h",
        "@s32k_sdk//:platform/drivers/src/clock/S32K1xx/sim_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/flexcan/flexcan_irq.c",
        "@s32k_sdk//:platform/drivers/src/flexcan/flexcan_irq.h",
        "@s32k_sdk//:platform/drivers/src/flexcan/flexcan_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/flexcan/flexcan_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/flexcan/flexcan_driver.c",
        "@s32k_sdk//:platform/drivers/src/flexio/flexio_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/flexio/flexio_spi_driver.c",
        "@s32k_sdk//:platform/drivers/src/flexio/flexio_common.c",
        "@s32k_sdk//:platform/drivers/src/flexio/flexio_uart_driver.c",
        "@s32k_sdk//:platform/drivers/src/flexio/flexio_i2s_driver.c",
        "@s32k_sdk//:platform/drivers/src/flexio/flexio_common.h",
        "@s32k_sdk//:platform/drivers/src/flexio/flexio_i2c_driver.c",
        # "@s32k_sdk//:platform/drivers/src/sai/sai_driver.c",
        # "@s32k_sdk//:platform/drivers/src/sai/sai_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/interrupt/interrupt_manager.c",
        "@s32k_sdk//:platform/drivers/src/wdog/wdog_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/wdog/wdog_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/wdog/wdog_driver.c",
        # "@s32k_sdk//:platform/drivers/src/enet/enet_irq.c",
        # "@s32k_sdk//:platform/drivers/src/enet/enet_driver.c",
        # "@s32k_sdk//:platform/drivers/src/enet/enet_hw_access.h",
        # "@s32k_sdk//:platform/drivers/src/enet/enet_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/csec/csec_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/csec/csec_driver.c",
        "@s32k_sdk//:platform/drivers/src/csec/csec_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/ewm/ewm_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/ewm/ewm_driver.c",
        "@s32k_sdk//:platform/drivers/src/pdb/pdb_driver.c",
        "@s32k_sdk//:platform/drivers/src/pdb/pdb_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/pdb/pdb_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/rtc/rtc_driver.c",
        "@s32k_sdk//:platform/drivers/src/rtc/rtc_irq.c",
        "@s32k_sdk//:platform/drivers/src/rtc/rtc_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/rtc/rtc_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/cmp/cmp_driver.c",
        "@s32k_sdk//:platform/drivers/src/cmp/cmp_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/cmp/cmp_hw_access.h",
        # "@s32k_sdk//:platform/drivers/src/quadspi/quadspi_hw_access.h",
        # "@s32k_sdk//:platform/drivers/src/quadspi/quadspi_driver.c",
        "@s32k_sdk//:platform/drivers/src/lpspi/lpspi_master_driver.c",
        "@s32k_sdk//:platform/drivers/src/lpspi/lpspi_shared_function.c",
        "@s32k_sdk//:platform/drivers/src/lpspi/lpspi_irq.c",
        "@s32k_sdk//:platform/drivers/src/lpspi/lpspi_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/lpspi/lpspi_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/lpspi/lpspi_slave_driver.c",
        "@s32k_sdk//:platform/drivers/src/lpit/lpit_driver.c",
        "@s32k_sdk//:platform/drivers/src/lpit/lpit_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/eim/eim_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/eim/eim_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/eim/eim_driver.c",
        "@s32k_sdk//:platform/drivers/src/lptmr/lptmr_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/lptmr/lptmr_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/lptmr/lptmr_driver.c",
        "@s32k_sdk//:platform/drivers/src/flash/flash_driver.c",
        # "@s32k_sdk//:platform/drivers/src/flash_mx25l6433f/flash_mx25l6433f_regs.h",
        # "@s32k_sdk//:platform/drivers/src/flash_mx25l6433f/flash_mx25l6433f_driver.c",
        "@s32k_sdk//:platform/drivers/src/edma/edma_irq.c",
        "@s32k_sdk//:platform/drivers/src/edma/edma_irq.h",
        "@s32k_sdk//:platform/drivers/src/edma/edma_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/edma/edma_driver.c",
        "@s32k_sdk//:platform/drivers/src/edma/edma_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/crc/crc_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/crc/crc_driver.c",
        "@s32k_sdk//:platform/drivers/src/crc/crc_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_qd_driver.c",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_mc_driver.c",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_ic_driver.c",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_common.c",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_pwm_driver.c",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/ftm/ftm_oc_driver.c",
        "@s32k_sdk//:platform/drivers/src/mpu/mpu_driver.c",
        "@s32k_sdk//:platform/drivers/src/mpu/mpu_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/mpu/mpu_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/lpi2c/lpi2c_irq.h",
        "@s32k_sdk//:platform/drivers/src/lpi2c/lpi2c_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/lpi2c/lpi2c_irq.c",
        "@s32k_sdk//:platform/drivers/src/lpi2c/lpi2c_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/lpi2c/lpi2c_driver.c",
        "@s32k_sdk//:platform/drivers/src/erm/erm_driver.c",
        "@s32k_sdk//:platform/drivers/src/erm/erm_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/erm/erm_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/power/S32K1xx/power_scg_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/power/S32K1xx/power_manager_S32K1xx.c",
        "@s32k_sdk//:platform/drivers/src/power/S32K1xx/power_smc_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/power/S32K1xx/power_rcm_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/power/S32K1xx/power_manager_S32K1xx.h",
        "@s32k_sdk//:platform/drivers/src/power/S32K1xx/power_smc_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/power/power_manager.c",
        "@s32k_sdk//:platform/drivers/src/lin/lin_irq.c",
        "@s32k_sdk//:platform/drivers/src/lin/lin_common.c",
        "@s32k_sdk//:platform/drivers/src/lin/lin_driver.c",
        "@s32k_sdk//:platform/drivers/src/adc/adc_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/adc/adc_driver.c",
        "@s32k_sdk//:platform/drivers/src/trgmux/trgmux_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/trgmux/trgmux_hw_access.c",
        "@s32k_sdk//:platform/drivers/src/trgmux/trgmux_driver.c",
        "@s32k_sdk//:platform/drivers/src/pins/pins_driver.c",
        "@s32k_sdk//:platform/drivers/src/pins/pins_gpio_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/pins/pins_port_hw_access.h",
        "@s32k_sdk//:platform/drivers/src/pins/pins_port_hw_access.c",


        "@s32k_sdk//:platform/devices/S32K144/startup/gcc/startup_S32K144.S",
    ],
    deps = [
        "@s32k_sdk//:platform/devices/S32K144/linker/gcc/S32K144_64_flash.ld",
        "@s32k_sdk//:include",
        "@CMSIS//:include",
    ],
    linkopts = [
        "-T $(location @s32k_sdk//:platform/devices/S32K144/linker/gcc/S32K144_64_flash.ld)",
        "-lc",
        "-lnosys",
        "-Wl,--defsym=__Vectors=__isr_vector",
        # force the symbol CAN0_Error_IRQHandler to be included
        "-Wl,--undefined=CAN0_Error_IRQHandler",
    ],
    defines = [
        "CPU_S32K144HFT0VLLT",
        "DEV_ERROR_DETECT=1U",
    ],
    target_compatible_with = ["//platforms:s32k"],
)