\# CrossWalk interface table



Supply: 1.8 V (Vref = VDD). All digital signals are 0 to 1.8 V.



| Signal | From | To | Notes |

|---|---|---|---|

| Vin | external pin | Sample/hold | analog |

| clk\_in | external pin | Clocks | 4 MHz (proposed) |

| clk\_sh | Clocks | Sample/hold | active in P0 |

| Vsh | Sample/hold | Comparator | analog, may merge with CDAC |

| Vref | supply | CDAC | = VDD |

| Dtrial\[7:0] | SAR logic | CDAC | 8-bit trial code |

| Vdac | CDAC | Comparator | analog |

| clk\_cmp | TBD | Comparator | source not decided |

| comp\_bit | Comparator | SAR logic | 1-bit decision |

| clk\_sar, rst | Clocks | SAR logic | |

| final\_code\[7:0] | SAR logic | Output register | |

| clk\_door | Clocks | Output register | active in P9 |

| D\[7:0] | Output register | external pins | 8-bit output |



Frame: P0 sample, P1 to P8 bit decisions, P9 output capture.

