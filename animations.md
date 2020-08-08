## CSS STEPS TIMING FUNCTION
### Function: Allows us to break an animation or transition into segments, rather than one continuous transition from one state to another. 
### Parameters: 
  + number_of_steps: The number of frames we will break our animation/transition into. Must be positive.
  + direction: **(optional)** Determines when will this frame occur?
    + start: Each frame animation will execute at the start of each frame duration.
    + end: **(default)** Each frame animation will execute at the end of each frame duration.

#### [View Visual Example][1]

#### Example: 
    animation: play 1s steps(10) infinite;
    @keyframes play {
	      100% { background-position: 1900px; }
    }
    
#### Explanation:
    The animation executes 1 frame every .1s (animation duration / # of frames) and will run on an infinite loop.
    We execute a total of 10 frames in 1 second and the complete animation is a shift in the background-position of 1900px.
    Since we have 10 frames, each frame will shift the background 190px.
    
#### Timeline of animation: 
Shows at the start of each frame how many pixels have we transitioned from where we started.
    
|        | 1      | 2      | 3      | 4      | 5      | 6      | 7      | 8      | 9      | 10     |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| start: | 190px  | 380px  | 570px  | 760px  | 950px  | 1140px | 1330px | 1520px | 1710px | 1900px |
| end:   | 0px    | 190px  | 380px  | 570px  | 760px  | 950px  | 1140px | 1330px | 1520px | 1710px |

[1]: https://codepen.io/Guilh/pen/yldGp
