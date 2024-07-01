using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class playerMove : MonoBehaviour
{

    public float speed = 8.0f;
    //speed rotation
    public float rotationSpeed = 80f;
    //referencia a rifybody
    private Rigidbody physics;
    //Fuerza de salto
    public float jumpForce = 1.0f;

    // Start is called before the first frame update
    void Start()
    {
        
        Cursor.lockState = CursorLockMode.Locked;
        Cursor.visible = false;

        //Iniciamos el componente de rigibody
        physics = GetComponent<Rigidbody>();

    }

    // Update is called once per frame
    void Update()
    {
        float horizontal = Input.GetAxis("Horizontal");
        float vertical = Input.GetAxis("Vertical");

        transform.Translate(new Vector3(-horizontal,0.0f, -vertical)*Time.deltaTime*speed);

        //rotation 
        float rotationY = Input.GetAxis("Mouse X");
        transform.Rotate(new Vector3(0,rotationY*Time.deltaTime*rotationSpeed,0.0f));

        //salto
        if(Input.GetKeyDown("space")){
            physics.AddForce(new Vector3(0,jumpForce,0),ForceMode.Impulse);
        }


    }
}
