# **Build Requirements for SAINTq & SAINTexpress**

## **1. System Requirements**
SAINTq and SAINTexpress require a **Linux (Ubuntu)** system for compilation.

## **2. Compiler Requirements**
To successfully compile SAINTq and SAINTexpress, you **must** use a compatible **GCC and G++ version**:

- **Minimum required version:** GCC/G++ **4.4**
- **Maximum supported version:** GCC/G++ **9**

To check your GCC version, run:
```bash
gcc --version
g++ --version
```

If your version is outside the supported range, update or install an appropriate version.

## **3. Cloning the Repository**
Cloning this repository ensures that all required libraries are available:
```bash
git clone https://github.com/vesalkasmaeifar/Modified_SAINTq_SAINTexpress.git
cd Modified_SAINTq_SAINTexpress
```

## **4. Additional Notes**
- No external libraries need to be installed separately.
- If compilation issues occur, check your **GCC/G++ version** and update if necessary.

For further details, refer to [`docs/compilation.md`](compilation.md) for build instructions.
