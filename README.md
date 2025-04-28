# RETO_2
Diagrama de clases de un computador
En este diagrama, dividí el computador en 2 clases, componentes y sistema operativo, estos a su vez tienen sus propias clases y atributos.
```mermaid
classDiagram
class Computer {
    +list Components
    +list available_OS
    +TurnON()
    +TurnOFF()
}

class Components {
    +string manufacturer
    +list release_date
    +string color
    +float MSRP
    +Function()
}

class Motherboard {
    +string socket
    +string chipset
    +string form_factor
    +string memory_type
    +int memory_slots
    +int nvme_slots
    +int sata_ports
    +int PCIe_x16_slots
}

class CPU {
    +bool integrated_graphics
    +string model
    +int cores
    +float clock_speed
    +int TDP
}

class GPU {
    +string chipset
    +int vram_size
    +int TDP
    +float clock_speed
}

class RAM {
    +int quantity
    +int modules
    +int speed
    +string memory_type
    +int CAS_latency
}

class Storage {
    +float capacity
    +string type
    +string form_factor
}

class CPU_cooler {
    +bool water_cooled
    +int number_of_fans
    +string socket
}

class Power_supply {
    +int wattage
    +string form_factor
    +string modularity
    +string certification
}

class Case {
    +string type
    +int max_number_of_fans
    +float volume_liters
    +list dimensions
}

class OS {
    +float partition_size
    +bool dual_boot
}

class Windows {
    +string version
    +string edition
    +int disk_space_required
}

class Linux_distro {
    +string distro_name
    +int disk_space_required
}

Computer *-- Components
Computer *-- OS
Components <|-- Motherboard
Components <|-- CPU
Components <|-- GPU
Components <|-- RAM
Components <|-- Storage
Components <|-- CPU_cooler
Components <|-- Power_supply
Components <|-- Case
OS <|-- Windows
OS <|-- Linux_distro
```
P.D. Cada clase tiene un constructor para que cada objeto pueda usar valores distintos y definirse de manera distinta



