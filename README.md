This Python script performs image-based steganography by embedding a secret message into an image and later decrypting it using a password. The script begins by reading an image (mypic.jpg) using OpenCV (cv2.imread). The user is prompted to enter a secret message and a password, which will be used for encryption and decryption. The script then creates two dictionaries: one for mapping characters to ASCII values and another for reversing the mapping. These mappings are used to encode the message into pixel values of the image. The embedding process iterates through each character of the message and modifies the pixel values in the image accordingly. The pixel coordinates (n, m, z) are incremented to ensure each character is distributed across different color channels (Red, Green, and Blue). Once the message is embedded, the modified image is saved as encryptedImage.jpg and opened automatically using the os.system command.

For decryption, the user is required to input the correct password. If the entered password matches the original one, the script retrieves the hidden message by reversing the encoding process. It reads the pixel values and reconstructs the message using the ASCII mapping. If the password is incorrect, the program displays a message denying access to decryption.

Key Features:
Image-Based Encryption: The script embeds a secret message inside an image by modifying pixel values.
Character-to-ASCII Mapping: Uses ASCII values to encode and decode messages efficiently.
Pixel Manipulation: Distributes message characters across different color channels for encryption.
Password Protection: Ensures that only authorized users can decrypt the message.
Automated Image Handling: Saves and opens the encrypted image automatically.
Simple and Effective: Uses a straightforward approach to steganography with minimal computation.
