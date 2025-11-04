Sheet Metal Cutting Plan Optimizer

Overview
A web-based tool for optimizing sheet metal cutting plans to minimize waste and maximize material usage. The application implements a binary tree packing algorithm to efficiently arrange parts on metal sheets while respecting the physical constraints of the cutting equipment.

Key Features
✅ 3D Cutting Plan Optimization: Intelligent arrangement of parts on metal sheets
✅ Cutter Width Constraint: Respects the 3-meter (3000mm) maximum cutter width limitation
✅ Multi-language Support: Arabic and English interfaces
✅ Dark/Light Mode: User-friendly theme selection
✅ Excel Import: Load parts data from Excel files
✅ Comprehensive Reporting:
Cutting plan summary
Stock statement with material codes
Returns/waste statement for reusable scraps
✅ Weight Calculation: Automatic weight calculation based on dimensions and steel density
✅ Material Database: Pre-configured steel types and thicknesses with corresponding stock codes
How to Use
Add Parts:
Manually enter part details (name, steel type, dimensions, quantity)
Or import from Excel (requires columns: Name, SteelType, Quantity, Length, Width, Thickness)
Set Cutting Parameters:
Sheet dimensions (length and width)
Enable/disable part rotation (if within cutter width limits)
Maximum cutter width is set to 3000mm by default
Generate Plan:
Click "Generate Cutting Plan" to create the optimized layout
The system will group parts by steel type and thickness
Review Results:
Summary shows total sheets, material usage efficiency, and waste area
Detailed cutting plan shows which parts go on each sheet
Waste pieces ≥500x500mm are automatically added to returns statement
Export Reports:
Cutting plan summary
Stock statement (with material codes)
Returns statement (waste materials)
Technical Details
Algorithm: Binary tree packing algorithm with rotation handling
Key Constraint: Maximum cutter width of 3000mm (applied to sheet width)
Weight Calculation:


1
Weight = (Length(m) × Width(m) × Thickness(mm) × 7.85) / 1000
Waste Identification: Any area ≥500×500mm is considered reusable waste
Requirements
Modern web browser (Chrome, Firefox, Edge)
No server required - runs completely in the browser
For Excel import: SheetJS library (included)
Contributing
Contributions are welcome! Please follow these steps:

Fork the repository
Create your feature branch (git checkout -b feature/AmazingFeature)
Commit your changes (git commit -m 'Add some AmazingFeature')
Push to the branch (git push origin feature/AmazingFeature)
Open a Pull Request
Notes
The system automatically prevents sheet width from exceeding 3000mm (cutter capacity)
For best results, keep part dimensions well below cutter width
The algorithm prioritizes placing larger parts first to maximize efficiency
Waste materials with dimensions ≥500mm are automatically considered reusable
License
This project is licensed under the MIT License - see the LICENSE file for details.
