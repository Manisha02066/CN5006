import React, { useState } from "react";
import Button from "./Button.js";
import './Calculator.css';
import pic from './pic.png'; // Import the image from src folder

function KeyPadComponent(props) {
    const [text1, setText] = useState(""); // State for current input
    const [showImage, setShowImage] = useState(false); // State to track whether to show the image

    // Handle button clicks
    const ClickHandle = (e) => {
        const value = e.target.value;

        if (value === "C") {
            setText("");  // Clear the input
        } else if (value === "=") {
            try {
                setText(eval(text1));  // Evaluate the expression
            } catch (error) {
                setText("Error");  // Handle any errors
            }
        } else if (value === "show me") {
            setShowImage(!showImage);  // Toggle image visibility
        }  
        else if (value === "square") {
            setText(Math.pow(parseFloat(text1), 2));}
            else {
            setText(text1 + value);  // Append value to the current input
        }
    };

    return (
        <div className="Calculator">
            <div className="screen-row">
                <input type="text" readOnly value={text1} />
            </div>

            <div>
                <Button label="(" ClickHandle={ClickHandle} />
                <Button label="CE" ClickHandle={ClickHandle} />
                <Button label=")" ClickHandle={ClickHandle} />
                <Button label="C" ClickHandle={ClickHandle} />
            </div>

            <div>
                <Button label="1" ClickHandle={ClickHandle} />
                <Button label="2" ClickHandle={ClickHandle} />
                <Button label="3" ClickHandle={ClickHandle} />
                <Button label="+" ClickHandle={ClickHandle} />
            </div>

            <div>
                <Button label="4" ClickHandle={ClickHandle} />
                <Button label="5" ClickHandle={ClickHandle} />
                <Button label="6" ClickHandle={ClickHandle} />
                <Button label="-" ClickHandle={ClickHandle} />
            </div>

            <div>
                <Button label="7" ClickHandle={ClickHandle} />
                <Button label="8" ClickHandle={ClickHandle} />
                <Button label="9" ClickHandle={ClickHandle} />
                <Button label="*" ClickHandle={ClickHandle} />
            </div>

            <div>
                <Button label="." ClickHandle={ClickHandle} />
                <Button label="0" ClickHandle={ClickHandle} />
                <Button label="=" ClickHandle={ClickHandle} />
                <Button label="/" ClickHandle={ClickHandle} />
            </div>
            <div>
                <Button label="square" ClickHandle={ClickHandle} />
            </div>

            {/* Add show me button */}
            <div>
                <Button label="show me" ClickHandle={ClickHandle} />
            </div>

            {/* Conditionally render the image */}
            {showImage && <img src={pic} alt="My picture" style={{ width: "200px", height: "200px" }} />}
        </div>
    );
}

export default KeyPadComponent;
