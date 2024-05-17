# Ex06-Redirect the Scene
# Aim :
To Redirecting the scene in the unity engine.

# Algorithm :
# Step 1 :
To open the unity engine.

# Step 2 :
Create a new 3D project.

# Step 3 :
Create plane and name it as ground and create cube and name it as player.

# Step 4 :
Add WinText in Hierarchy.

# Step 5 :
Create a C# Script and name it as playercontroller and add the script to player.

# Step 6 :
Use the R button to change the level 2

# Step 7 :
Print the Output and end the program.

# Program 
```
DEVELOPED BY: VAISHNAVI S
REGISTER NUMBER : 212222230165
```

# CUBE PLAYER :
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class CubePlayer : MonoBehaviour
{
    Rigidbody rb;
    public GameObject WinText;
    // Start is called before the first frame update
    void Start()
    {
        rb = GetComponent<Rigidbody>();
        
    }

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }
        
    }
    private void OnCollisionEnter(Collision other)
    {
        if(other.gameObject.tag=="sphere")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}
```
# Output :
![329290373-6b2052e9-e3c0-4726-b179-1de163ce7f6a](https://github.com/Vaishnavi-saravanan/Ex06-Redirecting-the-Scene/assets/118541897/cef1a5b5-e9b3-4a7c-bd7d-e48658b2bbda)

# Result :
The above C# coding is successfully redirecting the scene in the unity engine.
