# MeshReflectorMaterial
#### The MeshReflectorMaterial is a component of the drei library that provides a material for creating reflections on 3D objects in a WebXR application.

#### A material in a 3D graphics application is used to define the appearance of an object, including its color, texture, and how it responds to light. The MeshReflectorMaterial is a specialized material that is designed to create reflections on the surface of an object, which can help to make the object appear more realistic and add depth to the scene.

#### The MeshReflectorMaterial component takes advantage of the capabilities of WebXR to create reflections by rendering a reflection map of the scene and applying it to the surface of the object. The reflection map is updated in real-time as the camera moves, allowing the reflections to respond to the changing environment in a natural way.

#### The MeshReflectorMaterial component can be used in combination with other components from the drei library, such as lights, cameras, and 3D objects, to create complex and interactive 3D scenes in a web application.

#### [MeshReflectorMaterial Drei.js](https://drei.pmnd.rs/?path=/story/shaders-meshreflectormaterial--reflector-st)

______________________________________________________________________________________________________________

## Properties

* **dispose**

    is a method that is used to dispose of the resources associated with the material.

    In a 3D graphics application, materials can consume significant amounts of memory and computational resources, especially when they involve reflections and other complex effects. The "dispose" property provides a way to clean up these resources when they are no longer needed.

    When you call the "dispose" method on a MeshReflectorMaterial, it will release any memory and other resources that are associated with the material, freeing up resources for other parts of the application to use. This is particularly important when working with complex 3D scenes that may contain many materials, objects, and other resources.

    In general, you should call the "dispose" method on a MeshReflectorMaterial when you are finished using it, or when you want to replace it with another material. This will help to ensure that the resources associated with the material are cleaned up in a timely and efficient manner, and will prevent potential performance issues in your 3D application.

* **addEventListener**

    is a method that is used in JavaScript to attach event listeners to an element.

    In JavaScript, events are notifications that are sent to your script when certain things happen in the web page, such as a user clicking a button, a page finishing loading, or an element being updated. Event listeners are functions that are called when an event occurs, allowing you to respond to the event and take some action.

    The "addEventListener" method is used to attach an event listener to an element. You can specify the type of event you want to listen for (such as "click", "load", or "mousemove"), and the function you want to be called when the event occurs. For example:

    ```js
        document.querySelector("button").addEventListener("click", function() {
            console.log("Button was clicked");
        });
    ```

    In this example, an event listener is attached to a button element, and it will log a message to the console whenever the button is clicked.

    The "addEventListener" method is a powerful tool for working with events in JavaScript, and is used in many different types of web applications, including games, interactive user interfaces, and more.

* **hasEventListener**

    The "hasEventListener" property is typically used to check whether a specific event listener has been added to an element. In some libraries, it might return a Boolean value indicating whether an event listener with a specific type and function has been attached to an element.

    For example:

    ```js
        var button = document.querySelector("button");
        var listener = function() { console.log("Button was clicked"); };

        button.addEventListener("click", listener);

        if (button.hasEventListener("click", listener)) {
            console.log("Event listener is attached to the button");
        }
    ```

    In this example, the "hasEventListener" property is used to check whether the specified event listener has been attached to the button element. If it has, a message is logged to the console.

    Please note that the exact implementation and usage of the "hasEventListener" property may vary depending on the library or framework you are using. Some libraries provide this functionality as part of their API, while others do not. If you are working with a specific library, it is best to consult the documentation for that library to learn how to use the "hasEventListener" property.

* **removeEventListener**

    is a method used in JavaScript to remove an event listener from an element.

    In JavaScript, events are notifications that are sent to your script when certain things happen in the web page, such as a user clicking a button, a page finishing loading, or an element being updated. Event listeners are functions that are called when an event occurs, allowing you to respond to the event and take some action.

    The "addEventListener" method is used to attach an event listener to an element, and the "removeEventListener" method is used to remove an event listener from an element. You can use the "removeEventListener" method to remove event listeners that you no longer need, or to stop responding to an event that is no longer relevant.

    For example:

    ```js
        var button = document.querySelector("button");
        var listener = function() { console.log("Button was clicked"); };

        button.addEventListener("click", listener);

        // Later on in your code...

        button.removeEventListener("click", listener);
    ```

    In this example, an event listener is added to the button element using the "addEventListener" method, and later removed using the "removeEventListener" method.

    It is important to remove event listeners that you no longer need, as leaving them attached can lead to memory leaks and other performance issues. Additionally, removing event listeners can help to keep your code organized and easy to maintain.

* **dispatchEvent**

    is a method used in JavaScript to manually trigger an event on an element.

    In JavaScript, events are notifications that are sent to your script when certain things happen in the web page, such as a user clicking a button, a page finishing loading, or an element being updated. Event listeners are functions that are called when an event occurs, allowing you to respond to the event and take some action.

    The "dispatchEvent" method is used to manually trigger an event on an element. When you call this method, an event of the specified type is created and dispatched to the element, as if it had occurred naturally in the web page. This can be useful when you need to simulate an event, or when you want to trigger an event programmatically.

    For example:

    ```js
        var button = document.querySelector("button");
        var clickEvent = new Event("click");

        button.dispatchEvent(clickEvent);
    ```

    In this example, a new "click" event is created using the "Event" constructor, and then dispatched to the button element using the "dispatchEvent" method. This will trigger any event listeners that are attached to the button for the "click" event, just as if the button had been clicked by a user.

    The "dispatchEvent" method is a powerful tool for working with events in JavaScript, and can be used in many different types of web applications, including games, interactive user interfaces, and more.

* **type**

    it typically refers to the type of object or component that is being represented.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "type" property would indicate the type of material that is being used to render the mesh. For example, the "type" property of a MeshReflectorMaterial component would likely be set to "MeshReflectorMaterial".

    Here is an example of how the "type" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
        });

        console.log(material.type); // "MeshReflectorMaterial"
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created and its "type" property is logged to the console.

    The exact behavior and usage of the "type" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **id**

    it typically refers to a unique identifier for an object or component.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "id" property would likely be a unique identifier for the material that is used to render a mesh.

    Here is an example of how the "id" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
        });

        console.log(material.id); // "MeshReflectorMaterial_1" (or some other unique identifier)
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created and its "id" property is logged to the console. The "id" property is a unique identifier for the material, which can be used to refer to the material in other parts of the code.

    The exact behavior and usage of the "id" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **uuid**

    it typically refers to a universally unique identifier for an object or component.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "uuid" property would likely be a universally unique identifier for the material that is used to render a mesh.

    Here is an example of how the "uuid" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
        });

        console.log(material.uuid); // "7ddd0a48-7074-4f1d-a3b3-3328fbeab59b" (or some other universally unique identifier)
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created and its "uuid" property is logged to the console. The "uuid" property is a universally unique identifier for the material, which can be used to refer to the material in other parts of the code or across different systems.

    The exact behavior and usage of the "uuid" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **name**

    it typically refers to a human-readable string that can be used to identify an object or component.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "name" property would likely be a string that can be used to identify the material that is used to render a mesh.

    Here is an example of how the "name" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
            name: "RedMaterial",
        });

        console.log(material.name); // "RedMaterial"
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created and its "name" property is set to "RedMaterial". The "name" property is a string that can be used to identify the material, which can be helpful for organizing and managing materials in larger projects.

    The exact behavior and usage of the "name" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **visible**

    it typically refers to a boolean value that determines whether an object or component should be visible or not.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "visible" property would likely be a boolean value that determines whether the material that is used to render a mesh should be visible or not.

    Here is an example of how the "visible" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
            visible: false,
        });

        console.log(material.visible); // false
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created and its "visible" property is set to false. The "visible" property is a boolean value that determines whether the material should be visible or not. If the "visible" property is set to false, the mesh that uses this material will not be visible.

    The exact behavior and usage of the "visible" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **userData**

    it typically refers to a boolean value that determines whether an object or component should be visible or not.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "visible" property would likely be a boolean value that determines whether the material that is used to render a mesh should be visible or not.

    Here is an example of how the "visible" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
            visible: false,
        });

        console.log(material.visible); // false
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created and its "visible" property is set to false. The "visible" property is a boolean value that determines whether the material should be visible or not. If the "visible" property is set to false, the mesh that uses this material will not be visible.

    The exact behavior and usage of the "visible" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **toJSON**

    it typically refers to a method that returns a JSON representation of an object or component.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "toJSON" property would likely be a method that returns a JSON representation of the material. This method can be useful for serializing the material and storing its state, or for transmitting the material information over a network.

    Here is an example of how the "toJSON" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
        });

        console.log(material.toJSON());
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created, and its "toJSON" property is called to get a JSON representation of the material. The exact format of the JSON data will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js.

    The exact behavior and usage of the "toJSON" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **clone**

    it typically refers to a method that creates a new instance of an object or component that is a copy of an existing instance.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "clone" property would likely be a method that creates a new instance of the material that is a copy of the existing material. This method can be useful for creating new materials with the same properties as an existing material.

    Here is an example of how the "clone" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material1 = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
        });

        const material2 = material1.clone();

        console.log(material1 === material2); // false
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created (material1), and then the "clone" property is used to create a new instance of the material that is a copy of material1 (material2). The two instances are then compared, and it is demonstrated that they are not the same instance, but are instead separate instances with the same properties.

    The exact behavior and usage of the "clone" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **copy**

    it typically refers to a method that creates a new instance of an object or component that is a copy of an existing instance.

    In the context of the MeshReflectorMaterial component from the Drei.js library, the "copy" property would likely be a method that creates a new instance of the material that is a copy of the existing material. This method can be useful for creating new materials with the same properties as an existing material.

    Here is an example of how the "copy" property might be used with the MeshReflectorMaterial component in Drei.js:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material1 = new MeshReflectorMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
        });

        const material2 = material1.copy();

        console.log(material1 === material2); // false
    ```

    In this example, a new instance of the MeshReflectorMaterial component is created (material1), and then the "copy" property is used to create a new instance of the material that is a copy of material1 (material2). The two instances are then compared, and it is demonstrated that they are not the same instance, but are instead separate instances with the same properties.

    The exact behavior and usage of the "copy" property will depend on the specific implementation of the MeshReflectorMaterial component in Drei.js. It is always best to consult the Drei.js documentation for the most up-to-date and accurate information.

* **opacity**

    it controls the transparency level of the material, where a value of 0 is completely transparent and a value of 1 is completely opaque.

* **blur**

    in 3D graphics, the term "blur" typically refers to a post-processing effect that simulates the way that objects appear out of focus when viewed through a camera lens. This effect is also known as depth of field.

* **resolution**

    is used to control the resolution of the material's texture. Specifically, it determines the size of the texture buffer used for rendering the reflection.

    The ***resolution*** property is an object with two properties: ***x*** and ***y***, which specify the width and height of the texture buffer, respectively. The default value of ***resolution*** is ***{x: 256, y: 256}***.

    You can adjust the ***resolution*** property to increase or decrease the quality of the reflection effect. Higher values of x and y will result in a sharper and more detailed reflection, but may impact performance, especially on low-end devices. Lower values of ***x*** and ***y*** will result in a less detailed reflection, but may improve performance.

* **color**

    is used to specify the color of the material. It is a ***THREE.Color*** instance, which represents a color value as a combination of red, green, and blue components.

    You can set the ***color*** property to any valid color value, including a CSS-style color string (e.g. ***"red"***, ***"#ff0000"***, or ***"rgb(255, 0, 0)"***), a hexadecimal value (e.g. ***0xff0000***), or a ***THREE.Color*** instance.

    For example, to set the ***color*** property of a ***MeshReflectorMaterial*** instance to red, you can do:

    ```js
        import { MeshReflectorMaterial } from 'drei';
        import * as THREE from 'three';

        const material = new MeshReflectorMaterial({
            color: new THREE.Color('red'),
            // ... other options
        });
    ```

    Note that the ***color*** property only affects the appearance of the reflection, not the underlying geometry of the material.

* **depthWrite**

    is a boolean value that indicates whether or not the material should write to the depth buffer when rendered. When ***depthWrite*** is set to ***false***, the material will not write to the depth buffer, allowing other objects behind it to be visible.

    The depth buffer is used by the renderer to determine which objects should be visible and which should be hidden based on their distance from the camera. When ***depthWrite*** is set to ***true***, the material will write to the depth buffer, which means that it will be considered in the visibility calculation, and other objects that are behind it may be occluded.

    By default, ***depthWrite*** is set to ***true***. If you want to prevent the material from writing to the depth buffer, you can set it to ***false***, like this:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            // ... other options
            depthWrite: false,
        });
    ```

    Setting ***depthWrite*** to ***false*** can be useful in certain situations, such as when rendering transparent materials or when you want to create special effects that require multiple passes of the renderer. However, be careful when using this property, as it can affect the visual quality and performance of your scene.

* **side**

    is used to specify which side of the material should be rendered.

    In three.js, each ***Material*** object can be configured to render either the front face, the back face, or both faces of the associated ***Geometry***. This is important for rendering objects with non-closed geometries, such as planes or cylinders, where the back faces may be visible depending on the camera position.

    The ***side*** property can be set to one of the following values:

    ***THREE.FrontSide***: Only render the front face of the material.
    ***THREE.BackSide***: Only render the back face of the material.
    ***THREE.DoubleSide***: Render both the front and back faces of the material.

    By default, the ***side*** property of ***MeshReflectorMaterial*** is set to ***THREE.FrontSide***, which means that only the front face of the material will be rendered. You can set it to a different value when creating a new material, like this:

    ```js
        import { MeshReflectorMaterial } from 'drei';
        import * as THREE from 'three';

        const material = new MeshReflectorMaterial({
            // ... other options
            side: THREE.DoubleSide,
        });
    ```

    In this example, the material is configured to render both the front and back faces of the associated ***Geometry***. Note that rendering both faces can be more computationally expensive than rendering only one face, and may affect the performance of your scene.

* **blending**

    it determines how the material is blended with the background when rendered.

    It is an enumeration of the ***THREE*** library, which can take any of the following values:

    ***THREE.NoBlending***: This is the default value, which means that the material is not blended with the background.

    ***THREE.NormalBlending***: This blends the material with the background using the normal blend equation.

    ***THREE.AdditiveBlending***: This blends the material with the background using the additive blend equation.

    ***THREE.SubtractiveBlending***: This blends the material with the background using the subtractive blend equation.

    ***THREE.MultiplyBlending***: This blends the material with the background using the multiply blend equation.

    ***THREE.CustomBlending***: This allows for a custom blend function to be specified using the ***blendSrc***, ***blendDst***, ***blendSrcAlpha***, and ***blendDstAlpha*** properties.

    The ***blending*** property is often used to create transparent materials or to simulate lighting effects.

* **toneMapped**

    is a boolean value that specifies whether or not the material's colors should be tone-mapped.

    Tone-mapping is a process that maps high dynamic range (HDR) colors to low dynamic range (LDR) colors for display on standard monitors. This is necessary because most monitors cannot display the full range of brightness values that can be represented in HDR images.

    When ***toneMapped*** is set to ***true***, the material's colors will be tone-mapped using the tone-mapping function specified by the renderer's ***toneMapping*** property. When ***toneMapped*** is set to ***false***, the material's colors will not be tone-mapped.

    Note that if you are using the ***MeshReflector*** component from the drei library, you should set the ***toneMapped*** property of its material to ***false*** in order to avoid issues with reflections appearing too bright.

* **transparent**

    is a boolean value that specifies whether or not the material is transparent.

    When ***transparent*** is set to ***true***, the material's opacity can be set to a value less than 1 using the ***opacity*** property. This allows the material to be partially see-through, which can be useful for creating effects like stained glass or water.

    If ***transparent*** is set to ***false***, the material will be completely opaque and the ***opacity*** property will have no effect.

    Note that when using transparent materials, you may need to set the ***depthWrite*** property to ***false*** in order to avoid z-fighting issues. Z-fighting occurs when two objects are rendered at almost the same depth and the renderer is unable to determine which one should be in front. Setting ***depthWrite*** to ***false*** disables depth writing for the material, which can help to reduce z-fighting.

* **vertexColors**
    
    is used to specify whether the material uses per-vertex coloring or not. If the value is set to ***THREE.NoColors***, the material ignores any vertex colors. If the value is set to ***THREE.VertexColors***, the material uses the vertex colors for coloration. By default, ***vertexColors*** is set to ***THREE.NoColors***.

    In three.js, vertex colors can be defined for a geometry by setting the ***color*** attribute of the geometry. Each vertex in the geometry can have a different color. The ***vertexColors*** property of a material determines whether or not to use these vertex colors in the rendering of the material. If ***vertexColors*** is set to ***THREE.VertexColors***, then the vertex colors will be used to color the geometry.

* **alphaToCoverage**

    is a boolean that determines whether or not to enable alpha to coverage. Alpha to coverage is a technique that is used in computer graphics to improve the visual quality of transparency in images with rough or jagged edges.

    When ***alphaToCoverage*** is enabled, it works by using the alpha value of the pixels in the image to determine how many samples of that pixel should be covered. This can help to produce smoother edges and prevent jagged lines and other artifacts that may appear when using transparent materials in a scene.

    The ***alphaToCoverage*** property is used in conjunction with other properties of the material, such as the ***opacity*** and ***transparent*** properties, to achieve the desired visual effect.

* **wireframe**

    is a boolean that determines whether or not the material should be rendered as a wireframe. When this property is set to ***true***, the material will be rendered as a wireframe, which means that only the edges of the triangles that make up the mesh will be drawn. When this property is set to ***false*** (which is the default), the material will be rendered normally, with filled triangles. The wireframe rendering mode can be useful for debugging or for creating certain artistic effects.

* **alphaTest**

    is a numerical value between 0 and 1 that determines the minimum alpha value that a pixel must have in order to be rendered.

    If the alpha value of the pixel is less than the specified ***alphaTest*** value, the pixel is not rendered, effectively creating a transparent effect.

    This property is commonly used for textures with transparent areas, where the goal is to render only the opaque areas of the texture while leaving the transparent areas invisible. By setting the ***alphaTest*** value to a threshold slightly above 0, it is possible to achieve this effect.

* **blendDst**

    is used to set the destination blending factor for the material.

    In three.js, blending is used to control how transparent objects are rendered when they overlap with each other. The ***blendDst***property sets the blending destination factor, which determines how the output color is combined with the background color.

    The ***blendDst*** property of the ***MeshReflectorMaterial*** component can be set to one of the blending factors defined in the ***THREE*** object, such as ***THREE.OneMinusSrcAlphaFactor***, ***THREE.DstAlphaFactor***, ***THREE.DstColorFactor***, and so on. The default value of the ***blendDst*** property is ***THREE.OneMinusSrcAlphaFactor***.

* **blendDstAlpha**

    is a property that defines the destination alpha factor for the material's blend equation. This property is used in conjunction with the ***blendEquation*** and ***blendSrcAlpha*** properties to control how the material's color and transparency are blended with the underlying pixels in the scene.

    The ***blendDstAlpha*** property is a numerical value that represents the weight or intensity of the destination alpha factor. It ranges from 0 to 1, with 0 representing a fully transparent alpha channel and 1 representing a fully opaque alpha channel. The default value of this property is 1.

* **blendEquation**

    is a property that determines the mathematical operation used to combine the source and destination colors during blending.

    In the context of WebGL and Three.js, blending refers to the process of combining the color of a pixel in the output image with the color of the pixel already present in the same location. The ***blendEquation*** property is used to set the type of operation used for this process.

    The ***blendEquation*** property of the ***MeshReflectorMaterial*** can take one of the following constants as its value:

    * ***AddEquation***: The source and destination colors are added together.
    * ***SubtractEquation***: The destination color is subtracted from the source color.
    * ***ReverseSubtractEquation***: The source color is subtracted from the destination color.
    * ***MinEquation***: The minimum of the source and destination colors is used.
    * ***MaxEquation***: The maximum of the source and destination colors is used.

    By default, the ***blendEquation*** property of the ***MeshReflectorMaterial*** is set to ***AddEquation***.

* **blendEquationAlpha**

    is used to set the equation used for blending the alpha component of the source and destination colors.

    In three.js, blending is a way to combine transparent objects with the background. Blending is determined by two factors: the blend function and the blend equation. The blend function determines how the source and destination colors are combined, while the blend equation determines how the result of the blend function is combined with the background color.

    The ***blendEquationAlpha*** property sets the blend equation used for the alpha component. The possible values are:

    * ***AddEquationAlpha***: Add the source alpha component to the destination alpha component.
    * ***SubtractEquationAlpha***: Subtract the source alpha component from the destination alpha component.
    * ***ReverseSubtractEquationAlpha***: Subtract the destination alpha component from the source alpha component.
    * ***MinEquationAlpha***: Use the minimum of the source and destination alpha components.
    * ***MaxEquationAlpha***: Use the maximum of the source and destination alpha components.

    By default, the ***blendEquationAlpha*** property is set to ***AddEquationAlpha***.

* **blendSrc**

    is a property that determines how the material's color should be blended with the existing color in the scene when the material is rendered.

    The value of ***blendSrc*** property is a constant that defines the blending factor for the source color (the color of the material being rendered). Some possible values for ***blendSrc*** include:

    * ***THREE.ZeroFactor***: The source color is not blended with the existing color in the scene.
    * ***THREE.OneFactor***: The source color is completely blended with the existing color in the scene.
    * ***THREE.SrcAlphaFactor***: The source color's alpha channel is used as the blending factor.
    * ***THREE.DstAlphaFactor***: The existing color's alpha channel is used as the blending factor.
    * ***THREE.OneMinusSrcAlphaFactor***: The inverse of the source color's alpha channel is used as the blending factor.

    The ***blendSrc*** property works in conjunction with the ***blendDst*** property to determine the final blending of colors during rendering.

* **blendSrcAlpha**

    it specifies the alpha value to be used as the source factor in the alpha blending equation. This property works in conjunction with the ***blendDstAlpha*** property, which specifies the alpha value to be used as the destination factor.

    In alpha blending, the source factor specifies how much of the source color to use, and the destination factor specifies how much of the destination color to use. The alpha values of the source and destination colors are also used in the blending equation.

    The ***blendSrcAlpha*** property is set to ***null*** by default, which means that the value of the ***blendSrc*** property is used for the alpha blending equation. If you want to use a different value for the source alpha factor, you can set the ***blendSrcAlpha*** property to a different value.

* **clipIntersection**

    is a property in three.js that controls whether the material should be clipped when intersecting with other objects in the scene. When set to ***true***, the material will be clipped based on its intersection with other objects, and when set to ***false***, the material will not be clipped at its intersections.

    This property can be set on any material in three.js that inherits from ***Material***, such as ***MeshBasicMaterial***, ***MeshLambertMaterial***, ***MeshPhongMaterial***, and others.

* **clippingPlanes**

    is used to specify an array of clipping planes to be used when rendering the material. Clipping planes are used to define a region of space in which objects will be visible or hidden.

    The ***clippingPlanes*** property is an array of ***THREE.Plane*** objects that define the clipping planes. The planes are defined in object space, and will be transformed into world space by the renderer when the material is rendered.

    For example, to create a ***MeshReflectorMaterial*** that uses a single clipping plane, you could use the following code:

    ```js
        import { MeshReflectorMaterial } from 'drei';
        import * as THREE from 'three';

        const material = new MeshReflectorMaterial({
            clippingPlanes: [new THREE.Plane(new THREE.Vector3(0, 1, 0), 0)]
        });
    ```

    In this example, a single clipping plane is created that lies in the ***x-y*** plane (the normal vector is ***[0, 1, 0]***) and passes through the origin (the distance is ***0***).

* **clipShadows**

    it is actually a property of the ***MeshStandardMaterial*** class in the three.js library.

    The ***clipShadows*** property is a boolean value that indicates whether the material should be clipped against shadows. When set to ***true***, the material is clipped against shadows cast by other objects in the scene, resulting in a more realistic and accurate rendering of shadows.

    When ***clipShadows*** is set to ***true***, the material is excluded from the calculation of shadows, making the rendering more efficient. However, this can result in artifacts when the material is intersecting with shadow volumes.

    Here is an example of how to set the ***clipShadows*** property in three.js:

    ```js
        const material = new THREE.MeshStandardMaterial({
            color: 0xff0000,
            roughness: 0.5,
            metalness: 0.5,
            clipShadows: true, // enable shadow clipping
        });
    ```

* **colorWrite**

    controls whether the material writes to the color buffer. If set to ***false***, the material will not write any color to the buffer. If set to ***true*** (the default value), the material will write its color to the buffer.

    This property is inherited from ***THREE.Material***, which is the base class for all materials in the Three.js library. It is used to optimize rendering performance, by allowing materials to skip writing color data to the color buffer when it is not needed.

* **defines**

    is an object that contains a set of preprocessor macros used during the shader compilation process. These macros define constants and variables that can be used in the shader code.

    The ***defines*** object has several properties, including:

    * ***REFLECTOR***: A boolean value that indicates whether the material is a reflector material or not.
    * ***CLIPPING***: A boolean value that indicates whether clipping planes are enabled or not.
    * ***NUM_CLIPPING_PLANES***: An integer value that indicates the number of clipping planes.
    * ***OVERDRAW***: A boolean value that indicates whether overdraw is enabled or not.

    The ***defines*** property is used internally by ***MeshReflectorMaterial*** to generate the shader code for the material. You can customize the behavior of the material by modifying the values of the properties in the ***defines*** object.

* **depthFunc**

    specifies the depth comparison function used when rendering the material. It determines how the material is compared to the depth buffer to determine if it should be drawn.

    The ***depthFunc*** property takes an integer value that corresponds to one of the depth comparison functions supported by WebGL. These functions include:

    * ***Never***: never passes
    * ***Less***: passes if the incoming depth value is less than the stored depth value
    * ***Equal***: passes if the incoming depth value is equal to the stored depth value
    * ***Lequal***: passes if the incoming depth value is less than or equal to the stored depth value
    * ***Greater***: passes if the incoming depth value is greater than the stored depth value
    * ***Notequal***: passes if the incoming depth value is not equal to the stored depth value
    * ***Gequal***: passes if the incoming depth value is greater than or equal to the stored depth value
    * ***Always***: always passes

    The default value of ***depthFunc*** is ***Less***.

* **depthTest**

    is a boolean that indicates whether depth testing is enabled. Depth testing is a technique used in 3D graphics to ensure that objects that are closer to the camera appear in front of objects that are farther away.

    When ***depthTest*** is set to ***true***, objects will be compared against the depth buffer to determine whether they are visible. If an object is behind another object that has already been drawn, it will not be drawn. If ***depthTest*** is set to ***false***, all objects will be drawn in the order they are specified in the scene, regardless of their distance from the camera.

    In the case of ***MeshReflectorMaterial***, setting ***depthTest*** to ***false*** might be useful if you want to draw reflections of objects that are behind the reflecting surface. However, this can also result in incorrect rendering in some cases, so it should be used with care.

* **polygonOffset**

    is used to specify a ***Vector2*** representing the polygon offset factor and units for the material. The polygon offset is used to prevent z-fighting when rendering overlapping polygons by slightly offsetting the depth of the polygons. This can be useful when rendering materials that have the same depth values and are overlapping.

    In ***MeshReflectorMaterial***, the ***polygonOffset*** property is an optional property that can be used to create a new instance of the material with the specified polygon offset settings. Here is an example:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 'red',
            polygonOffset: true,
            polygonOffsetFactor: 1,
            polygonOffsetUnits: 1
        });
    ```

    In this example, the ***polygonOffset*** property is set to ***true*** to enable the polygon offset feature, and the ***polygonOffsetFactor*** and ***polygonOffsetUnits*** properties are set to 1 to specify the offset factor and units.

* **polygonOffsetFactor**

    it sets the value used to create a ***polygonOffset*** for polygons being rendered. It is used to avoid "z-fighting" artifacts, where two polygons are coplanar or almost coplanar, and as a result, the depth buffer cannot correctly determine which polygon to draw in front.

    The ***polygonOffsetFactor*** property is a float value that determines the factor by which to multiply the maximum depth slope in order to create the polygon offset. A positive value pushes the polygons closer to the camera, while a negative value pushes them farther away.

* **polygonOffsetUnits**

    is a float value that represents the amount by which the depth value is offset for polygons that are coplanar. It is used to prevent z-fighting (or "depth fighting") between polygons that are at the same depth in the scene.

    When ***polygonOffset*** is enabled, the depth value for a polygon is offset by ***polygonOffsetFactor * DZ + polygonOffsetUnits * r***, where ***DZ*** is the change in depth caused by projecting the polygon onto the screen, ***r*** is the smallest value that is guaranteed to produce a resolvable difference in depth values, and ***polygonOffsetFactor*** and ***polygonOffsetUnits*** are user-defined values.

    In ***MeshReflectorMaterial***, ***polygonOffset*** is disabled by default, and the ***polygonOffsetFactor*** and ***polygonOffsetUnits*** properties are set to 0.

* **precision**

    it sets the string value that specifies the shader precision. It corresponds to the ***precision*** qualifier in GLSL, which specifies the minimum precision of floating-point values used in the shader.

    In three.js, the precision ***property*** is used to set the shader precision for custom materials. It is a string value that can be set to one of the following: "highp", "mediump", or "lowp", corresponding to high, medium, or low precision respectively. The default value is "highp".

* **premultipliedAlpha**

    it specifies whether the alpha channel of the texture is premultiplied with its color values.

    In computer graphics, premultiplied alpha is a technique for compositing transparent images that improves performance and accuracy by pre-multiplying the alpha values of an image with its color values. When premultiplied alpha is used, the resulting color values are a combination of the alpha value and the color value, resulting in an image that is more accurately blended with the underlying image or background.

    In the context of ***MeshReflectorMaterial***, setting ***premultipliedAlpha*** to ***true*** will cause the material to take into account premultiplied alpha when blending with the scene. This can help improve the accuracy of the reflection and improve performance by reducing the number of blending operations required.

* **forceSinglePass**

    is a boolean value that indicates whether the material should use a single-pass rendering technique, regardless of whether or not the device supports multi-pass rendering.

    In general, multi-pass rendering is a technique used in 3D graphics that involves rendering the same scene multiple times, each time with different settings or techniques applied. For example, in order to create a reflection effect, a second pass could be used to render the reflection of an object onto a mirror surface. This can be an expensive process, as it requires rendering the scene multiple times.

    In contrast, single-pass rendering involves rendering the entire scene in a single pass. This can be more efficient, as it reduces the number of times the scene needs to be rendered.

    The ***forceSinglePass*** property in ***MeshReflectorMaterial*** allows developers to choose between these techniques, regardless of whether the device supports multi-pass rendering or not. This can be useful in situations where the scene is simple enough that single-pass rendering is sufficient, or where multi-pass rendering is not performing well on a particular device.

* **dithering**

    is a boolean value that specifies whether or not to apply dithering to the material.

    Dithering is a technique used to reduce banding artifacts in images with limited color depth or when transitioning from one color to another. It adds noise to the image to simulate more colors than are actually present, which can help smooth out transitions and make them appear more natural.

    In the context of the ***MeshReflectorMaterial*** component, setting the ***dithering*** property to ***true*** can help to reduce visual artifacts and improve the overall quality of the reflected image.

* **shadowSide**

    it is a property of the ***MeshReflectorMaterial*** component from the Drei library in Three.js.

    The ***shadowSide*** property determines which faces of the mesh will be used to cast shadows. The possible values for the ***shadowSide*** property are:

    * ***null***: The material will cast shadows from both sides of the mesh.
    * ***Three.FrontSide***: Only the front faces of the mesh will cast shadows.
    * ***Three.BackSide***: Only the back faces of the mesh will cast shadows.
    * ***Three.DoubleSide***: Both the front and back faces of the mesh will cast shadows.

    By default, the ***shadowSide*** property is set to ***null***, which means that shadows will be cast from both sides of the mesh.

* **stencilWrite**

    is a boolean value that determines whether the material writes to the stencil buffer when rendering. The ***MeshReflectorMaterial*** component from the drei library is a custom material that extends the built-in ***ShaderMaterial*** in Three.js, and it allows for creating a reflective surface by rendering the reflected objects in a separate render pass and using a stencil buffer to mask out the areas where the reflective surface should be visible.

    In the context of ***MeshReflectorMaterial***, the ***stencilWrite*** property controls whether the material writes to the stencil buffer during the reflection pass. When set to ***true***, the material will write to the stencil buffer and mark the pixels where the reflection should be visible. When set to ***false***, the material will not write to the stencil buffer, and the reflection will not be visible.

    Here's an example of how the ***stencilWrite*** property can be used with ***MeshReflectorMaterial***:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            color: 'white',
            stencilWrite: true,
            ...
        });
    ```

    In this example, the ***stencilWrite*** property is set to ***true***, which means that the material will write to the stencil buffer during the reflection pass. This will allow the reflection to be visible only in the areas where the stencil buffer is marked.

* **stencilFunc**

    is a WebGL rendering context property used to set the function used to compare stencil values to the reference value.

    The ***stencilFunc*** property takes three arguments:

    * ***stencilFunc(func: number, ref: number, mask: number)***: a method that sets the function used to compare stencil values to the reference value.

    The three arguments are:

    * ***func***: an enumeration specifying the comparison function. It can be one of the following values: Never, Less, Equal, LEqual, Greater, NotEqual, GEqual, and Always.
    * ***ref***: an integer reference value for the stencil test.
    * ***mask***: an integer bit mask that is ANDed with both the reference value and the stored stencil value when the test is performed.

    In summary, the ***stencilFunc*** property is used to determine if a fragment should be drawn based on the comparison of its stencil value with the reference value. It is commonly used for techniques like stencil shadows or masking.

* **stencilRef**

    is a value used in stencil testing to determine whether or not a pixel is drawn. Stencil testing is a technique used to limit the area of rendering by checking if the fragment's stencil value is the same as a reference value. This allows for a wide range of effects such as creating cutouts, highlights, and selective rendering of different parts of a scene. The stencil reference value determines what value the stencil buffer is compared to during the stencil test. If the comparison is true, the pixel is drawn. Otherwise, it is discarded. The stencil reference value is set using the stencil reference property.

* **stencilWriteMask**

    is used to set the bit mask for the stencil buffer. The stencil buffer is used to mark pixels that pass a stencil test, which can then be used for effects such as reflections or shadows. The ***stencilWriteMask*** property sets the write mask for the stencil buffer, which is a bit mask that determines which bits of the stencil buffer can be written to.

    For example, setting ***stencilWriteMask*** to ***0xff*** would allow all bits of the stencil buffer to be written to, while setting it to ***0x0f*** would only allow the first four bits to be written to. By default, ***stencilWriteMask*** is set to ***0xff***, which allows all bits to be written to.

* **stencilFuncMask**

    is used to set the bit mask used in the stencil test for the material.

    The stencil test is a rendering technique that determines whether a pixel should be drawn based on its stencil value. The stencil test can be configured using the ***stencilFunc*** property of the material. The ***stencilFuncMask*** property is used to set the bit mask that is ANDed with the stencil value and the reference value in the stencil test.

    The ***stencilFuncMask*** property is a number that represents the bit mask used in the stencil test. The default value is ***0xff***, which means that all bits are used in the stencil test. You can set this property to a different value to mask out certain bits in the stencil value. For example, if you set ***stencilFuncMask*** to ***0x0f***, the stencil test will only use the lower 4 bits of the stencil value.

* **stencilFail**

    is used to set the stencil operation to perform if the stencil test fails.

    In stencil testing, a comparison is made between the reference value (***stencilRef***) and the value in the stencil buffer for the corresponding pixel. If the comparison fails, the specified stencil operation is performed (***stencilFail***).

    The ***stencilFail*** property can take one of the following values:

    * ***THREE.KeepStencilOp***: Keeps the current value in the stencil buffer.
    * ***THREE.ZeroStencilOp***: Sets the stencil buffer value to zero.
    * ***THREE.ReplaceStencilOp***: Sets the stencil buffer value to the reference value (stencilRef).
    * ***THREE.IncrementStencilOp***: Increments the stencil buffer value.
    * ***THREE.IncrementWrapStencilOp***: Increments the stencil buffer value, but wraps to zero when the maximum value is reached.
    * ***THREE.DecrementStencilOp***: Decrements the stencil buffer value.
    * ***THREE.DecrementWrapStencilOp***: Decrements the stencil buffer value, but wraps to the maximum value when zero is reached.
    * ***THREE.InvertStencilOp***: Bitwise inverts the stencil buffer value.

    The default value of ***stencilFail*** is ***THREE.KeepStencilOp***.

* **stencilZFail**

    is used to set the stencil operation to perform when both the stencil test and the depth test fail.

    Stencil operation is a term used in computer graphics to describe a set of operations that can be performed on the stencil buffer to create complex shapes or to render objects with cutouts. The stencil buffer is a buffer in the graphics card that stores integer values for each pixel of the screen. The value of the stencil buffer for a pixel is determined by the result of a comparison between the current value of the stencil buffer and a reference value, using a comparison function.

    The ***stencilZFail*** property of ***MeshReflectorMaterial*** component can be set to any of the following constants:

    * ***THREE.KeepStencilOp*** - Keep the current value in the stencil buffer.
    * ***THREE.ZeroStencilOp*** - Set the stencil buffer value to zero.
    * ***THREE.ReplaceStencilOp*** - Replace the stencil buffer value with the reference value.
    * ***THREE.IncrementStencilOp*** - Increment the stencil buffer value.
    * ***THREE.DecrementStencilOp*** - Decrement the stencil buffer value.
    * ***THREE.IncrementWrapStencilOp*** - Increment the stencil buffer value, but wrap it to zero when it reaches the maximum value.
    * ***THREE.DecrementWrapStencilOp*** - Decrement the stencil buffer value, but wrap it to the maximum value when it reaches zero.

    The ***stencilZFail*** property is used in conjunction with the ***stencilFail*** and ***stencilZPass*** properties of ***MeshReflectorMaterial***.

* **stencilZPass**

    is a property that defines the operation to perform on the stencil buffer when the stencil test passes and the depth test passes.

    The stencil buffer is a data buffer that keeps track of which pixels have been drawn to during rendering. The stencil test compares a value in the stencil buffer to a reference value, and based on the result, decides whether to render a pixel or not.

    The ***stencilZPass*** property can have one of the following values:

    * ***THREE.KeepStencilOp***: keep the current value in the stencil buffer.
    * ***THREE.ZeroStencilOp***: set the stencil buffer value to 0.
    * ***THREE.ReplaceStencilOp***: set the stencil buffer value to the reference value.
    * ***THREE.IncrementStencilOp***: increment the stencil buffer value.
    * ***THREE.DecrementStencilOp***: decrement the stencil buffer value.
    * ***THREE.IncrementWrapStencilOp***: increment the stencil buffer value, wrapping to 0 when the maximum value is reached.
    * ***THREE.DecrementWrapStencilOp***: decrement the stencil buffer value, wrapping to the maximum value when 0 is reached.

* **wireframeLinewidth**

    is a numeric value that specifies the width of the wireframe lines in pixels.

    When the ***wireframe*** property is set to ***true***, the object using this material will be rendered in wireframe mode, meaning that only the edges of the object will be visible. The ***wireframeLinewidth*** property determines the width of these lines.

    For example, setting ***wireframeLinewidth*** to ***2*** will make the wireframe lines appear thicker and more visible. The default value is ***1***.

* **fog**

    is a boolean value that indicates whether or not the material should be affected by fog. If ***true***, the material will be affected by any fog in the scene, while if ***false***, the material will be fully opaque regardless of the fog settings.

    Fog is a visual effect that can be added to a 3D scene to simulate atmospheric conditions like haze or mist. It works by blending the color of the scene with a color representing the fog, based on the distance of the object from the camera. The farther away an object is from the camera, the more it is affected by the fog, creating a gradual transition from clear to hazy.

* **setValues**

    is used to set one or more properties of the material. It takes an object as its parameter, where each property of the object corresponds to a property of the material. The values of these properties are then set to the values specified in the object.

    For example, to set the ***color*** and ***metalness*** properties of a ***MeshReflectorMaterial***, you could use the ***setValues method*** like this:

    ```php
        const material = new MeshReflectorMaterial();
        material.setValues({ color: 'red', metalness: 0.5 });
    ```

    This would set the ***color*** property of the material to 'red' and the ***metalness*** property to 0.5.

* **isMaterial**

    is a boolean that returns ***true*** to indicate that the object is a material. This property is part of the ***three.js*** library which is a WebGL-based 3D graphics library.

    In ***three.js***, every material has an ***isMaterial*** property that is set to ***true*** by default. This property is useful for checking if an object is a material or not, especially when dealing with large and complex scenes that contain a lot of different objects.

    For example, you can use the ***isMaterial*** property to check if a particular object in the scene is a material, like this:

    ```js
        if (myObject.material.isMaterial) {
            // do something with the material
        }
    ```

    Or, you can use it to filter out all non-material objects in the scene, like this:

    ```js
        const materials = scene.children.filter(obj => obj.material.isMaterial);
    ```

* **needsUpdate**

    is a boolean value that specifies whether the material needs to be recompiled.

    When this property is set to ***true***, it means that the material's state has changed and needs to be recompiled before it can be used again. This is typically used when you change one or more of the material's properties.

    You can set this property to ***true*** to trigger a recompile of the material, or you can set it to ***false*** if you know that the material is up to date and does not need to be recompiled.

* **version**

    is used to indicate the version of the material.

    This property is specific to the ***drei*** library and is not part of the standard ***three.js*** material. It is a number that is incremented whenever the material's shader code or behavior is changed. This can be useful for debugging and ensuring that the correct version of the material is being used in a project.

    For example, if you were to log the value of the ***version*** property before and after making a change to the material, you would be able to see whether or not the change has been picked up by the system.

* **onBeforeCompile**

    allows you to define a function to be executed just before the material is compiled in the shader.

    This method is used to customize the material by providing additional instructions to the shader program. It takes a function as an argument, and this function will receive an instance of ***Shader*** class, which contains the vertex and fragment shader code. You can then modify the shader code as needed by adding or replacing code in the vertex and fragment shaders.

    For example, you can use ***onBeforeCompile*** to add custom uniforms, modify the vertex or fragment shaders, or add custom code to any part of the shader program.

    Here is an example of how to use ***onBeforeCompile*** to add a custom uniform to a ***MeshReflectorMaterial***:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const customMaterial = new MeshReflectorMaterial({
            onBeforeCompile: (shader) => {
                shader.uniforms.myCustomUniform = { value: 0.5 };

                // Modify the fragment shader to use the custom uniform
                shader.fragmentShader = shader.fragmentShader.replace(
                '#include <dithering_fragment>',
                `
                uniform float myCustomUniform;

                // Your custom code goes here

                #include <dithering_fragment>
                `
                );
            },
        });
    ```

    In this example, we add a custom uniform named ***myCustomUniform*** to the material and modify the fragment shader to use this uniform. Note that we use the ***replace*** method to add our custom code just before the ***dithering_fragment code***.

* **customProgramCacheKey**

    is used to customize the cache key used to store compiled shader programs for the material. By default, this is a combination of the material's type, UUID, and hash code of its parameters. However, in some cases, it may be useful to override this key to allow for more fine-grained control over shader caching, for example, to cache different shader programs for different values of certain material properties.

    To use ***customProgramCacheKey***, you can set it to a string that represents the custom key you want to use. When the material is compiled, this key will be used to store and retrieve the compiled shader program from the cache.

    Here is an example usage of ***customProgramCacheKey***:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        const material = new MeshReflectorMaterial({
            customProgramCacheKey: 'my-custom-key'
        });
    ```

    In this example, the material's compiled shader program will be stored in the cache using the key "my-custom-key", instead of the default cache key.

* **roughness**

    is a float value between 0 and 1 that determines the surface roughness of the material. A value of 0 means that the surface is perfectly smooth and reflects light in a mirror-like manner, while a value of 1 means that the surface is completely rough and scatters the reflected light in all directions. Values in between 0 and 1 control the degree of roughness of the surface.

    In physically-based rendering, roughness is often used as a complementary property to the material's specular/glossiness value to simulate the appearance of different surfaces, ranging from highly polished metals to rough and porous materials like concrete or fabric.

* **metalness**

    is a value between ***0*** and ***1*** that controls the amount of metalness of the material.

    A metalness value of ***0*** indicates that the material is completely dielectric, while a value of ***1*** indicates that the material is completely metallic. Materials with a metalness value of ***0.5*** are a blend of both dielectric and metallic properties.

    This property is typically used in conjunction with the ***roughness*** property to control the appearance of the material.

* **map**

    is a texture map to be used for the surface of the material. It is used to define the surface color of the material by modulating the reflectivity and roughness values. The texture is a 2D image that is typically loaded from an external file or generated dynamically in code.

    The ***map*** property can be set to a ***Texture*** object, which is an instance of the ***THREE.Texture*** class in the ***three.js*** library. This class provides many options for controlling the behavior of the texture, such as mapping modes, wrapping modes, and filtering modes.

* **lightMap**

    is a texture map that can be used to modulate the lightness or darkness of different areas of the material. This is accomplished by multiplying the texture color with the base color of the material. The result is that the areas of the material that correspond to lighter areas of the texture will be lighter, while the areas that correspond to darker areas of the texture will be darker.

    The ***lightMap*** texture can be set with a ***Texture*** object and is used in conjunction with the ***lightMapIntensity*** property to control the strength of the effect.

* **lightMapIntensity**

    is used to set the intensity of the light map. It is a value between ***0*** and ***1*** which controls how much the light map affects the material's appearance. A value of ***0*** will completely remove the effect of the light map, while a value of ***1*** will apply the full effect of the light map.

    Light maps are a type of texture used to simulate global illumination in real-time rendering. They are precomputed textures that store lighting information for a scene and can be used to enhance the appearance of materials. The ***lightMap*** property is used to specify the light map texture to use for the material, and the ***lightMapIntensity*** property controls how much the light map affects the material's appearance.

* **aoMap**

    is a texture representing the ambient occlusion shading of the material. Ambient occlusion is a shading method that calculates how much each point in a scene is exposed to ambient lighting, which is light that has been scattered and reflected multiple times before reaching the point. The ***aoMap*** texture is multiplied with the base color of the material to create the final shading. The ***aoMap*** property is a ***Texture*** object and can be set to any valid texture.

* **aoMapIntensity**

    it specifies the intensity of the ambient occlusion map.

    The ambient occlusion map is a texture that is used to add shadowing to the material, based on the proximity of surfaces to each other. The ***aoMapIntensity*** property determines how much the ambient occlusion affects the material's overall appearance, with a value of 1 being the maximum amount of influence.

    A higher value for ***aoMapIntensity*** will result in a stronger shadow effect, while a lower value will make the shadows more subtle. The default value for ***aoMapIntensity*** is ***1***.

* **emissive**

    is a color representing the emissive color of the material. The emissive color is the color that the material appears to emit as if it were a light source.

    In three.js, the emissive color is combined with the scene's lighting to produce the final color of the material. The default value of the ***emissive*** property is a black color, which means that the material does not emit any light.

    Here is an example of setting the emissive color of a ***MeshReflectorMaterial***:

    ```jsx
        import { MeshReflectorMaterial } from 'drei'

        // Create a new MeshReflectorMaterial with a red emissive color
        const material = new MeshReflectorMaterial({
            color: 0xff0000, // set the base color of the material to red
            emissive: 0xff0000, // set the emissive color of the material to red
        })
    ```

* **emissiveIntensity**

    is a numeric value that controls the strength of the emissive map. Emissive maps are textures that add extra brightness to the material, as if it was emitting light. The emissive intensity value scales the brightness of the emissive color, with a default value of ***1.0***. A value of ***0*** will make the material not emit light at all. A value greater than ***1*** will make the material appear even brighter.

* **emissiveMap**

    is a texture map that specifies the emissive color of the material.

    The ***emissive*** color is the color of the material that appears to be self-illuminated, regardless of any light sources in the scene. This texture map is used to define the intensity and color of the emissive effect, which can be useful for creating materials that appear to glow in the dark or emit light.

    If the ***emissiveMap*** property is set to a texture, it will be multiplied by the ***emissive*** color and added to the final color of the material during rendering. The intensity of the emissive effect can be controlled with the ***emissiveIntensity*** property.

* **bumpMap**

    is a texture that provides height information to simulate bumpiness or roughness on the surface of the material. The texture should be in grayscale and lighter shades represent higher elevations. The texture is used to perturb the surface normals and create the appearance of bumps and roughness in lighting calculations.

    When the ***bumpMap*** property is set, the ***MeshReflectorMaterial*** will use the texture to calculate the surface normal perturbation in the shader, which affects how the material reacts to light. The ***bumpScale*** property can be used to adjust the strength of the effect.

* **bumpScale**

    is used to set the amount of bump mapping applied to the material. Bump mapping is a technique used in computer graphics to simulate bumps and wrinkles on the surface of an object.

    The ***bumpScale*** property is a scalar value that multiplies the bump map's RGB color values. A higher value will make the bumps appear more pronounced, while a lower value will make them appear more subtle. The default value of ***bumpScale*** is ***1***.

* **normalMap**

    is used to specify the normal map texture of the material.

    A normal map is an image texture that stores surface normal data in its RGB channels. It is used to give the impression of a surface with more detail than what is actually modeled in the geometry. The normal map texture is used to perturb the surface normals of a model, creating the illusion of bumps, scratches, and other surface details that would be too complex or too resource-intensive to model with geometry.

    Here is an example of using the ***normalMap*** property in a ***MeshReflectorMaterial*** component:

    ```jsx
        import { MeshReflectorMaterial } from 'drei'
        import normalMapTexture from './textures/normalMap.png'

        const material = new MeshReflectorMaterial({
            normalMap: normalMapTexture
        })
    ```

* **normalMapType**

    it specifies how the normal map texture should be interpreted.

    It can be set to one of three values:

    * ***THREE.TangentSpaceNormalMap***: This is the default value, and indicates that the normal map is in tangent space. This means that the texture uses the tangent, bitangent, and normal vectors to specify the orientation of the surface normal at each texel.
    * ***THREE.ObjectSpaceNormalMap***: This value indicates that the normal map is in object space, meaning that the texture specifies the orientation of the surface normal relative to the surface itself, rather than relative to the tangent, bitangent, and normal vectors.
    * ***THREE.RGBADepthPacking***: This value is used when the normal map is stored in an RGBA texture, with the red, green, and blue channels storing the XYZ components of the normal vector, and the alpha channel storing a depth value. This is an alternative to using a separate texture for the depth values.

* **normalScale**

    is used to specify how to scale the normals of a reflected object in a WebXR application.

    The normal scale property controls the appearance of the reflections on the surface of an object that is using the MeshReflectorMaterial. The normals of the reflected object are used to calculate the angle at which light should be reflected, and the normal scale property allows you to adjust this calculation. By changing the normal scale property, you can control the intensity and quality of the reflections on the surface of the object.

    For example, a value of 1 will result in reflections that match the normals of the reflected object exactly, while a value of 0 will result in no reflections. The normal scale property can also be negative, which will result in inverted reflections.

* **displacementMap**

    is a texture map used to displace the vertices of the mesh in the direction of their normals. The displacement amount is controlled by the values of the texture map.

    When the displacement map is applied, the geometry of the mesh is modified, creating the appearance of surface details that are not actually present in the original mesh. The ***displacementMap*** property is a Texture object that can be loaded from an image or created dynamically. The texture can be used to create a range of effects, from subtle surface variations to extreme deformations.

    The ***displacementMap*** property is typically used in conjunction with the ***displacementScale*** property, which controls the intensity of the displacement effect. The ***displacementBias*** property can be used to adjust the center point of the displacement effect.

* **displacementScale**

    is a numeric property that defines the scaling factor of the displacement map. The displacement map is a texture that modifies the position of vertices in the mesh to give the appearance of 3D depth. The ***displacementScale*** property controls the amount of displacement, with larger values resulting in more dramatic depth effects.

* **displacementBias**

    is used to specify the amount of displacement to apply to the vertices of the material's mesh. It is a number that determines how much to move the vertices along their normals before rendering. A positive value will move the vertices outwards, while a negative value will move them inwards.

    This property is used in conjunction with the ***displacementMap*** property, which is a texture that specifies how much displacement to apply to each pixel on the material's surface.

* **roughnessMap**

    is a texture map used to specify the roughness of the material. The roughness map is a grayscale image where lighter colors represent rougher surfaces and darker colors represent smoother surfaces. This property is used in combination with the ***roughness*** property, which specifies the overall roughness of the material.

    When both ***roughnessMap*** and ***roughness*** properties are used, the ***roughness*** property acts as a multiplier for the values in the ***roughnessMap***. This means that the final roughness of the material is determined by multiplying the values in the ***roughnessMap*** by the value of the ***roughness*** property.

* **metalnessMap**

    is a texture map that defines the metalness of the material for each pixel. The map uses grayscale values where black corresponds to non-metallic and white corresponds to metallic. The texture is usually a grayscale image, where brighter areas correspond to more metallic surfaces.

    When a ***metalnessMap*** is provided, it overrides the ***metalness*** property of the material. If both the ***metalnessMap*** and ***metalness*** properties are set, the ***metalnessMap*** takes precedence.

    Here's an example of how to use ***metalnessMap*** in a ***MeshReflectorMaterial***:

    ```jsx
        import { MeshReflectorMaterial } from 'drei'
        import metalnessMapTexture from './metalnessMapTexture.jpg'

        const material = new MeshReflectorMaterial({
            metalnessMap: metalnessMapTexture,
            // Other material properties...
        })
    ```

    In this example, the ***metalnessMapTexture*** is a pre-loaded texture that defines the metalness of the material.

* **alphaMap**

    is a texture map that controls the alpha channel (transparency) of the material. It is used to create cutout effects, such as for objects with holes or for foliage with irregular shapes.

    The ***alphaMap*** is a texture that should be assigned to the property as a ***THREE.Texture*** object. The texture can be created using an image or a data URL, or loaded from a file using a texture loader. The alpha channel of the texture determines the transparency of the material, with black being completely transparent and white being completely opaque. The ***alphaMap*** property is multiplied with the alpha channel of the material's ***map*** property, if it exists.

* **envMap**

    is used to specify the environment map to be used for reflections on the material. An environment map is a texture that provides an image of the surrounding environment, and is typically used for simulating reflections and refractions.

    When ***envMap*** is set to a texture, the material will use it to generate reflections based on the properties specified in other material settings. For example, the ***reflectivity*** property can be used to adjust the strength of the reflections.

    Here is an example of how to set the ***envMap*** property to a texture:

    ```jsx
        import { MeshReflectorMaterial } from 'drei'
        import { CubeTextureLoader } from 'three'

        // Create a CubeTextureLoader instance
        const loader = new CubeTextureLoader();

        // Load an environment map texture
        const envMap = loader.load([
            'path/to/px.png',
            'path/to/nx.png',
            'path/to/py.png',
            'path/to/ny.png',
            'path/to/pz.png',
            'path/to/nz.png',
        ]);

        // Create a MeshReflectorMaterial with the environment map
        const material = new MeshReflectorMaterial({ envMap: envMap });
    ```

    In this example, a ***CubeTextureLoader*** is used to load an environment map texture with six faces, and the resulting texture is set as the ***envMap*** property of the ***MeshReflectorMaterial***.

* **envMapIntensity**

    is used to control the intensity of the environment map that is applied to the material.

    An environment map is a texture that is used to simulate the reflection of the surrounding environment on a material. The ***envMap*** property of the ***MeshReflectorMaterial*** component is used to specify the environment map texture.

    The ***envMapIntensity*** property is a value between 0 and 1, where 0 means the environment map has no effect on the material, and 1 means the environment map is fully applied to the material.

    By adjusting the ***envMapIntensity*** property, you can control the strength of the reflection and achieve the desired level of realism for your scene.

* **wireframeLinecap**

    It sets the style of the ends of wireframe lines in a material.

    The ***wireframeLinecap*** property accepts three values: ***"butt", "round", and "square"***. ***"butt"*** is the default value, and it creates a flat end to each wireframe line. ***"round"*** creates a rounded end, while ***"square"*** creates a square end.

    This property is typically used to control the style of wireframe meshes, which are a visual representation of an object's wireframe, made up of lines rather than solid faces.

* **wireframeLinejoin**

    it determines how the corners of the wireframe geometry are joined together.

    The value of ***wireframeLinejoin*** can be set to one of the following string values:

    * ***"round"***: the corners of the wireframe geometry are rounded.
    * ***"bevel"***: the corners of the wireframe geometry are beveled.
    * ***"miter"***: the corners of the wireframe geometry are joined with a sharp miter.

    By default, ***wireframeLinejoin*** is set to ***"round"***.

* **flatShading**

    is a boolean value that specifies whether the shading of the material should be flat or smooth.

    If ***flatShading*** is set to ***true***, the material will be shaded using flat shading, where the color of each face is constant and does not vary across the face. This can create a faceted appearance for the object.

    If ***flatShading*** is set to ***false***, the material will be shaded using smooth shading, where the color of each point on the surface is interpolated based on the normals of adjacent faces. This creates a smoother appearance for the object.

    By default, ***flatShading*** is set to ***false***.

* **isMeshStandardMaterial**

    is a boolean property that is set to ***true*** to indicate that the material is an instance of the ***MeshStandardMaterial*** class in the three.js library. This property is used internally by the three.js renderer to identify and handle instances of ***MeshStandardMaterial***.

* **mixBlur**

    is a custom shader material for three.js that allows a mesh to reflect its surroundings.

    The ***mixBlur*** property specifies the amount of blurring to be applied to the reflected image. It is a float value between 0 and 1, with 0 indicating no blurring and 1 indicating maximum blurring.

    By adjusting this property, you can control the degree of sharpness of the reflection. A lower value will produce a sharper reflection, while a higher value will produce a more blurred reflection.

* **mixStrength**

    it specifies the strength of the reflection mixing between the reflected scene and the surface color of the material. It is a value between 0 and 1, where 0 means no reflection mixing and 1 means full reflection mixing.

* **minDepthThreshold**

    is used to set the minimum depth threshold for the reflection.

    This property is used to control how far back the reflections should be visible. It is a value between 0 and 1, where 0 means that the reflections will be visible from the camera position, and 1 means that the reflections will only be visible from the reflection plane.

    By default, this value is set to 0, which means that the reflections will be visible from the camera position. Setting it to a higher value will limit the visibility of the reflections to a smaller range, resulting in a more realistic reflection effect.

* **maxDepthThreshold**

    is used to control the maximum depth at which the reflection can be seen on the surface of the material. It is a float value that represents the maximum depth in world units. Objects beyond this depth will not be visible in the reflection. This property is useful for controlling the level of detail in the reflection and optimizing performance.

* **depthScale**

    is used to scale the depth of the reflections. It is a floating-point value that defaults to 1. Increasing this value will make the reflections appear deeper, while decreasing it will make them appear shallower.

* **depthToBlurRatioBias**

    is used for creating a blur effect on the reflected objects. It is a value that determines the ratio between the depth map and the blur strength.

    The depth map is a texture that stores the distance of each pixel from the camera. The blur strength determines how much the reflected objects are blurred. By adjusting the ***depthToBlurRatioBias*** value, you can control how much the blur effect is influenced by the depth map.

    A higher value will make the blur effect more dependent on the depth map, while a lower value will make the blur effect less dependent on the depth map.

* **mirror**

    is a boolean that*** determines whether or not the material should act as a mirror, reflecting the environment or other objects in the scene. If the ***mirror*** property is set to ***true***, the material will reflect the surrounding environment. If it is set to ***false***, the material will not reflect anything.

    When ***mirror*** is set to ***true***, the material will use the ***envMap*** property as a texture to generate reflections. The ***envMap*** is typically set to a cube map texture that represents the surrounding environment. The ***mirror*** property can be used to create reflective surfaces such as mirrors or shiny objects in the scene.

* **distortion**

    is a Boolean that specifies whether or not to enable the distortion effect on the reflected surface. When set to ***true***, the reflection will appear to have a rippled or wavy effect, similar to the way light is distorted when reflected off a body of water. This effect is achieved by applying a distortion texture to the reflection. The texture is defined by the ***distortionMap*** property, which can be set to an instance of the ***Texture*** class. The intensity of the distortion effect can be adjusted with the ***distortionScale*** property.

* **mixContrast**

    it controls the contrast of the mixed reflection and refraction of the material. It is a float value between 0 and 1, with a default value of 0.2. A value of 0 produces no contrast, while a value of 1 produces high contrast between the reflection and refraction.

* **distortionMap**

    is used to specify a texture that will be used to apply distortion to the reflected image. This can be used to create a variety of effects, such as creating a rippling water effect or a distorted mirror effect. The texture should be a grayscale image, where the white areas represent areas of the texture that should cause the most distortion, and the black areas represent areas that should cause no distortion. The intensity of the distortion can be controlled using the "distortion" property.

* **reflectorOffset**

    resents the amount of offset in the horizontal and vertical direction of the texture.

    For example, if you set ***reflectorOffset={[1,1]}***, it will shift the texture one unit to the right and one unit up. Similarly, if you set ***reflectorOffset={[-1,0]}***, it will shift the texture one unit to the left.

    Here's an example of how you can use it:

    ```js
        import { MeshReflectorMaterial } from 'drei';

        function MyComponent() {
            return (
                <mesh>
                <sphereBufferGeometry />
                <MeshReflectorMaterial reflectorOffset={[1, 1]} />
                </mesh>
            );
        }
    ```
