<style>

:root {  
    --grey-1: #303030;
    --grey-2: #505050;
    --grey-3: #707070;
    --grey-4: #909090;
    --grey-5: #b0b0b0;
    --red-1: #500000;
    --red-2: #900000;
    --red-3: #d00000;
    --green-1: #005000;
    --green-2: #009000;
    --green-3: #00d000;
    --blue-1: #000050;
    --blue-2: #000090;
    --blue-3: #0000d0;
    --blue-4: #0000f0;
}

/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
    .main {
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr 5fr 3fr 3fr;
    }
    #bar{

    }
    #game-bar{

    }
    #events{

    }
    #properties{

    }
    #game{

    }
    #assets{

    }
    #scene{

    }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {

}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {

}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {

}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {

}


main{
    color: #d9d9d9;
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    
    width: 100%;
    height: 100%;
    background-color: var(--grey-3);
    display: grid;
    grid-template-columns: 2fr 2fr 4fr;
    grid-template-rows: 1fr 9fr 5fr;
}

section{
    border-style: solid;
    border-width: 4px 4px 4px 4px;
    border-color: var(--grey-1);
    border-radius: 0px;
    background-color: var(--grey-2);
    margin: 6px;
    min-width: 0;
    min-height: 0;
    overflow-x: hidden;
    overflow-y: auto;
    transition: all 0.2s linear
}
section:hover{
    margin: 2px;
    padding: 4px;
}
h1{
    text-align: center;
}
h2{
    text-decoration:underline;
}
h3{
    margin-block: 5px;
}
input{
    background-color: var(--grey-5);
    border-radius: 5px;
    border: 3px solid var(--grey-2);
}

select{
    background-color: var(--grey-5);
    border-radius: 5px;
    border-style: solid;
    border-width: 3px;
    border-color: var(--grey-2);
}
.selection_window{
    position: fixed;
    width: 50vw;
    height: 70vh;
    left: 25vw;
    top: 15vh;
    display:flex;
    flex-direction: column;
    z-index: 1;

    background-color: #707070;
    border-style: solid;
    border-radius: 10px;
    border-width: 5px;

}
.selection_window_header{
    display: flex;
    justify-content: space-between;
    background-color: var(--grey-2);
}

.selection{
    color: #ffffff;
    background-color: var(--grey-2);
    margin: 4px;
    padding: 5px;
    border-radius: 7px;
    border-style: solid;
    border-color: black;
    border-width: 2px;
    
}

.add_button{
    color: #ffffff;
    background-color: var(--green-3);
    margin: 4px;
    padding: 5px;
    border-radius: 7px;
    border-style: outset;
    border-color: var(--green-3);
    border-width: 10px;
    box-sizing: border-box;
}
.add_button:hover{
    background-color: var(--green-2);
    border-color: var(--green-2);
}
.add_container{
    display: flex;
    justify-content: center;
    
    border-width: 0px 0px 10px 0px;
    border-style: outset;
    border-color: var(--grey-3);
}
#bar{
    grid-column-start: 1;
    grid-column-end:3;

    background-color: var(--grey-1);
}
#bar a{
    color: white;
}
#game-bar{
    display: flex;
    justify-content: space-evenly;
}
.play_button{
    background-color: var(--grey-1);
    color: white;
    height: 100%;
}
.play_button:hover{
    background-color: var(--grey-2);
}
#variables{
    display: none;
}
.variable_row{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0px 10px 0px 10px;
    margin: 0px 5px 0px 5px;
    overflow-x: auto;
    min-width: 0;
}
.variable_row:nth-child(odd){
    background-color: var(--grey-3);
}
.variable_row:last-child{
    margin-bottom: 5px;
}
#events{
    display: flex;
    flex-direction: column;
}
.list_header{
    display: flex;
    justify-content: right;
}
.remove_item_button{
    background-color: var(--red-3);
}
.remove_item_button:hover{
    background-color: var(--red-2);
}
.rename_item_button{
    background-color: var(--blue-4);
}
.rename_item_button:hover{
    background-color: var(--blue-3);
}
.event_button{
    width: 100%;
    border-style: outset;
    box-sizing: border-box;
    border-width: 10px;
    background-color: var(--grey-3);
    border-color: var(--grey-2);
    min-width: 0;
}
.event_button_expanded{
    border-width: 10px 10px 0px 10px;
    background-color: var(--grey-4);
    border-color: var(--grey-3);
    min-width: 0;
    overflow: hidden;
    
}
.event_button_expanded:hover{
    background-color: var(--grey-5);
}
.event_button:hover{
    background-color: var(--grey-4);
    border-color: var(--grey-3);
}
.event_priority{
    display: flex;
    flex-direction: column;
}
.event_priority_button{
    flex-grow: 1;
    background-color: var(--green-3);
}
.event_priority_button:hover{
    background-color: var(--green-2);
}

.item_list{
    flex: 1;
    overflow-y: auto;
    overflow-x: hidden;
    min-height: 0;
    transition: all 0.2s ease-out;
}
.event_info{
    background-color: var(--grey-4);
    border-style: outset;
    border-width: 0px 10px 10px 10px;
    border-color: var(--grey-3);
    
}
.property_updates_header{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    overflow: hidden;
    background-color: var(--grey-4);
    border-width: 0px;
    border-radius: 10px;
    transition: all 0.2s linear;
    justify-self: center;
    width: 80%;
}
.property_updates_header:hover{
    background-color: var(--grey-5);
}
.property_updates_header:last-child{
    margin-bottom: 5px;
}
.devider_line{
    background-color: black;
    height: 2px;
    margin: 10px;
}
.devider_line:first-child{
    height: 0px;
    margin: 0px;
}

#properties{
    display: flex;
    flex-direction: column;
}
input{
    min-width: 40px;
}
#game{
    position: relative;
    overflow: hidden;
    
    user-select: none;
}
#game:hover{
    padding: 0px;
    margin: 6px
}
#viewport{
    width: 100%;
    height: 100%;
}
#tile_map_editor{
    display: flex;
    justify-content: center;
    background-color: rgba(0, 100, 100, 0.35);
    position: absolute;
    bottom: 0px;
    width: 100%;
    padding-block: 10px;
    z-index: 1;
}
#tile_map_editor div{
    width: 70px;
    margin: 2px;
}
.tile_editor_button{
    width: 70px;
    height: 70px;
    border-radius: 50%;
    margin: 2px;
    background-color: #f0a000;
    transition: all 0.2s linear;
}
.tile_editor_button:hover{
    background-color: #ffd090;
}
#active_tile_button{
    background-color: var(--green-3);
}
#active_tile_button:hover{
    background-color: var(--green-2);
}
.tile_editor_image{
    height: 50px;
    padding-top: 5px;
}
#calculator{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}
#calc_area{

}
#calc_keypad{

}
.sprite{
    position: absolute;
    transform: translate(-50%, -50%);

    transition: none;
}
.sprite img{
    transform-origin: center;
    pointer-events: none;
    user-select: none;
    -webkit-user-drag: none;
}
.tile{
    position: absolute;
}
.tile img{
    width: 100%;
    height: 100%;
}
.hitbox{
    position: absolute;
    background-color: #9090ff90;
    transform: translate(-50%, -50%);
    z-index: 1;
    border-width: 1px;
    border-style: solid;
    box-sizing: border-box;
    border-color: black;
}
.hitbox_hidden{
    position: absolute;
    transform: translate(-50%, -50%);
    z-index: 1;
}
#assets{
    grid-column-start: 1;
    grid-column-end: 3;

    display: flex;
    flex-direction: column;
}
.item_grid{
    display: flex;
    flex-wrap: wrap;
    overflow-y: auto;
    min-height: 0;
    flex: 1;
    
}
.asset{
    margin: 10px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background-color: var(--grey-3);
    border-style: none;
    padding: 5px;
    border-radius: 10px;
    gap: 5px;
    transition: all 0.2s linear;
}
.assets_image_wrapper{
    margin-block: 10%;
    max-height: 80%;
    width: 90%;
    overflow-y: auto;
    align-self: center;
}
.assets_image_wrapper img{
    width: 100%;
}
.asset img{
    width: 50px;
}
.remove_asset_button{
    position: absolute;
    top: 5px;
    right: 0px;
    border-radius: 50%;
    width: 30px;
    height: 30px;
    background-color: var(--red-3);
    color: white;
    box-shadow: 0px 5px 5px black;
}
.remove_asset_button:hover{
    background-color: var(--red-2);
}
.sprite_box{
    position: relative;
}
.sprite_button{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    background-color: var(--grey-3);
    border-style: none;
    border-radius: 10px;
    padding: 5px;
    gap: 5px;
    margin: 10px;
    transition: all 0.2s linear;
    
}
.sprite_button img{
    width: 50px;
}
.sprite_button:hover{
    background-color: var(--grey-4);
}
.tabs_bar{
    background-color: var(--grey-2);
    display: flex;
    justify-content: left;
    border-style: solid;
    border-width: 0px 0px 2px 0px;
    overflow-x: auto;
}
.tab{
    background-color: var(--grey-3);
    padding-inline: 10px;
    padding-block: 5px;
    margin-top: 10px;
    margin-inline: 5px;
    border-radius: 10px 10px 0 0;
    border-width: 0;
    transition: all 0.2s linear;
}
.tab:hover{
    background-color: var(--grey-4);
}
.active_tab{
    background-color: var(--grey-5);
}
.active_tab:hover{
    background-color: var(--grey-5);
}
.new_tab_button{
    background-color: var(--grey-3);
    padding-inline: 10px;
    padding-block: 5px;
    margin-top: 10px;
    margin-inline: 5px;
    border-radius: 10px;
    border-width: 0;
    transition: all 0.2s linear;
}
.new_tab_button:hover{
    background-color: var(--grey-4);
}

#scene{
    display: flex;
    flex-direction: column;
}

</style>

<svelte:window on:keydown={onKeyDown} on:keyup={onKeyUp} on:mousemove={mouseMove} on:mouseup={mouseUp}/>
<script>

    const DEFAULT_PROJECT = {
        name: "unnamed game",
        version: 1,
        global_variables: {},
        assets: {images: {
            mario: "https://www.nicepng.com/png/full/164-1648710_8-bit-mario-by-pokedude911-super-mario-bros.png",
            block: "https://art.pixilart.com/82f97e33624310f.png",
        }},
        scenes: {
            scene_1: {
                collision_groups: ["Default"],
                local_variables: {},
                sprites: {},
                events: [
                    {
                        name: "on scene load",
                        type: "scene load",
                        settings: {},
                        property_updates: {},
                        scene_setting_updates: {
                            backgroundColor: {value: "#ffffff", operation: "set"},
                            cameraX: {value: 0, operation: "set"},
                            cameraY: {value: 0, operation: "set"},
                            cameraZoom: {value: 1, operation: "set"},
                            cameraFollowSprite: {value: null, operation: "set"},
                            camFollowX: {value: true, operation: "set"},
                            camFollowY: {value: true, operation: "set"}
                        },
                        scene_change: null
                    },
                ]
            }
        }
    }
    import { defaultProjects } from '$lib/defaults'
    import { goto } from '$app/navigation';   
    import { base } from '$app/paths';
    import { page } from '$app/state';
    import { browser } from '$app/environment';
    import { onMount, onDestroy } from 'svelte';

    const projectId = $derived(page.params.id);

    let project = $state(structuredClone(DEFAULT_PROJECT));

    function loadProject() {
        if (!browser) return;

        const raw =
            localStorage.getItem(`project_${projectId}`);

        if (raw) {
            if (raw.length > 2){
                project = JSON.parse(raw);
            }   
        } 
        else if (defaultProjects[projectId]) {
            project = defaultProjects[projectId]
        } 
        else {
            goto(base + "/create/")
        }
    }

    function saveProject() {
        
        if (!browser) return;
        
        localStorage.setItem(
            `project_${projectId}`,
            JSON.stringify(project)
        );
    }

    function migrate_project(){
        // migrate project between versions
    }

    let interval;

    onMount(() => {
        loadProject();

        interval = setInterval(
            saveProject,
            20000
        );
    });

    onDestroy(() => {
        clearInterval(interval);
    });

    let game_window_width = $state()
    let game_window_height = $state()
    let game_section

    let editor_camX = $state(0)
    let editor_camY = $state(0)
    let editorZoom = $state(1)
    let dragLastX = 0
    let dragLastY = 0
    let dragging = false

    let selected_sprite = $state("")
    let tiling = $state(false)
    let erasing = $state(false)
    let tile_image = $state("")

    function mouseDown(e){
        if (running)
            return
        dragging = true
        dragLastX = e.clientX
        dragLastY = e.clientY
    }
    function mouseUp(e){
        dragging = false
    }
    function mouseMove(e){
        if (running || !dragging)
            return
        if (selected_sprite !== "" && get_sprite_type(selected_sprite) === "tile_map" && (tiling || erasing)){
            const rect = game_section.getBoundingClientRect()
            const x = Math.floor((e.clientX - rect.left + editor_camX - project.scenes[current_scene].events[0].property_updates[selected_sprite].offsetX.value - game_window_width / 2) / project.scenes[current_scene].events[0].property_updates[selected_sprite].tileWidth.value)
            const y = Math.floor((e.clientY - rect.top + editor_camY - project.scenes[current_scene].events[0].property_updates[selected_sprite].offsetY.value - game_window_height / 2) / project.scenes[current_scene].events[0].property_updates[selected_sprite].tileHeight.value)
            let key = JSON.stringify({'x': x, 'y': y})
            if (tiling){
                project.scenes[current_scene].sprites[selected_sprite].tiles[key] = tile_image
            }
            else {
                delete project.scenes[current_scene].sprites[selected_sprite].tiles[key]
            }
            return
        }
        editor_camX -= e.clientX - dragLastX
        editor_camY -= e.clientY - dragLastY

        dragLastX = e.clientX
        dragLastY = e.clientY
    }
	
    const PROPERTY_INFO = {
        sprite: {
            posX: {
                baseValue: 0,
                type: "float",
                min: -1000000,
                max: 1000000,
            },
            posY: {
                baseValue: 0,
                type: "float",
                min: -1000000,
                max: 1000000,
            },
            image: {
                baseValue: "",
                type: "select",
                getOptions: ()=>{return {None: "", ...project.assets.images}}
            },
            Zindex: {
                baseValue: 0,
                type: "float",
                min: -1000,
                max: 1000,
            },
            scaleX: {
                baseValue: 1,
                type: "float",
                min: -1000,
                max: 1000,
            },
            scaleY: {
                baseValue: 1,
                type: "float",
                min: -1000,
                max: 1000,
            },
            rotation: {
                baseValue: 0,
                type: "float",
                min: -3600000,
                max: 3600000,
            },
            velX: {
                baseValue: 0,
                type: "float",
                min: -100000,
                max: 100000,
            },
            velY: {
                baseValue: 0,
                type: "float",
                min: -100000,
                max: 100000,
            },
            gravity: {
                baseValue: 0,
                type: "float",
                min: -1000,
                max: 1000,
            },
            airResistance: {
                baseValue: 0,
                type: "float",
                min: 0,
                max: 1,
            },
            collidable: {
                baseValue: false,
                type: "bool",
            },
            collisionGroups: {
                baseValue: ["Default"],
                type: "select_multiple",
                getOptions: ()=>{
                    let used_groups = project.scenes[current_scene].events[selected_event].property_updates[expanded_sprite].collisionGroups.value
                    return project.scenes[current_scene].collision_groups.filter(x => !used_groups.includes(x))
                }
            },
            mass: {
                baseValue: 1,
                type: "float",
                min: 0.001,
                max: 1000000,
            },
            infiniteMass: {
                baseValue: false,
                type: "bool",
            },
            bounce: {
                baseValue: 0,
                type: "float",
                min: 0,
                max: 100,
            },
            hitboxWidth: {
                baseValue: 50,
                type: "float",
                min: 1,
                max: 100000,
            },
            hitboxHeight: {
                baseValue: 50,
                type: "float",
                min: 1,
                max: 100000,
            },
            hitboxOffsetX: {
                baseValue: 0,
                type: "float",
                min: -1000000,
                max: 1000000,
            },
            hitboxOffsetY: {
                baseValue: 0,
                type: "float",
                min: -1000000,
                max: 1000000,
            },
        },
        tile_map: {
            offsetX: {
                baseValue: 0,
                type: "float",
                min: -1000000,
                max: 1000000,
            },
            offsetY: {
                baseValue: 0,
                type: "float",
                min: -1000000,
                max: 1000000,
            },
            tileWidth: {
                baseValue: 100,
                type: "float",
                min: -10000,
                max: 10000,
            },
            tileHeight: {
                baseValue: 100,
                type: "float",
                min: -10000,
                max: 10000,
            },
            collidable: {
                baseValue: true,
                type: "bool"
            },
            collisionGroups: {
                baseValue: ["Default"],
                type: "select_multiple",
                getOptions: ()=>{
                    let used_groups = project.scenes[current_scene].events[selected_event].property_updates[expanded_sprite].collisionGroups.value
                    return project.scenes[current_scene].collision_groups.filter(x => !used_groups.includes(x))
                }
            },
            bounce: {
                baseValue: 0,
                type: "float",
                min: 0,
                max: 100,
            },
        }
    }

    const SCENE_SETTING_INFO = {
        backgroundColor: {
            baseValue: "#ffffff",
            type: "color"
        },
        cameraX: {
            baseValue: 0,
            type: "float",
            min: -1000000,
            max: 1000000,
        },
        cameraY: {
            baseValue: 0,
            type: "float",
            min: -1000000,
            max: 1000000,
        },
        cameraZoom: {
            baseValue: 1,
            type: "float",
            min: 0.001,
            max: 100,
        },
        cameraFollowSprite: {
            baseValue: null,
            type: "select",
            getOptions: ()=>{
                let obj = get_sprite_object()
                return {None: null, ...obj}
            }
        },
        camFollowX : {
            baseValue: true,
            type: "bool"
        },
        camFollowY: {
            baseValue: true,
            type: "bool"
        }
    }
    
    let sprite_properties = $state({})
    let scene_settings = $state({})
    //let global_variables = $state({})
    //let local_variables = $state({})

    let current_scene = $state("scene_1")

    function add_scene(){
        let new_scene_name = "scene"
        let i = 1
        while (Object.hasOwn(project.scenes, new_scene_name)){
            new_scene_name = "scene_"+i
            i++
        }
        project.scenes[new_scene_name] = {
            collision_groups: ["Default"],
            local_variables: {},
            sprites: {},
            events: [
                {
                    name: "on scene load",
                    type: "scene load",
                    access_sprites: [],
                    other: {},
                    property_updates: {},
                    variable_updates: {},
                    scene_setting_updates: {},
                    scene_change: null
                }
            ]
        }
        for (let setting in SCENE_SETTING_INFO){
            project.scenes[new_scene_name].events[0].scene_setting_updates[setting] = {operation: "set", value: SCENE_SETTING_INFO[setting].baseValue}
        }
        switch_scene(new_scene_name)
    }
    /*
    let project = $state({
        global_variables: {},
        assets: {images: {
            mario: "https://www.nicepng.com/png/full/164-1648710_8-bit-mario-by-pokedude911-super-mario-bros.png",
            block: "https://art.pixilart.com/82f97e33624310f.png",
        }},
        scenes: {
            scene_1: {
                collision_groups: new Set(["Default"]),
                local_variables: {},
                sprites: {},
                events: [
                    {
                        name: "on scene load",
                        type: "scene load",
                        settings: {},
                        property_updates: {},
                        scene_setting_updates: {
                            backgroundColor: {value: "#ffffff", operation: "set"},
                            cameraX: {value: 0, operation: "set"},
                            cameraY: {value: 0, operation: "set"},
                            cameraZoom: {value: 1, operation: "set"},
                            cameraFollowSprite: {value: null, operation: "set"},
                            camFollowX: {value: true, operation: "set"},
                            camFollowY: {value: true, operation: "set"}
                        },
                        scene_change: null
                    },
                ]
            }
        }
    })    
    */
    let tick = 0;

    function get_sprite_object(){
        let sprites = {}
        for (let sprite in project.scenes[current_scene].sprites){
            if (project.scenes[current_scene].sprites[sprite].type === "sprite")
                sprites[sprite] = sprite
        }
        return sprites
    }
    function get_tile_map_object(){
        let sprites = {}
        for (let sprite in project.scenes[current_scene].sprites){
            if (project.scenes[current_scene].sprites[sprite].type === "tile_map")
                sprites[sprite] = sprite
        }
        return sprites
    }
    function get_event_type_object(){
        let events = {}
        for (let event of Object.keys(EVENTS)){
            if (event === "combined event") continue
            events[event] = event
        }
        return events
    }
    function get_sprite_type(sprite){
        return project.scenes[current_scene].sprites[sprite].type
    }
   
    const KEYCODES = {
        space: 32,
        shift: 16,
        ctrl: 17,
        arrowUp: 38,
        arrowDown: 40,
        arrowLeft: 37,
        arrowRight: 39,
        a: 65,
        b: 66,
        c: 67,
        d: 68,
        e: 69,
        f: 70,
        g: 71,
        h: 72,
        i: 73,
        j: 74,
        k: 75,
        l: 76,
        m: 77,
        n: 78,
        o: 79,
        p: 80,
        q: 81,
        r: 82,
        s: 83,
        t: 84,
        u: 85,
        v: 86,
        w: 87,
        x: 88,
        y: 89,
        z: 90,
        å: 221,
        ä: 222,
        ö: 192,
        0: 48,
        1: 49,
        2: 50,
        3: 51,
        4: 52,
        5: 53,
        6: 54,
        7: 55,
        8: 56,
        9: 57,
    }
    const EVENTS = {
        "scene load": {
            get_settings: (event)=>{return {}},
            
            trigger_function: (settings)=>{if(tick===0){return true}; return false},
        },
        "sprite click": {
            get_settings: (event)=>{
                let sprite_obj = get_sprite_object()
                return {"Clicked sprite": {type: "select", options: sprite_obj}}
            },
            
            trigger_function: (settings)=>{
                if (sprites_just_clicked.has(settings["Clicked sprite"]))
                    return true
                return false
            },
            
        },
        "sprite collision": {
            get_settings: (event)=>{
                let sprite_obj = get_sprite_object()
                let tile_obj = get_tile_map_object()
                return {
                    "Sprite A": {type: "select", options: sprite_obj}, 
                    "Sprite B": {type: "select", options: {any: "any", ...tile_obj, ...sprite_obj}},
                    "Collision axis": {type: "select", options: {Either: "either", "Left/right": "x","Up/down": "y"}}
                }
            },
            
            trigger_function: (settings)=>{
                if (!Object.hasOwn(collisions, settings["Sprite A"]))
                    return false
                if (settings["Sprite B"] === "any"){
                    if (settings["Collision axis"] === "either")
                        return true
                    for (let sprite in collisions[settings["Sprite A"]]){
                        if (collisions[settings["Sprite A"]][sprite][settings["Collision axis"]])
                            return true
                    }
                    return false
                }
                if (!Object.hasOwn(collisions[settings["Sprite A"]], settings["Sprite B"]))
                    return false
                if (settings["Collision axis"] === "either")
                    return true
                if (collisions[settings["Sprite A"]][settings["Sprite B"]][settings["Collision axis"]])
                    return true
                return false
            },
        },
        "sprites touch": {
            get_settings: (event)=>{
                let sprite_obj = get_sprite_object()
                return {
                    "Sprite A": {type: "select", options: sprite_obj}, 
                    "Sprite B": {type: "select", options: sprite_obj},
                }
            },
            trigger_function: (settings)=>{
                if (settings["Sprite A"] === settings["Sprite B"]) return false
                if (tick === 0) return false

                let props1 = sprite_properties[settings["Sprite A"]]
                let props2 = sprite_properties[settings["Sprite B"]]

                let posX1 = props1.posX + props1.hitboxOffsetX
                let posY1 = props1.posY + props1.hitboxOffsetY
                let halfWidth1 = props1.hitboxWidth/2
                let halfHeight1 = props1.hitboxHeight/2
                let top1 = posY1 - halfHeight1
                let bottom1 = posY1 + halfHeight1
                let left1 = posX1 - halfWidth1
                let right1 = posX1 + halfWidth1

                let posX2 = props2.posX + props2.hitboxOffsetX
                let posY2 = props2.posY + props2.hitboxOffsetY
                let halfWidth2 = props2.hitboxWidth/2
                let halfHeight2 = props2.hitboxHeight/2
                let top2 = posY2 - halfHeight2
                let bottom2 = posY2 + halfHeight2
                let left2 = posX2 - halfWidth2
                let right2 = posX2 + halfWidth2

                if (top1 >= bottom2 || top2 >= bottom1 || left1 >= right2 || left2 >= right1) 
                    return false
                
                return true
            }
        },
        "key press": {
            get_settings: (event)=>{return {"Key": {type: "select", options: KEYCODES}}},
            
            trigger_function: (settings)=>{
                if (keys_just_pressed.has(settings.Key))
                return true;
            return false
            }
        },
        "key release": {
            get_settings: (event)=>{return {"Key": {type: "select", options: KEYCODES}}},
            
            trigger_function: (settings)=>{
                if (keys_just_released.has(settings.Key))
                return true;
            return false
            }
        },
        "key held": {
            get_settings: (event)=>{return {"Key": {type: "select", options: KEYCODES}}},
            
            trigger_function: (settings)=>{
                if (keys_down.has(settings.Key))
                    return true;
                return false
            }
        },
        "interval": {
            get_settings: (event)=>{return {
                "Unit": {
                    type: "select",
                    options: {
                        //Seconds: "sec",
                        Ticks: "tic",
                    },
                },
                "Interval": {
                    type: "number",
                    min: 1,
                    max: 1000000,
                },
                "Interval start": {
                    type: "number",
                    min: 0,
                    max: 1000000,
                }
            }},
            
            trigger_function: (settings)=>{
                if (tick < settings["Interval start"])
                    return false
                if ((tick - settings["Interval start"])%settings.Interval <= (tick - settings["Interval start"] - 1)%settings.Interval)
                    return true
                if (tick - settings["Interval start"] - 1 < 0)
                    return true
                return false
            }
        },
        "combined event": {
            get_settings: (event)=>{
                let settings = event.settings
                let n_events = settings["Number of events"]? settings["Number of events"]: 0
                let events = {}
                let event_type_obj = get_event_type_object()
                for (let i = 1; i <= n_events; i++){
                    events["Event "+i+" type"] = {type: "select", options: event_type_obj}
                    let type = settings["Event "+i+" type"]
                    if (!type) continue
                    for (let setting in EVENTS[type].get_settings({})){
                        let q = {}
                        q.type = EVENTS[type].get_settings({})[setting].type
                        if (q.type === "select"){
                            q.options = EVENTS[type].get_settings({})[setting].options
                        } else if (q.type = "number"){
                            q.min = EVENTS[type].min
                            q.max = EVENTS[type].max
                        }
                        events["Event "+i+" "+setting] = q
                    }

                }
                return {"Number of events": {type: "number", min: 0, max: 50}, ...events}
            },
            trigger_function: (settings)=>{
                for (let i = 1; i <= settings["Number of events"]; i++){
                    let type = settings["Event "+i+" type"]
                    let s = {}
                    for (let setting in EVENTS[type].get_settings({})){
                        s[setting] = settings["Event "+i+" "+setting]
                    }
                    if (!EVENTS[type].trigger_function(s)){
                        return false
                    }
                }
                return true
            }
        }
    }
    
    let keys_down = new Set()

    let keys_just_pressed = new Set()
    function onKeyDown(e){
        if (!running)
            return
        if (e.repeat)
            return
        keys_just_pressed.add(e.keyCode)
        keys_down.add(e.keyCode)
    }
    let keys_just_released = new Set()
    function onKeyUp(e){
        if (!running)
            return
        keys_just_released.add(e.keyCode)
        keys_down.delete(e.keyCode)
    }
    let sprites_just_clicked = new Set()

    let expanded_event_action = $state("")
    let expanded_sprite = $state("")
    
    let selected_event = $state(null)
    let new_event_type = $state("")
    function add_event(){
        if (!new_event_type)
            return
        
        project.scenes[current_scene].events.push({
            name: new_event_type,
            type: new_event_type,
            settings: {},
            property_updates: {},
            variable_updates: {},
            scene_setting_updates: {},
            scene_change: null,
        })
    }

    function remove_event(index){
        project.scenes[current_scene].events.splice(index, 1)
        if (selected_event === index)
            selected_event = null
        if (selected_event > index)
            selected_event --
        project = {...project}
    }
    function raise_event_prio(index){
        let events = project.scenes[current_scene].events
        let event1 = events[index]
        events[index] = events[index - 1]
        events[index - 1] = event1

        //events = [...events.slice(0, index - 1), events[index], events[index - 1], ...events.slice(index + 1)]
        //project.scenes[current_scene].events = events
    }
    function lower_event_prio(index){
        let events = project.scenes[current_scene].events
        let event1 = events[index]
        events[index] = events[index + 1]
        events[index + 1] = event1
    }
    
    let adding_asset = $state(false)
    let active_asset_tab = $state("Link")
    let asset_name = $state("")
    let asset_src = $state("")
    function get_property_updates(){
        return project.scenes[current_scene].events[selected_event].property_updates
    }
    
    function add_asset(){
        let images = project.assets.images
        if (Object.hasOwn(images, asset_name)){
            alert("Asset with that name already exists")
            return
        }
        if (asset_name === ""){
            alert("Please choose a name for your asset")
            return
        }
        images[asset_name] = asset_src
        adding_asset = false
        asset_name = ""
        asset_src = ""
    }

    let adding_sprite = $state(false)
    let sprite_name = $state("")
    let sprite_type = $state("sprite")
    function create_sprite(name){
        let scene = project.scenes[current_scene]
        let sprites = scene.sprites
        let events = scene.events
        
        if (Object.hasOwn(sprites, sprite_name)){
            alert("Sprite with that name already exists")
            return
        }
        if (sprite_name === ""){
            alert("Please choose a name for your sprite")
            return
        }
        
        switch (sprite_type){
            case "sprite":
                sprites[sprite_name] = {type: "sprite"}
                break
            case "tile_map":
                sprites[sprite_name] = {type: "tile_map", tiles: {}}
                break
        }
                
        events[0].property_updates[sprite_name] = {}
        for (let property in PROPERTY_INFO[sprite_type]){
            events[0].property_updates[sprite_name][property] = {value: PROPERTY_INFO[sprite_type][property].baseValue, operation: "set"}
        }
        adding_sprite = false
        sprite_name = ""
        sprite_type = "sprite"
        project = {...project}
    }
    function remove_sprite(sprite){
        if (selected_sprite === sprite)
            selected_sprite = ""
        if (expanded_sprite === sprite)
            expanded_sprite = ""
        delete project.scenes[current_scene].sprites[sprite]
        project.scenes[current_scene].events.forEach(event => {
            delete event.property_updates[sprite]
        });
    }

    let game_interval = ""
    let running = $state(false)
    let paused = $state(false)
    let calculator = $state(false)
    let event_status = $state([])

    function switch_scene(scene){
        current_scene = scene
        selected_event = null
        expanded_event_action = ""
        expanded_sprite = ""
        selected_sprite = ""
    }

    const FRAME_DURATION = (1000/30)
    function runScene(){
        running = true
        scene_settings = {}
        sprite_properties = {}
        collisions = {}
        for (let sprite in project.scenes[current_scene].sprites){
            sprite_properties[sprite] = {}
        }
        game_interval = setInterval(runFrame, FRAME_DURATION)
    }
    function stopScene(){
        running = false
        paused = false
        tick = 0
        event_status = []
        clearInterval(game_interval)
        //for (let sprite in project.scenes[current_scene].sprites){
        //    sprite_properties[sprite] = {}
        //}
    }
    function pauseScene(){
        paused = true
        clearInterval(game_interval)
    }
    function resumeScene(){
        paused = false
        game_interval = setInterval(runFrame, FRAME_DURATION)
    }
    
    function getEventStatus(){
    // Event status function -> Array/object with true/false for every event
        let events = project.scenes[current_scene].events
        let status = []
        // for each connected event in scene
        for (let index in events){
            let event = events[index]
            // get requested properties from sprites
        
            let settings = event.settings
            status.push(EVENTS[event.type].trigger_function(settings))
            // call trigger function of event with properties as parameter
            // append result of trigger function
        }
        return status
        // return array/object
    }
    
    const Physics = {
        apply_forces: function(){
            for (let sprite in sprite_properties){
                if (project.scenes[current_scene].sprites[sprite].type !== "sprite")
                    continue
                let props = sprite_properties[sprite]
                props.velY += props.gravity
                props.velX *= 1 - props.airResistance
                props.velY *= 1 - props.airResistance
            }
        },
        apply_vel: function(sprite, time){
            sprite_properties[sprite].posX += sprite_properties[sprite].velX * time
            sprite_properties[sprite].posY += sprite_properties[sprite].velY * time
        },
        resolve_collision: function(sprite1, sprite2, axis){
            let props1 = sprite_properties[sprite1]
            let props2 = sprite_properties[sprite2]
            let v1
            let v2
            let b = (props1.bounce + props2.bounce) / 2
            let m1 = props1.mass
            let m2 = props2.mass
            switch (axis){
                case "x":
                    v1 = props1.velX
                    v2 = props2.velX

                    if (get_sprite_type(sprite1) === "tile_map"){
                        props2.velX = (-b) * v2
                        break
                    }
                    if (get_sprite_type(sprite2) === "tile_map"){
                        props1.velX = (-b) * v1
                        break
                    }

                    if (props1.infiniteMass){
                        props2.velX = v1 - b * (v2 - v1)
                        break
                    }
                    if (props2.infiniteMass){
                        props1.velX = v2 - b * (v1 - v2)
                        break
                    }
                    
                    props1.velX = ((m1 - b * m2) * v1 + (1 + b) * m2 * v2) / (m1 + m2)
                    props2.velX = ((1 + b) * m1 * v1 + (m2 - b * m1) * v2) / (m1 + m2)
                    
                    break
                case "y":
                    v1 = props1.velY
                    v2 = props2.velY

                    if (get_sprite_type(sprite1) === "tile_map"){
                        props2.velY = (-b) * v2
                        break
                    }
                    if (get_sprite_type(sprite2) === "tile_map"){
                        props1.velY = (-b) * v1
                        break
                    }

                    if (props1.infiniteMass){
                        props2.velY = v1 - b * (v2 - v1)
                        break
                    }
                    if (props2.infiniteMass){
                        props1.velY = v2 - b * (v1 - v2)
                        break
                    }
                    
                    props1.velY = ((m1 - b * m2) * v1 + (1 + b) * m2 * v2) / (m1 + m2)
                    props2.velY = ((1 + b) * m1 * v1 + (m2 - b * m1) * v2) / (m1 + m2)
                    
                    
            }
        },
        colliding: function(sprite1, sprite2, time){
            let props1 = sprite_properties[sprite1]
            let props2 = sprite_properties[sprite2]

            // calculate hitbox frame bounds
            let posX1 = props1.posX + props1.hitboxOffsetX
            let posY1 = props1.posY + props1.hitboxOffsetY
            let velX1 = props1.velX
            let velY1 = props1.velY
            let halfWidth1 = props1.hitboxWidth/2
            let halfHeight1 = props1.hitboxHeight/2
            let top1 = posY1 - halfHeight1
            let bottom1 = posY1 + halfHeight1
            let left1 = posX1 - halfWidth1
            let right1 = posX1 + halfWidth1

            let posX2 = props2.posX + props2.hitboxOffsetX
            let posY2 = props2.posY + props2.hitboxOffsetY
            let velX2 = props2.velX
            let velY2 = props2.velY
            let halfWidth2 = props2.hitboxWidth/2
            let halfHeight2 = props2.hitboxHeight/2
            let top2 = posY2 - halfHeight2
            let bottom2 = posY2 + halfHeight2
            let left2 = posX2 - halfWidth2
            let right2 = posX2 + halfWidth2

            let boundTop1 = velY1 > 0 ? top1 : top1 + velY1 * time
            let boundBottom1 = velY1 < 0 ? bottom1 : bottom1 + velY1 * time
            let boundLeft1 = velX1 > 0 ? left1 : left1 + velX1 * time
            let boundRight1 = velX1 < 0 ? right1 : right1 + velX1 * time

            let boundTop2 = velY2 > 0 ? top2 : top2 + velY2 * time
            let boundBottom2 = velY2 < 0 ? bottom2 : bottom2 + velY2 * time
            let boundLeft2 = velX2 > 0 ? left2 : left2 + velX2 * time
            let boundRight2 = velX2 < 0 ? right2 : right2 + velX2 * time
            
            // if no overlap, skip
            if (boundTop1 >= boundBottom2 || boundTop2 >= boundBottom1 || boundLeft1 >= boundRight2 || boundLeft2 >= boundRight1) return null
            
            // check overlap on x- and y-axis
            let overlapYstart
            let overlapYend
            if (velY1 === velY2){
                overlapYstart = -Infinity
                overlapYend = Infinity
            } else if (velY1 > velY2){
                overlapYstart = (top2 - bottom1) / (velY1 - velY2)
                overlapYend = (bottom2 - top1) / (velY1 - velY2)
            } else{
                overlapYstart = (bottom2 - top1) / (velY1 - velY2)
                overlapYend = (top2 - bottom1) / (velY1 - velY2)
            }
            
            let overlapXstart
            let overlapXend
            if (velX1 === velX2){
                overlapXstart = -Infinity
                overlapXend = Infinity
            } else if (velX1 > velX2){
                overlapXstart = (left2 - right1) / (velX1 - velX2)
                overlapXend = (right2 - left1) / (velX1 - velX2)
            } else{
                overlapXstart = (right2 - left1) / (velX1 - velX2)
                overlapXend = (left2 - right1) / (velX1 - velX2)
            }

            // if overlap on axis do not intersect, skip
            if (!(overlapXstart < overlapYend && overlapYstart < overlapXend)) return null
            if (overlapXstart > time || overlapYstart > time) return null
            
            // at this point, the sprites must have collided
            
            let alreadyOverlapX = overlapXstart < -0.0001
            let alreadyOverlapY = overlapYstart < -0.0001

            if (alreadyOverlapX && alreadyOverlapY){
                return null
            }
            
            let collision_axis = alreadyOverlapX ? "y" : alreadyOverlapY ? "x": overlapXstart < overlapYstart ? "x": "y"
            return {axis: collision_axis, time: (overlapXstart > overlapYstart ? overlapXstart: overlapYstart)}
        },
        tile_colliding: function(sprite, tile_map, time){
            let sprite_props = sprite_properties[sprite]
            let tile_props = sprite_properties[tile_map]
            let tile_data = project.scenes[current_scene].sprites[tile_map].tiles

            let spriteX = sprite_props.posX + sprite_props.hitboxOffsetX
            let spriteY = sprite_props.posY + sprite_props.hitboxOffsetY
            let spriteVX = sprite_props.velX
            let spriteVY = sprite_props.velY
            let spriteHalfWidth = sprite_props.hitboxWidth/2
            let spriteHalfHeight = sprite_props.hitboxHeight/2
            let spriteTop = spriteY - spriteHalfHeight
            let spriteBottom = spriteY + spriteHalfHeight
            let spriteLeft = spriteX - spriteHalfWidth
            let spriteRight = spriteX + spriteHalfWidth

            let boundTop = spriteVY > 0 ? spriteTop : spriteTop + spriteVY * time
            let boundBottom = spriteVY < 0 ? spriteBottom: spriteBottom + spriteVY * time
            let boundLeft = spriteVX > 0 ? spriteLeft : spriteLeft + spriteVX * time
            let boundRight = spriteVX < 0 ? spriteRight : spriteRight + spriteVX * time

            let firstTileX = Math.floor((boundLeft - tile_props.offsetX) / tile_props.tileWidth)
            let lastTileX = Math.floor((boundRight - tile_props.offsetX) / tile_props.tileWidth)
            let firstTileY = Math.floor((boundTop - tile_props.offsetY) / tile_props.tileHeight)
            let lastTileY = Math.floor((boundBottom - tile_props.offsetY) / tile_props.tileHeight)

            let collision = null

            for (let x = firstTileX; x <= lastTileX; x++){
                for (let y = firstTileY; y <= lastTileY; y++){

                    let key = JSON.stringify({x: x, y: y})
                    if (tile_data[key] === undefined) continue // Object.hasOwn() fungerade inte här pga proxy eller något det var jätteskumt
                    
                    let tileLeft = x * tile_props.tileWidth + tile_props.offsetX
                    let tileRight = x * tile_props.tileWidth + tile_props.offsetX + tile_props.tileWidth
                    let tileTop = y * tile_props.tileHeight + tile_props.offsetY
                    let tileBottom = y * tile_props.tileHeight + tile_props.offsetY + tile_props.tileHeight

                    let overlapYstart
                    let overlapYend
                    if (spriteVY === 0 && !(tileTop === boundBottom || tileBottom === boundTop)){
                        overlapYstart = -Infinity
                        overlapYend = Infinity
                    } else if (spriteVY > 0){
                        overlapYstart = (tileTop - spriteBottom) / spriteVY
                        overlapYend = (tileBottom - spriteTop) / spriteVY
                    } else{
                        overlapYstart = (tileBottom - spriteTop) / spriteVY
                        overlapYend = (tileTop - spriteBottom) / spriteVY
                    }

                    let overlapXstart
                    let overlapXend
                    if (spriteVX === 0 && !(tileLeft === boundRight || tileRight === boundLeft)){
                        overlapXstart = -Infinity
                        overlapXend = Infinity
                    } else if (spriteVX > 0){
                        overlapXstart = (tileLeft - spriteRight) / spriteVX
                        overlapXend = (tileRight - spriteLeft) / spriteVX
                    } else{
                        overlapXstart = (tileRight - spriteLeft) / spriteVX
                        overlapXend = (tileLeft - spriteRight) / spriteVX
                    }

                    // if overlap on axis do not intersect, skip
                    if (!(overlapXstart < overlapYend && overlapYstart < overlapXend)) continue
                    if (overlapXstart > time || overlapYstart > time) continue
                    
                    // at this point, the sprites must have collided
                    
                    let alreadyOverlapX = overlapXstart < -0.0001
                    let alreadyOverlapY = overlapYstart < -0.0001

                    if (alreadyOverlapX && alreadyOverlapY){
                        continue
                    }
                    let collision_axis = alreadyOverlapX ? "y" : alreadyOverlapY ? "x": overlapXstart < overlapYstart ? "x": "y"
                    let coll_time = collision_axis === "x" ? overlapXstart : overlapYstart

                    if (collision === null)
                        collision = {time: coll_time, x: collision_axis === "x", y: collision_axis === "y"}
                    else if (coll_time <= collision.time){
                        if (coll_time === collision.time)
                            collision[collision_axis] = true
                        else {
                            collision.time = coll_time
                            collision.x = collision_axis === "x"
                            collision.y = collision_axis === "y"
                        }
                    }
                }
            }
            return collision
        }
    }

    let collisions = {}
    
    function runFrame(){
         
        // Main loop

        // Call event status function to get array/object of what events are triggered
        event_status = getEventStatus()
        
        keys_just_pressed.clear()
        keys_just_released.clear()
        sprites_just_clicked.clear()

        // For the triggered events, update the sprites properties
        let sprites = project.scenes[current_scene].sprites
        let events = project.scenes[current_scene].events
        for (let index in events){
            let event = events[index]
            if (!event_status[index]) continue
            
            if (event.scene_change !== null){ // scene change
                stopScene()
                switch_scene(event.scene_change)
                runScene()
                return
            }

            // property updates
            let prop_updates = event.property_updates
            for (let sprite in prop_updates){

                let properties = prop_updates[sprite]
                for (let property in properties){
                    switch (properties[property].operation){
                        case "set":
                            sprite_properties[sprite][property] = properties[property].value;
                            break
                        case "add":
                            sprite_properties[sprite][property] += properties[property].value;
                            break
                        case "multiply":
                            sprite_properties[sprite][property] *= properties[property].value;
                            break
                    }

                    let prop_info = PROPERTY_INFO[project.scenes[current_scene].sprites[sprite].type][property]
                    if (prop_info.type !== "float") continue
                    if (sprite_properties[sprite][properties] > prop_info.max){
                        sprite_properties[sprite][properties] = prop_info.max
                    } else if (sprite_properties[sprite][properties] < prop_info.min){
                        sprite_properties[sprite][properties] = prop_info.min
                    }
                }
            }

            // scene setting updates
            let setting_updates = event.scene_setting_updates
            for (let setting in setting_updates){
                switch (setting_updates[setting].operation){
                    case "set":
                        scene_settings[setting] = setting_updates[setting].value;
                        break
                    case "add":
                        scene_settings[setting] += setting_updates[setting].value;
                        break
                    case "multiply":
                        scene_settings[setting] *= setting_updates[setting].value;
                        break
                }

                let setting_info = SCENE_SETTING_INFO[setting]
                if (setting_info.type !== "float") continue
                if (scene_settings[setting] > setting_info.max){
                    scene_settings[setting] = setting_info.max
                } else if (scene_settings[setting] < setting_info.min){
                    scene_settings[setting] = setting_info.min
                }
            }
        }

        let cam_follow_sprite = scene_settings.cameraFollowSprite
        if (cam_follow_sprite !== null){
            if (scene_settings.camFollowX)
                scene_settings.cameraX = sprite_properties[cam_follow_sprite].posX
            if (scene_settings.camFollowY)
                scene_settings.cameraY = sprite_properties[cam_follow_sprite].posY
        }

        collisions = {}

        Physics.apply_forces()


        // physics

        let affected_sprites = new Set(Object.keys(sprite_properties))
        let frame_left = 1
        
        let iterations = 0
        while (frame_left > 0){
            let collision_times = {}
            let unused_sprites = new Set(Object.keys(sprite_properties))
            
            // for each sprite
            for (let sprite1 of affected_sprites){

                if (get_sprite_type(sprite1) !== "sprite") continue

                // remove sprite from set of unused sprites
                unused_sprites.delete(sprite1)

                let props1 = sprite_properties[sprite1]
                // if not collidable, skip
                if (!props1.collidable) continue

                // for each unused sprite
                for (let sprite2 of unused_sprites){
                    let props2 = sprite_properties[sprite2]
                    let is_tile_map = get_sprite_type(sprite2) === "tile_map"

                    if (get_sprite_type(sprite2) !== "sprite" && !is_tile_map) continue

                    // if not collidable, skip
                    if (!props2.collidable) continue

                    // if sprites do not have any common collision group, skip
                    if (!props1.collisionGroups.some((group)=>{return props2.collisionGroups.includes(group)})) continue

                    let collision
                    if (!is_tile_map){
                        // if both sprites have infinite mass, skip
                        if (props1.infiniteMass && props2.infiniteMass) continue

                        // at this point the sprites must be able to collide

                        collision = Physics.colliding(sprite1, sprite2, frame_left)
                    } else {
                        collision = Physics.tile_colliding(sprite1, sprite2, frame_left)
                    }

                    if (collision === null) continue // no collision, skip

                    if (!Object.hasOwn(collision_times, collision.time)){
                        collision_times[collision.time] = []
                    }

                    if (!is_tile_map){
                        collision_times[collision.time].push({axis: collision.axis, sprites: [sprite1, sprite2]})
                    }
                    else{
                        if (collision.x && collision.y){
                            collision_times[collision.time].push({axis: "x", sprites: [sprite1, sprite2]})
                            collision_times[collision.time].push({axis: "y", sprites: [sprite1, sprite2]})
                        } else {
                            collision_times[collision.time].push({axis: collision.x ? "x": "y", sprites: [sprite1, sprite2]})
                        }
                    }
                    
                
                }
            }
            
            // check if collision_times is empty
            let no_times = true
            for (let i in collision_times){
                no_times = false
                break
            }

            let time
            if (no_times){
                time = frame_left
            } else {
                time = Math.min(...Object.keys(collision_times).map(Number))
            }
            
            // update positions up to time of collision
            for (let sprite in sprite_properties){
                if (get_sprite_type(sprite) === "sprite")
                    Physics.apply_vel(sprite, time)
            }
            frame_left -= time
            
            if (!no_times){
                //console.log(sprite_properties)
                // resolve colliding sprites
                for (let coll of collision_times[time]){
                    if (!Object.hasOwn(collisions, coll.sprites[0])){
                        collisions[coll.sprites[0]] = {}
                    }
                    if (!Object.hasOwn(collisions[coll.sprites[0]], coll.sprites[1])){
                        collisions[coll.sprites[0]][coll.sprites[1]] = {x: false, y: false}
                    }
                    collisions[coll.sprites[0]][coll.sprites[1]][coll.axis] = true

                    if (!Object.hasOwn(collisions, coll.sprites[1])){
                        collisions[coll.sprites[1]] = {}
                    }
                    if (!Object.hasOwn(collisions[coll.sprites[1]], coll.sprites[0])){
                        collisions[coll.sprites[1]][coll.sprites[0]] = {x: false, y: false}
                    }
                    collisions[coll.sprites[1]][coll.sprites[0]][coll.axis] = true
                    
                    Physics.resolve_collision(coll.sprites[0], coll.sprites[1], coll.axis)
                    affected_sprites.add(coll.sprites[0])
                    affected_sprites.add(coll.sprites[1])
                }
            }

            iterations ++
            if (iterations > 1000) {
                alert("1000+ collisions in one frame, what have you done?")
                stopScene()
                break
            }
        }
        //console.log(iterations)
        tick ++
    }
    
    let example = [[5, '+', 4, '*', 2], '-', 2] // 11
    function calculate(expression){
        if (typeof(expression) === "number")
            return expression

        let terms = []
        for (let factor of expression){

        }
    }
</script>


<main>
    <section id="bar">
        <a href="{base}/"><i class="fa-solid fa-house"></i></a>
        <input type="text" bind:value={project.name}>
        <button onclick={()=>{console.log($state.snapshot(project))}}>Print project</button>
        
    </section>

    <section id="game-bar">
        {#if running}
            <div>
                <button class="play_button" onclick={stopScene}>Stop</button>
                {#if paused}
                    <button class="play_button" onclick={resumeScene}>Resume</button>
                    <button class="play_button" onclick={runFrame}>Step Frame</button>
                {:else}
                    <button class="play_button" onclick={pauseScene}>Pause</button>
                {/if}
            </div>
        {:else if current_scene}
            <button class="play_button" onclick={runScene}>Run Scene</button>
        {/if}
        <!--<button onclick={()=>{calculator = !calculator}}>Calc</button>-->
    </section>

    <section id="variables">
        <h1>Variables</h1>
        <h2>{current_scene} Local</h2>
            {#if current_scene}
                {#each Object.entries(project.scenes[current_scene].local_variables) as [name, value]}
                    <div class="variable_row">
                        <div>{name}</div>
                        <div>|</div>
                        <div>{value}</div>
                    </div>
                {/each}
            {/if}
        <h2>Global</h2>
        {#each Object.entries(project.global_variables) as [name, value]}
            <div class="variable_row">
                <div>{name}</div>
                <div>|</div>
                <div>{value}</div>
            </div>
        {/each}
    </section>

    <section id="events">
        <h1>Events</h1>
        <div class="add_container">
            {#if current_scene}
            <select class="selection" bind:value={new_event_type}>
                {#each Object.keys(EVENTS) as event}
                    {#if event !== "scene load"}
                        <option value={event}>{event}</option>
                    {/if}
                {/each}
            </select>
            <button class="add_button" onclick={add_event}>Add</button>
            {/if}
        </div>
        <div class="item_list">
            {#if current_scene}
            {#each project.scenes[current_scene].events as event, index}
                <div class="list_header">
                    <div class="event_priority">
                        {#if event.type !== "scene load" && index !== 1}
                            <button class="event_priority_button" onclick={()=>{raise_event_prio(index)}}>^</button>
                        {/if}
                        {#if event.type !== "scene load" && index !== project.scenes[current_scene].events.length - 1}
                            <button class="event_priority_button" onclick={()=>{lower_event_prio(index)}}>v</button>
                        {/if}
                    </div>
                    <button style={event_status[index]?"background-color: var(--green-3); border-color: var(--green-2)":""} class={selected_event===index?"event_button event_button_expanded":"event_button"} onclick={()=>{if(selected_event===index){selected_event=null}else{selected_event=index}; expanded_event_action=""}}>
                        <h2>{event.name}</h2>
                        {selected_event===index?"^":"v"}
                    </button>
                    {#if event.type !== "scene load"}
                        <button class="remove_item_button" onclick={()=>{remove_event(index)}}>X</button>
                    {/if}
                </div>
                {#if selected_event === index}
                    <div class="event_info" style={event_status[index] ? "border-color: var(--green-2)": ""}>
                        <div class="variable_row"> <!-- Event type -->
                            <p>Event type</p>
                            <p>|</p>
                            <p>{event.type}</p>
                        </div>

                        {#each Object.entries(EVENTS[event.type].get_settings(event)) as [name, data]}
                            <div class="variable_row">
                                <label for={name}>{name}</label>
                                {#if data.type === "select"}
                                    <select bind:value={event.settings[name]} id={name}>
                                        {#each Object.entries(data.options) as [n, value]}
                                            <option value={value}>{n}</option>
                                        {/each}
                                    </select>
                                {:else if data.type === "number"}
                                    <input type="number" min={data.min} max={data.max} step="any" bind:value={event.settings[name]} id={name}>
                                {/if}
                            </div>
                        {/each}
                    </div>
                {/if}
            {/each}
            {/if}
        </div>

    </section>

    <section id="properties">
        <h1>Event Actions</h1>
        
        <div class="item_list">
            {#if selected_event !== null}
                {#each ["Property updates", "Scene setting updates", "Scene change"] as action}
                    <div class="list_header">
                        <button class={expanded_event_action === action ? "event_button event_button_expanded": "event_button"} onclick={()=>{expanded_event_action = expanded_event_action === action ? "": action; expanded_sprite = ""}}>
                            <h2>{action}</h2>
                            {expanded_event_action === action ? "^": "v"}
                        </button>
                    </div>
                    {#if expanded_event_action === action}
                        <div class="event_info">
                            {#if action === "Property updates"}
                                {#each Object.entries(project.scenes[current_scene].sprites) as [sprite, data]}
                                    <div class="devider_line"></div>
                                    <button class = "property_updates_header" onclick={()=>{
                                            expanded_sprite === sprite? expanded_sprite="": expanded_sprite=sprite; 
                                            if (!Object.hasOwn(get_property_updates(), sprite)){
                                                get_property_updates()[sprite] = {}
                                            }}}>
                                        <h3>{sprite}</h3>
                                        {sprite===expanded_sprite?"^":"v"}
                                    </button>
                                    {#if expanded_sprite === sprite}
                                        <br>
                                        {#each Object.entries(PROPERTY_INFO[data.type]) as [property, info]}
                                            <div class="variable_row">
                                                <label for={property}>{property}</label>
                                                {#if Object.hasOwn(get_property_updates()[sprite], property)}
                                                    {#if info.type === "select"}
                                                        <select id={property} bind:value={project.scenes[current_scene].events[selected_event].property_updates[sprite][property].value}>
                                                            {#each Object.entries(info.getOptions()) as [name, value]}
                                                                <option value={value}>{name}</option>
                                                            {/each}
                                                        </select>
                                                    {:else if info.type === "select_multiple"}
                                                        <select id={property} bind:value={project.scenes[current_scene].events[selected_event].property_updates[sprite][property].value[get_property_updates()[sprite][property].value.length]}>
                                                            {#each info.getOptions() as value}
                                                                <option value={value}>{value}</option>
                                                            {/each}
                                                        </select>
                                                        {#each get_property_updates()[sprite][property].value as value}
                                                            <div>{value}</div>
                                                            <button class="remove_item_button">X</button>
                                                        {/each}
                                                    {:else if info.type === "bool"}
                                                        <input id={property} type="checkbox" bind:checked={project.scenes[current_scene].events[selected_event].property_updates[sprite][property].value}>
                                                    {:else if info.type === "float"}
                                                        {#if selected_event !== 0}
                                                            <select bind:value={project.scenes[current_scene].events[selected_event].property_updates[sprite][property].operation}>
                                                                <option value="set">set</option>
                                                                <option value="add">add</option>
                                                                <option value="multiply">multiply</option>
                                                            </select>
                                                        {/if}
                                                        <input id={property} type="number" min={info.min} max={info.max} step="any" bind:value={project.scenes[current_scene].events[selected_event].property_updates[sprite][property].value}>
                                                    {:else if info.type === "text"}
                                                        <input id={property} type="text" bind:value={project.scenes[current_scene].events[selected_event].property_updates[sprite][property].value}>
                                                    {/if}
                                                    {#if selected_event !== 0}
                                                        <button class="remove_item_button" onclick={()=>{delete get_property_updates()[sprite][property]; project = {...project}}}>X</button>
                                                    {/if}
                                                {:else}
                                                    <button onclick={()=>{get_property_updates()[sprite][property] = {value: info.baseValue, operation: "set"}; project = {...project}/*Force trigger reactivity*/}}>Set</button>
                                                {/if}
                                            </div>
                                        {/each}
                                    {/if}
                                {/each}
                            {:else if action === "Scene setting updates"}
                                {#each Object.entries(SCENE_SETTING_INFO) as [setting, info]}
                                    <div class="variable_row">
                                        <label for={setting}>{setting}</label>
                                        {#if Object.hasOwn(project.scenes[current_scene].events[selected_event].scene_setting_updates, setting)}
                                            {#if info.type === "select"}
                                                <select id={setting} bind:value={project.scenes[current_scene].events[selected_event].scene_setting_updates[setting].value}>
                                                    {#each Object.entries(info.getOptions()) as [name, value]}
                                                        <option value={value}>{name}</option>
                                                    {/each}
                                                </select>
                                            
                                            {:else if info.type === "bool"}
                                                <input id={setting} type="checkbox" bind:checked={project.scenes[current_scene].events[selected_event].scene_setting_updates[setting].value}>
                                            {:else if info.type === "float"}
                                                {#if selected_event !== 0}
                                                    <select bind:value={project.scenes[current_scene].events[selected_event].scene_setting_updates[setting].operation}>
                                                        <option value="set">set</option>
                                                        <option value="add">add</option>
                                                        <option value="multiply">multiply</option>
                                                    </select>
                                                {/if}
                                                <input id={setting} type="number" min={info.min} max={info.max} step="any" bind:value={project.scenes[current_scene].events[selected_event].scene_setting_updates[setting].value}>
                                            {:else if info.type === "text"}
                                                <input id={setting} type="text" bind:value={project.scenes[current_scene].events[selected_event].scene_setting_updates[setting].value}>
                                            {:else if info.type === "color"}
                                                <input id={setting} type="color" bind:value={project.scenes[current_scene].events[selected_event].scene_setting_updates[setting].value}>
                                            {/if}
                                            {#if selected_event !== 0}
                                                <button class="remove_item_button" onclick={()=>{delete project.scenes[current_scene].events[selected_event].scene_setting_updates[setting]; project = {...project}}}>X</button>
                                            {/if}
                                        {:else}
                                            <button onclick={()=>{project.scenes[current_scene].events[selected_event].scene_setting_updates[setting] = {value: info.baseValue, operation: "set"}; project = {...project}/*Force trigger reactivity*/}}>Set</button>
                                        {/if}
                                    </div>
                                {/each}
                            {:else if action === "Scene change"}
                                <div class="variable_row">
                                    <label for="load_scene">Load scene</label>
                                    <select id="load_scene" bind:value={project.scenes[current_scene].events[selected_event].scene_change}>
                                        <option value={null}>None</option>
                                        {#each Object.keys(project.scenes) as scene}
                                            <option value={scene}>{scene}</option>
                                        {/each}
                                    </select>
                                </div>
                            {/if}
                        </div>
                    {/if}
                {/each}
            {/if}
            
            
        </div>
    </section>

    <section id={calculator===true?"calculator":"game"} bind:clientWidth={game_window_width} bind:clientHeight={game_window_height} onmousedown={mouseDown} role="none" ondragstart={(e)=>e.preventDefault()} bind:this={game_section} style="background-color: {running ? scene_settings.backgroundColor : current_scene ? project.scenes[current_scene].events[0].scene_setting_updates.backgroundColor.value: "#ffffff"};">
        {#if calculator}
            <div id="calc_area">

            </div>
            <div id="calc_keypad">
                <button>+</button>
            </div>
        {:else if running}
            <div id="viewport" style="transform: scale({scene_settings.cameraZoom}); transition:{running? "all "+FRAME_DURATION+"ms linear":"none"};">
                {#each Object.entries(sprite_properties) as [name, sprite]}
                    {#if get_sprite_type(name) === "sprite"}
                        <div class="sprite" style="left: {sprite.posX + game_window_width/2 - scene_settings.cameraX}px; top: {sprite.posY + game_window_height/2 - scene_settings.cameraY}px; transition: all {FRAME_DURATION}ms linear;">
                            <img src={sprite.image} alt={name} draggable="false" style="transform:scale({sprite.scaleX}, {sprite.scaleY}) rotate({sprite.rotation}deg); z-index: {sprite.Zindex};">
                        </div>
                        
                        <div class="hitbox_hidden" onclick={()=>{sprites_just_clicked.add(name);}} onkeyup={()=>{}} role="button" tabindex="0" style="left: {sprite.posX + sprite.hitboxOffsetX  + game_window_width/2 - scene_settings.cameraX}px; top:{sprite.posY + sprite.hitboxOffsetY  + game_window_height/2 - scene_settings.cameraY}px; width: {sprite.hitboxWidth}px; height: {sprite.hitboxHeight}px; transition: all {FRAME_DURATION}ms linear;"></div>
                    {:else if get_sprite_type(name) === "tile_map"}
                        {#each Object.entries(project.scenes[current_scene].sprites[name].tiles) as [pos_str, image]}
                            {@const pos = JSON.parse(pos_str)}
                            <div class="tile" style="left: {pos.x * sprite.tileWidth + sprite.offsetX + game_window_width/2 - scene_settings.cameraX}px; top: {pos.y * sprite.tileHeight + sprite.offsetY + game_window_height/2 - scene_settings.cameraY}px; transition: all {FRAME_DURATION}ms linear;">
                                <img src={project.assets.images[image]} draggable="false" style="width: {sprite.tileWidth}px; height: {sprite.tileHeight}px;">
                            </div>
                        {/each}
                    {/if}
                {/each}
            </div>
        {:else}
            <div id="viewport">
                {#if current_scene}
                {#each Object.entries(project.scenes[current_scene].events[0].property_updates) as [name, sprite]}
                {#if get_sprite_type(name) === "sprite"}
                    <div class="sprite" style="left: {sprite.posX.value + game_window_width/2 - editor_camX}px; top: {sprite.posY.value + game_window_height/2 - editor_camY}px; transition: none;">
                        <img src={sprite.image.value} alt={name} draggable="false" style="transform:scale({sprite.scaleX.value}, {sprite.scaleY.value}) rotate({sprite.rotation.value}deg); z-index: {sprite.Zindex.value};">
                    </div>
                    
                    <div class="hitbox" style="left: {sprite.posX.value + sprite.hitboxOffsetX.value + game_window_width/2 - editor_camX}px; top:{sprite.posY.value + sprite.hitboxOffsetY.value + game_window_height/2 - editor_camY}px; width: {sprite.hitboxWidth.value}px; height: {sprite.hitboxHeight.value}px;"></div>
                {:else if get_sprite_type(name) === "tile_map"}
                    {#each Object.entries(project.scenes[current_scene].sprites[name].tiles) as [pos_str, image]}
                        {@const pos = JSON.parse(pos_str)}
                        <div class="tile" style="left: {pos.x * sprite.tileWidth.value + sprite.offsetX.value + game_window_width/2 - editor_camX}px; top: {pos.y * sprite.tileHeight.value + sprite.offsetY.value + game_window_height/2 - editor_camY}px; width: {sprite.tileWidth.value}px; height: {sprite.tileHeight.value}px;">
                            <img src={project.assets.images[image]} draggable="false">
                        </div>
                    {/each}
                {/if}
                {/each}
                {/if}

                {#if selected_sprite !== "" && get_sprite_type(selected_sprite) === "tile_map"}
                    <div id="tile_map_editor">
                        <button class="tile_editor_button" id={tiling?"active_tile_button":""} onclick={()=>{if (tiling){tiling = false} else {tiling = true; erasing = false}}}><i class="fa-solid fa-pen"></button>
                        <button class="tile_editor_button" id={erasing?"active_tile_button":""} onclick={()=>{if (erasing){erasing = false} else {tiling = false; erasing = true}}}><i class="fa-solid fa-eraser"></button>
                        <div>
                            <select bind:value={tile_image}>
                                <option value="">None</option>
                                {#each Object.keys(project.assets.images) as image}
                                    <option value={image}>{image}</option>
                                {/each}
                            </select>
                            <img src={project.assets.images[tile_image]} class="tile_editor_image">
                        </div>
                    </div>
                {/if}
            </div>
        {/if}
    </section>
    
    <section id="assets">
        <h1>Assets</h1>
        <div class="item_grid">
            {#each Object.entries(project.assets.images) as [name, image]}
                <div class="asset">
                    <img src={image} alt="Failed to load asset">
                    <p>{name}</p>
                </div>
            {/each}
            <button class="add_button" onclick={()=>{adding_asset = true}}><i class="fa-solid fa-plus"/></button>

        </div>
    </section>

    <section id="scene">
        <h1>Scene</h1>
        <div class="tabs_bar">
            {#each Object.keys(project.scenes) as scene}
                <button class={current_scene===scene ? "tab active_tab": "tab"} onclick={()=>{switch_scene(scene)}}>{scene}</button>
            {/each}
            <button class="new_tab_button" onclick={add_scene}>+</button>
        </div>
        <div class="item_grid">
            {#if current_scene}
            {#each Object.keys(project.scenes[current_scene].sprites) as sprite}
                <div class="sprite_box">
                    <button class="sprite_button" onclick={()=>{sprite === selected_sprite ? selected_sprite = "" : selected_sprite = sprite; if(selected_sprite===sprite){selected_event=0; expanded_event_action="Property updates"; expanded_sprite=sprite}}} style="{sprite === selected_sprite ? "background-color: var(--grey-5);":""} {get_sprite_type(sprite) === "tile_map" ? "padding-top: 30px;" : ""}">
                        {#if get_sprite_type(sprite) === "sprite"}
                            <img src={project.scenes[current_scene].events[0].property_updates[sprite].image.value} alt="No image">
                            <i class="fa-solid fa-shield-cat"></i>
                        {:else if get_sprite_type(sprite) === "tile_map"}
                            <i class="fa-solid fa-border-all"></i>
                        {/if}
                        <b>{sprite}</b>
                    </button>
                    <button class="remove_asset_button" onclick={()=>{remove_sprite(sprite)}}><i class="fa-regular fa-trash-can"></i></button>
                </div>
            {/each}
            {/if}
            {#if current_scene}
                <button class="add_button" onclick={()=>{adding_sprite=true}}><i class="fa-solid fa-plus"/></button>
            {/if}
        </div>
    </section>

    {#if adding_asset}
    <div class="selection_window">
        <div class="selection_window_header">
            <p>Choose asset</p>
            <button class="remove_item_button" onclick={()=>{adding_asset = false}}>X</button>
        </div>
        <div class="tabs_bar">
            {#each ["Link"] as tab}
                <button class={active_asset_tab === tab ? "tab active_tab": "tab"} onclick={()=>{active_asset_tab = tab}}>{tab}</button>
            {/each}
        </div>
        <label for="asset_name">Asset name</label>
        <input id="asset_name" bind:value={asset_name} type="text" defaultValue="Cool Image 1">
        {#if active_asset_tab === "Link"}
            <label for="asset_url">Image URL</label>
            <input id="asset_url" type="text" placeholder="Paste image URL here" bind:value={asset_src}>
            <div class="assets_image_wrapper">
                <img src={asset_src} alt="Please paste a valid image URL">
            </div>
            <button class="add_button" style="margin-top: auto;" onclick={add_asset}>Insert</button>
        {:else if active_asset_tab === "Choose"}
            This feature does not exist yet
        {:else if active_asset_tab === "Upload"}
            This feature does not exist yet
        {/if} 
    </div>
    {:else if adding_sprite}
    <div class="selection_window">
        <div class="selection_window_header">
            <p>Add sprite</p>
            <button class="remove_item_button" onclick={()=>{adding_sprite = false}}>X</button>
        </div>
        <label for="sprite_name">Sprite name</label>
        <input type="text" id="sprite_name" bind:value={sprite_name}>

        <label for="sprite_type">Sprite type</label>
        <select id="sprite_type" bind:value={sprite_type}>
            <option value="sprite">Normal sprite</option>
            <option value="tile_map">Tile map</option>
            <!--<option value="ui">UI sprite</option>-->
        </select>
        <p>Set the sprites starting properties, including image, in the "on scene load"-event.</p>
        <button class="add_button" style="margin-top: auto" onclick={create_sprite}>Add sprite</button>
    </div>
    {/if}

</main>