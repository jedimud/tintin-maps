# tintin-maps

Unicode maps for Jedimud generated with TinTin++.

![](midgaard.png)

## Legend

`[ ]` Basic Path

`[$]` Bank

`[#]` Shop/Vendor

`[%]` Fountain

`[D]` Donation

`[M]` Guild Master

`[&]` Innkeeper

`↖ ↑ ↗ ← · → ↙ ↓ ↘` Map Exit

`[ ]+` Exit Up

`[ ]-` Exit Down

## Usage

**show map**

````
#alias map_show {
    #split 0 1 0 -80;
    #map offset 1 81 -1 -1;
}
````

**hide map**

````
#alias map_hide {
    #split;
    #map offset;
}
````

**login from Midgaard**

````
#alias login_midgaard {
    #map read midgaard.map; 
    #map goto 1; 
    #map flag static on;
    map_hide;
    map_show;
    #variable map_current midgaard.map;
}
````

**login from Skara Brae**

`# TODO`

**login from New Thalos**

`# TODO`

**recite group recall**

````
#alias rc {
    c 'group recall';
    #map read midgaard.map;
    #map goto 1; 
    #map flag static on;
    map_hide;
    map_show;
    #variable map_current midgaard.map;
}
````
