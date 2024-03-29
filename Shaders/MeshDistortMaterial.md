# MeshDistortMaterial
#### The MeshDistortMaterial is a custom shader material provided by Drei.js, which can be used to create a variety of interesting 3D effects in Three.js. The material applies a distortion effect to the geometry of the mesh, which can create effects such as ripples, waves, or bulges.

#### The MeshDistortMaterial works by taking a texture as input, which is used to define the distortion effect. The texture can be any image or data that can be loaded as a texture in Three.js, such as a PNG, JPG, or data URL. The texture is then used to displace the vertices of the mesh in a customizable way, creating the desired distortion effect.

#### The MeshDistortMaterial also provides a number of customizable parameters that can be used to fine-tune the effect, such as the intensity and frequency of the distortion, the speed of the animation, and the overall color of the material.

#### To use the MeshDistortMaterial, you need to first create a mesh object in Three.js and apply the material to it. You can then use the texture and the customizable parameters to create the desired distortion effect. Here is an example of how to create a mesh with the MeshDistortMaterial in Three.js:

```js
    import { MeshDistortMaterial } from 'drei';

    // create a mesh object with some geometry
    const geometry = new THREE.BoxGeometry(1, 1, 1);
    const mesh = new THREE.Mesh(geometry);

    // create a MeshDistortMaterial and set its parameters
    const material = new MeshDistortMaterial({
    color: 0xff0000, // set the color of the material
    distort: 0.4, // set the intensity of the distortion effect
    speed: 2, // set the speed of the animation
    displacementScale: 1, // set the scale of the displacement effect
    displacementBias: 0.5, // set the bias of the displacement effect
    map: myTexture, // set the texture to use for the distortion effect
    });

    // apply the material to the mesh
    mesh.material = material;
```

### Overall, the MeshDistortMaterial is a powerful tool for creating unique and dynamic 3D effects in Three.js, and it can be used to create a wide range of visual styles and animations.

#### [MeshDistortMaterial Drei.js](https://drei.pmnd.rs/?path=/story/shaders-meshdistortmaterial--mesh-distort-material-st)

______________________________________________________________________________________________________________

## Properties

* **dispose**

    is a method that is used to clean up the material when it is no longer needed. When you create a **MeshDistortMaterial**, it allocates GPU memory and other resources that need to be properly freed when the material is no longer in use. The **dispose** method is responsible for releasing these resources.

    To use the **dispose** method, you simply need to call it on the **MeshDistortMaterial** object that you want to dispose of. For example:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial(/* options */);

        // use the material

        material.dispose(); // dispose of the material when no longer needed
    ```

    The **dispose** method will free up any resources allocated by the **MeshDistortMaterial** and ensure that they are available for other parts of your application. It is good practice to always dispose of materials when they are no longer needed to avoid memory leaks and other performance issues.

    In addition to **MeshDistortMaterial**, most materials in Three.js have a **dispose** method, and it is generally a good practice to dispose of any materials or other resources that you no longer need in your application.

* **addEventListener**

    is a material class that is used to define the appearance of a 3D mesh in Three.js.

    However, the **addEventListener** method is commonly used in JavaScript to attach event listeners to DOM elements, such as HTML elements on a webpage. It is not directly related to the **MeshDistortMaterial** class or Three.js.

    In Three.js, you can attach event listeners to various objects, such as **Scene**, **Camera**, **Mesh**, etc. by using the **addEventListener** method provided by the **EventDispatcher** class. This allows you to handle various events, such as mouse clicks, keyboard inputs, or object interactions, and respond to them in your application.

    Here is an example of how you can use the **addEventListener** method in Three.js to handle a mouse click event on a mesh:

    ```js
        import { Mesh, EventDispatcher } from 'three';

        const mesh = new Mesh(/* geometry, material */);
        mesh.name = 'MyMesh';

        // create an event dispatcher and attach it to the mesh
        const dispatcher = new EventDispatcher();
        mesh.userData.dispatcher = dispatcher;

        // add a click event listener to the mesh
        mesh.addEventListener('click', (event) => {
        console.log(`Clicked on mesh "${event.target.name}"`);
        });

        // trigger the click event programmatically
        mesh.userData.dispatcher.dispatchEvent({ type: 'click', target: mesh });
    ```

    In this example, we create a **Mesh** object and attach an **EventDispatcher** object to it using the **userData** property. We then add a click event listener to the mesh and log a message when the event is triggered. Finally, we programmatically trigger the click event using the **dispatchEvent** method of the event dispatcher.

    Note that while the **addEventListener** method is not directly related to the **MeshDistortMaterial** class in Drei.js, it can be used to create interactive 3D applications using Three.js.

* **hasEventListener**

    is a material class that is used to define the appearance of a 3D mesh in Three.js.

    However, the **hasEventListener** method is commonly used in Three.js to check if a particular object has a certain type of event listener attached to it. It is used in conjunction with the **addEventListener** method, which is used to attach event listeners to objects.

    Here is an example of how you can use the **hasEventListener** method in Three.js to check if a mesh has a click event listener attached to it:

    ```js
        import { Mesh, EventDispatcher } from 'three';

        const mesh = new Mesh(/* geometry, material */);

        // create an event dispatcher and attach it to the mesh
        const dispatcher = new EventDispatcher();
        mesh.userData.dispatcher = dispatcher;

        // add a click event listener to the mesh
        mesh.addEventListener('click', (event) => {
        console.log(`Clicked on mesh`);
        });

        // check if the mesh has a click event listener
        const hasClickListener = mesh.userData.dispatcher.hasEventListener('click');
        console.log(`Mesh has click event listener: ${hasClickListener}`); // should print "true"
    ```

    In this example, we create a **Mesh** object and attach an **EventDispatcher** object to it using the **userData** property. We then add a click event listener to the mesh and log a message when the event is triggered. Finally, we use the **hasEventListener** method to check if the mesh has a click event listener attached to it.

    Note that while the **hasEventListener** method is not directly related to the **MeshDistortMaterial** class in Drei.js, it can be used to check if certain types of events are attached to any object in Three.js, including meshes that are using the **MeshDistortMaterial**.

* **removeEventListener**

    is commonly used in Three.js to remove event listeners that were previously attached to an object using the **addEventListener** method. This method is used to selectively remove event listeners from objects, which can help to improve performance and reduce memory usage in interactive applications.

    Here is an example of how you can use the **removeEventListener** method in Three.js to remove a click event listener from a mesh:

    ```js
        import { Mesh, EventDispatcher } from 'three';

        const mesh = new Mesh(/* geometry, material */);

        // create an event dispatcher and attach it to the mesh
        const dispatcher = new EventDispatcher();
        mesh.userData.dispatcher = dispatcher;

        // add a click event listener to the mesh
        const clickListener = (event) => {
        console.log(`Clicked on mesh`);
        };
        mesh.addEventListener('click', clickListener);

        // remove the click event listener from the mesh
        mesh.removeEventListener('click', clickListener);

        // check if the mesh still has a click event listener
        const hasClickListener = mesh.userData.dispatcher.hasEventListener('click');
        console.log(`Mesh has click event listener: ${hasClickListener}`); // should print "false"
    ```

    In this example, we create a **Mesh** object and attach an **EventDispatcher** object to it using the **userData** property. We then add a click event listener to the mesh and log a message when the event is triggered. Finally, we remove the click event listener using the **removeEventListener** method and verify that the mesh no longer has a click event listener attached to it.

    Note that while the **removeEventListener** method is not directly related to the **MeshDistortMaterial** class in Drei.js, it can be used to remove event listeners from any object in Three.js, including meshes that are using the **MeshDistortMaterial**.

* **dispatchEvent**

    is commonly used in Three.js to trigger events on objects that have event listeners attached to them. This method is used to trigger custom events or built-in events, such as click, mouseover, or keydown events, on objects in Three.js.

    Here is an example of how you can use the **dispatchEvent** method in Three.js to trigger a custom event on a mesh:

    ```js
        import { Mesh, EventDispatcher } from 'three';

        const mesh = new Mesh(/* geometry, material */);

        // create an event dispatcher and attach it to the mesh
        const dispatcher = new EventDispatcher();
        mesh.userData.dispatcher = dispatcher;

        // add a custom event listener to the mesh
        mesh.addEventListener('customEvent', (event) => {
        console.log(`Custom event triggered on mesh`);
        });

        // trigger the custom event on the mesh
        const customEvent = { type: 'customEvent' };
        mesh.userData.dispatcher.dispatchEvent(customEvent);
    ```

    In this example, we create a **Mesh** object and attach an **EventDispatcher** object to it using the **userData** property. We then add a custom event listener to the mesh and log a message when the event is triggered. Finally, we use the **dispatchEvent** method to trigger the custom event on the mesh.

    Note that while the **dispatchEvent** method is not directly related to the **MeshDistortMaterial** class in Drei.js, it can be used to trigger events on any object in Three.js, including meshes that are using the **MeshDistortMaterial**.

* **type**

    is used to identify the type of the material. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **type** property is a string that identifies the type of the material. In the case of the **MeshDistortMaterial**, the value of the **type** property is **'MeshDistortMaterial'**.

    Here is an example of how you can access the **type** property of a **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({/* options */});
        console.log(material.type); // should print "MeshDistortMaterial"
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class and log the value of its **type** property to the console. The output should be the string **"MeshDistortMaterial"**, which identifies the type of the material.

* **id**

    is a unique identifier assigned to each instance of the material. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **id** property is an integer that is automatically generated when the material instance is created. This property can be useful for debugging and tracking material instances in your code.

    Here is an example of how you can access the **id** property of a **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({/* options */});
        console.log(material.id); // should print a unique integer value
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class and log the value of its **id** property to the console. The output should be a unique integer value that identifies the material instance.

* **uuid**

    is a unique identifier assigned to each instance of the material. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **uuid** property is a string that is automatically generated when the material instance is created. This property can be useful for identifying and tracking material instances in your code, especially when working with scenes and objects that contain multiple materials.

    Here is an example of how you can access the **uuid** property of a **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({/* options */});
        console.log(material.uuid); // should print a unique string value
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class and log the value of its **uuid** property to the console. The output should be a unique string value that identifies the material instance.

* **name**

    is an optional string that can be used to give a name to the material instance. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **name** property can be useful for identifying and accessing material instances in your code, especially when working with scenes and objects that contain multiple materials.

    Here is an example of how you can set the **name** property of a **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({/* options */});
        material.name = 'myMaterial';
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class and set its **name** property to the string value **'myMaterial'**. This can be useful later on for identifying and accessing the material instance in your code.

* **visible**

    determines whether the material instance is visible or not. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **visible** property is a boolean value that is **true** by default, meaning that the material is visible in the scene. If you set the **visible** property to **false**, the material will be hidden from the scene.

    Here is an example of how you can set the **visible** property of a **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({/* options */});
        material.visible = false;
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class and set its **visible** property to **false**. This will make the material instance invisible in the scene.

* **userData**

    is an object that can be used to store custom data associated with the material instance. This property is inherited from the Material class in Three.js, which is the base class for all material types.

    The userData property can be useful for attaching additional information or metadata to the material instance, such as custom properties or data that is not directly related to the rendering of the material.

    Here is an example of how you can set the userData property of a MeshDistortMaterial instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({/* options */});
        material.userData = {
            foo: 'bar',
            baz: 42
        };
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class and set its **userData** property to an object with two properties: **foo** with the string value **'bar'** and **baz** with the number value **42**. This custom data can be accessed later on by other parts of your code that have access to the material instance.

* **toJSON**

    is a method that returns a JSON representation of the material instance. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **toJSON** method can be useful for serializing material instances to JSON format, which can then be stored or transmitted over a network. When a material instance is serialized using **toJSON**, all of its properties are included in the resulting JSON object, except for properties that have the value **undefined**.

    Here is an example of how you can use the **toJSON** method to serialize a **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({/* options */});
        const materialJson = material.toJSON();
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class and then call its **toJSON** method to serialize the material instance to a JSON object. The resulting **materialJson** object will contain all of the material's properties as key-value pairs in JSON format.

* **clone**

    is a method that creates a new instance of the material that is a copy of the original material instance. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **clone** method can be useful for creating multiple copies of a material with the same properties, but with different settings or parameters. When you **clone** a material instance using clone, a new instance of the material is created with all of the same property values as the original material.

    Here is an example of how you can use the **clone** method to create a copy of a MeshDistortMaterial instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const originalMaterial = new MeshDistortMaterial({/* options */});
        const clonedMaterial = originalMaterial.clone();
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class called **originalMaterial**. We then call its **clone** method to create a new instance of the material that is a copy of **originalMaterial**. The resulting **clonedMaterial** instance will have all of the same property values as **originalMaterial**.

* **copy**

    is a method that copies the properties of another material instance to the current material instance. This property is inherited from the **Material** class in Three.js, which is the base class for all material types.

    The **copy** method can be useful for copying the properties of one material instance to another instance, without having to create a new instance from scratch. When you call the **copy** method on a **MeshDistortMaterial** instance, the properties of the material instance passed as an argument are copied to the current material instance.

    Here is an example of how you can use the **copy** method to copy the properties of one **MeshDistortMaterial** instance to another instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material1 = new MeshDistortMaterial({/* options */});
        const material2 = new MeshDistortMaterial({/* options */});

        material2.copy(material1);
    ```

    In this example, we create two instances of the **MeshDistortMaterial** class called **material1** and **material2**. We then call the **copy** method on **material2**, passing **material1** as an argument. The properties of **material1** are copied to **material2**, so **material2** now has the same property values as **material1**.

* **opacity**

    is a value that determines the transparency of the material. It is a number between **0** and **1**, where **0** is completely transparent (invisible) and **1** is completely opaque (visible).

    The **opacity** property can be used to create materials that are partially transparent or to create materials that fade in or out over time. For example, you can set the **opacity** of a **MeshDistortMaterial** instance to **0.5** to create a material that is half transparent.

    Here is an example of how you can use the **opacity** property to create a partially transparent **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({
        opacity: 0.5,
        transparent: true,
        // other options...
        });
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class called **material**. We set its **opacity** property to **0.5**, which makes the material half transparent. We also set the **transparent** property to **true**, which tells the material to render with transparency enabled. Finally, we set any other options that we want for the material.

* **color**

    is a value that determines the color of the material. It can be set to any valid CSS color string, such as **red**, **#ff0000**, or **rgb(255, 0, 0)**.

    The **color** property can be used to create materials that have a solid color. For example, you can set the **color** property of a **MeshDistortMaterial** instance to red to create a material that is **red**.

    Here is an example of how you can use the **color** property to create a **MeshDistortMaterial** instance with a solid color in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({
        color: 'red',
        // other options...
        });
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class called **material**. We set its **color** property to red, which makes the material solid **red**. We also set any other options that we want for the material.

* **depthWrite**

    is a boolean value that determines whether or not the material should write to the depth buffer when it is rendered.

    The depth buffer is a part of the rendering pipeline that keeps track of the depth of each pixel as it is rendered. By default, when a material is rendered, it writes its depth value to the depth buffer. This allows the renderer to correctly handle situations where one object is in front of another, and ensures that objects are rendered in the correct order.

    However, in some cases, you may want to disable depth writing for a material. For example, if you have a transparent material that is blended with other objects in the scene, you may want to disable depth writing so that the transparent object doesn't overwrite the depth buffer for the objects behind it.

    Here is an example of how you can use the **depthWrite** property to disable depth writing for a **MeshDistortMaterial** instance in Drei.js:

    ```js
        import { MeshDistortMaterial } from 'drei';

        const material = new MeshDistortMaterial({
        depthWrite: false,
        // other options...
        });
    ```

    In this example, we create a new instance of the **MeshDistortMaterial** class called **material**. We set its **depthWrite** property to **false**, which tells the renderer not to write the material's depth to the depth buffer when it is rendered. We also set any other options that we want for the material.