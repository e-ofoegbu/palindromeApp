# palindromeApp
My own palindrome app i have been working on




let inputData = "Masam";

const advancedPalindrome = () => {
    const numberCheck = (inputData) => {
        if (typeof inputData !== 'number') {
            return false;
        } else {
            return true;
        }
    }
    numberCheck(inputData);

    const integerCheck = (inputData) => {
        if (Number.isInteger(inputData) === true) {
            return true;
        } else {
            return false;
        }
    }
    integerCheck(inputData);

    const palindrome = (inputData) => {
        let outputData = inputData.toString().split("").reverse().join("");
        return inputData == outputData ? true : false;
    }

    palindrome(inputData);

    if (numberCheck(inputData) == true && integerCheck(inputData) == true && palindrome(inputData) == true) {
        console.log('This is a number, an integer and a palindrome');
    } else if (numberCheck(inputData) == true && integerCheck(inputData) == true && palindrome(inputData) == false) {
        console.log('This is a number, an integer but not a palindrome');
    } else if (numberCheck(inputData) == true && integerCheck(inputData) == false && palindrome(inputData) == true) {
        console.log('This is a number and a palindrome but not an integer');
    } else if (numberCheck(inputData) == true && integerCheck(inputData) == false && palindrome(inputData) == false) {
        console.log('This is a number but not an integer or a palindrome');
    } else if (numberCheck(inputData) == false && integerCheck(inputData) == false && palindrome(inputData) == true) {
        console.log('This is not a number or an integer but is a palindrome');
    } else {
        console.log('This is not a number, an integer or a palindrome');
    }
}
advancedPalindrome();
