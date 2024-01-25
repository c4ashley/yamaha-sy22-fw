# Yamaha SY22 Firmware
ROM dumps from the EEPROMs on the Yamaha SY22 synthesizer, for the purpose of
understanding and exploring the Hitachi H8 processor architecture.

| Name       | Memory Range      | File           |
|------------|-------------------|----------------|
| ROM        | 0x000000~0x01ffff | sy22.rom       |
| SRAM       | 0x020000~0x027fff |                |
| CARD       | 0x030000~0x03ffff |                |
| LD02       | 0x040000~0x0417ff |                |
| GEW5       | 0x041800~0x041804 |                |
| LCD_WR     | 0x042000~0x042002 |                |
| SFC        | 0x048000~0x048001 |                |
| SOUND      | 0x080000~0x09ffff | sy22.sound.rom |
| LCD_RD     | 0x0c2000~0x0c2002 |                |

Both ROMs contain executable code, but the SOUND ROM contains the sound presets.

For all I can tell, `0xFD80~0xFFFF` on the ROM is useless, because it maps to the
on-chip RAM and hardware registers of the processor. I expected all zeroes or all
ones, but there is indeed data there. Not sure what for.
