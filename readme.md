Insurance Dataset: Column Explanations

This dataset contains 41 columns that describe the policyholder, the vehicle, and the geographic region. For your Auto Fraud Detection System, these are categorized into four main groups.

1. Primary Identifiers & Target

policy_id: A unique string for each policy. (Recommendation: Drop this before training as it contains no patterns).

claim_status: (Target Variable) 0 = No Claim, 1 = Claim filed. This is what your model will predict.

2. Customer & Policy Profiles

subscription_length: How long the customer has been with the insurance company (in years).

customer_age: Age of the policyholder.

segment: The market segment of the vehicle (e.g., A, B1, B2, C1, C2).

ncap_rating: Safety rating of the vehicle (0 to 5). Higher ratings often correlate with lower injury claims.

3. Vehicle Specifications (The "Mechanical" Features)

Many of these are currently strings and were handled by the engineer_features function in your Python script.

vehicle_age: Age of the car.

model: The specific car model name.

fuel_type: Type of fuel (Petrol, Diesel, CNG).

max_torque: String describing engine torque (e.g., "250Nm@4000rpm").

max_power: String describing engine power (e.g., "113bhp@6000rpm").

engine_type: The specific engine architecture.

displacement: The engine size in CC (e.g., 1200, 1500).

cylinder: Number of cylinders in the engine.

gear_box: Number of gears.

steering_type: Type of steering (Power, Electric, Manual).

turning_radius: The space needed to make a U-turn.

length / width / height: Physical dimensions of the car.

gross_weight: Total weight of the vehicle.

4. Safety & Comfort Features (Boolean/Binary)

These are the is_... columns we converted to 0 and 1 in our cleaning script.

airbags: Number of airbags in the vehicle.

is_esc: Electronic Stability Control presence.

is_adjustable_steering: Whether the steering column can be moved.

is_tpms: Tire Pressure Monitoring System presence.

is_parking_sensors: Presence of proximity sensors.

is_parking_camera: Presence of a rear or 360 camera.

rear_brakes_type: Disc vs. Drum brakes.

is_front_fog_lights / is_rear_window_wiper / is_rear_window_washer / is_rear_window_defogger: Visibility features.

is_brake_assist / is_power_door_locks / is_central_locking / is_power_steering: Control and security features.

is_driver_seat_height_adjustable: Ergonomic feature.

is_day_night_rear_view_mirror / is_ecw / is_speed_alert: Safety alert features.

5. Geographical Features

region_code: A code representing the area where the vehicle is registered (e.g., C1, C2).

region_density: The population density of that region. High-density areas (cities) often have higher claim rates due to traffic.