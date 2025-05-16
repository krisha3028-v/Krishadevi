# KrishadeviINPUT:
import random
import time

class UrbanPlanningSystem:
    def _init_(self, area_name):
        self.area_name = area_name
        self.pedestrian_flow = {'north': 0, 'south': 0, 'east': 0, 'west': 0}
        self.vehicle_flow = {'north': 0, 'south': 0, 'east': 0, 'west': 0}
        self.optimized_layout = False

    def simulate_data(self):
        # Simulate real-time pedestrian and vehicle flow data
        for direction in self.pedestrian_flow:
            self.pedestrian_flow[direction] = random.randint(0, 500)
            self.vehicle_flow[direction] = random.randint(0, 300)

    def optimize_layout(self):
        # Simple optimization based on flow volumes
        total_pedestrians = sum(self.pedestrian_flow.values())
        total_vehicles = sum(self.vehicle_flow.values())
        self.optimized_layout = total_pedestrians > total_vehicles

    def display_status(self):
        print(f"Area: {self.area_name}")
        print(f"Pedestrian Flow: {self.pedestrian_flow}")
        print(f"Vehicle Flow: {self.vehicle_flow}")
        print(f"Optimized for Pedestrians: {'Yes' if self.optimized_layout else 'No'}")
        print("-" * 40)


def main():
    downtown_area = UrbanPlanningSystem("Downtown City Center")
    for _ in range(5):  # Simulate 5 planning cycles
        downtown_area.simulate_data()
        downtown_area.optimize_layout()
        downtown_area.display_status()
        time.sleep(2)  # Simulate real-time delay


if _name_ == "_main_":
    main()\


OUTPUT:

Area: Downtown City Center

Pedestrian Flow: {'north': 390, 'south': 415, 'east': 308, 'west': 198}

Vehicle Flow: {'north': 189, 'south': 116 'east': 289, 'west': 257}

Optimized for Pedestrians: Yes

Area: Downtown City Center

Pedestrian Flow: {'north': 313, 'south': 284, 'east': 404, 'west': 416}

Vehicle Flow: {'north': 28, 'south': 101, 'east': 138, 'west': 148}

Optimized for Pedestrians: Yes

Area: Downtown City Center

Pedestrian Flow: {'north': 44, 'south': 217, 'east': 74, 'west': 144}

Vehicle Flow: {'north': 282, 'south': 37, 'east': 155, 'west': 34}

Optimized for Pedestrians: No

Area: Downtown City Center

Pedestrian Flow: {'north': 25, 'south': 497, 'east': 433, 'west': 84}

Vehicle Flow: {'north': 283, 'south': 209 'east': 179, 'west': 5}

Optimized for Pedestrians: Yes
Area: Downtown City Center

Pedestrian Flow: {'north': 434, 'south':

366, 'east': 41, 'west': 257}

Vehicle Flow: {'north': 38, 'south': 92,

'east': 226, '

west': 50}

Optimized for Pedestrians: Yes

