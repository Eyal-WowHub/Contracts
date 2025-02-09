# Contracts

A library that provides Design by Contract like API to ensure functions adhere to specific preconditions and postconditions.

#### Dependencies: [LibStub](https://www.curseforge.com/wow/addons/libstub)

### Example:

```lua
local C = LibStub("Contracts-1.0")

local function Divide(numerator, denominator)
   C:IsNumber(numerator, 1)
   C:IsNumber(denominator, 2)
   
   C:Ensures(denominator ~= 0, "Divided by zero. The denominator cannot be zero.")
   
   return numerator / denominator
end
```