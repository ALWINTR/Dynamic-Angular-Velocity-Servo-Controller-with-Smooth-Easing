# Dynamic Angular Velocity Servo Controller with Smooth Easing

[![GitHub Repository](https://img.shields.io/badge/GitHub-Repository-00f0ff?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ALWINTR/dynamic-servo-angle-controller)
[![Developer](https://img.shields.io/badge/Developer-Alwin_T_R-0284c7?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/alwintr)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

Non-blocking servo angle interpolation firmware providing adjustable angular velocity control, smooth S-curve easing, and millisecond-level step granularity to eliminate mechanical servo jitter, gear train wear, and sudden inertial shock.

---

## Motion Interpolation Architecture

Standard servo libraries jump instantly from initial position to target angle, causing severe torque spikes and current draw surges. This library decomposes the angular delta into discrete micro-steps executed across a defined time horizon using non-blocking hardware timer ticks.

```
       [Target Angle Request]
                 |
                 v
       [Calculate Delta: Target - Current]
                 |
                 v
       [Step Increment = Delta / Total Steps]
                 |
                 v
       [Periodic Timer Callback (20ms)] ---> Update PWM Position Smoothly
```

---

## Author

**Alwin T R** - Robotics and Automation Engineer  
- LinkedIn: [linkedin.com/in/alwintr](https://www.linkedin.com/in/alwintr)  
- Portfolio: [alwintr.github.io](https://alwintr.github.io)  
- GitHub: [github.com/ALWINTR](https://github.com/ALWINTR)

---

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.
