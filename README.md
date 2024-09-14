# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

'''
import React, { useState } from 'react';

const CustomSelect = ({ options, onCurrencyChange }) => {
const [size, setSize] = useState(1);

const handleMouseDown = () => {
setSize(5);
};

const handleBlur = () => {
setSize(1);
};

const handleChange = (e) => {
setSize(1);
if (onCurrencyChange) {
onCurrencyChange(e.target.value);
}
};

return (
<select
      size={size}
      onMouseDown={handleMouseDown}
      onChange={handleChange}
      onBlur={handleBlur}
    >
{options.map((option, index) => (

<option key={index} value={option.value}>
{option.label}
</option>
))}
</select>
);
};

export default CustomSelect;
'''
