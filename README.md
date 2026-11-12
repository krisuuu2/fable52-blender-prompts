# fable52-blender-prompts

The two prompts from my reel "Claude Fable 5.2 makes a 3D film in Blender from one prompt" ([@aipractically](https://www.instagram.com/aipractically/)).

Each prompt makes Claude write one Python script that builds a full Blender scene (models, materials, light, camera move, colour grade) and renders it with Cycles. No downloaded models and no AI images.

## How to use

1. Install [Blender](https://www.blender.org/download/) (free) and ffmpeg.
2. Open an empty folder in Claude Code and pick the Fable 5.2 model.
3. Paste one of the prompts below. Change the text in [square brackets] to your own product or subject.
4. Let it run. It renders test frames, looks at them, names the three weakest things and fixes them, at least three times. That loop is what makes the difference.

The script it saves is a normal .blend scene, so you can open it and move the camera or swap the label.

## Prompt 01: product shot

Honey jar on a wooden table, slow arc around the product, brand name readable at the end.

````text
# A product film made in Blender by code

I will show this clip to an audience, full screen on a phone. Quality is the goal, so take the time that quality needs.

## The shot

A 7 second product shot, vertical 1080x1920, 24 frames a second, rendered with Blender Cycles.

The product: [a glass jar of honey from a small invented apiary called "Golden Hour Honey"]. Change the text in the square brackets to your own product and brand. If you have a logo file, put it in the folder and add: use logo.png on the label.

The jar stands on a worn wooden table in early morning window light. A wooden honey dipper rests beside it and a little honey has run onto the wood. The camera starts close on the label, then moves in a slow arc around the jar and ends on a hero frame with the whole product, the brand name sharp and readable. One small thing moves besides the camera, for example a slow drip from the dipper or dust in the light.

Everything comes from Python that drives Blender (bpy): the jar, the lid, the honey inside the glass, the label with its design and text, the table, the light, the camera move and the colour grade. No downloaded models. The label art is made in code too. This must look like a real photograph from a small brand's shop page: correct glass thickness, honey that glows where the light passes through it, a paper label with a slight texture, soft shadows, shallow depth of field.

## Rules

- Work only in the current folder. One script builds the whole scene and saves it as a .blend file, so I can open it later and change the camera, the colours or the label.
- Original work only. No real brand, logo or packaging design.
- Every frame must be a pure function of the frame number: keyframes, drivers and modifiers are fine, but no physics caches and no simulation that has to be played from frame 1.
- Text on the label must be spelled correctly and readable in the last frame.

## Process

1. Build a complete first version. Render three test frames at small size with few samples (start, middle, end). Open the pictures and look at them.
2. Run at least 3 improvement rounds. In each round: render test frames of different moments, look at every one, and judge them as a strict art director who compares them with the best product photography. Name the three weakest things. Fix them. Render the test frames again and check that the fix shows.
3. Keep the test frames of every round in their own folder (round1, round2 and so on) and never overwrite them.
4. When one more round would not show on a phone, or after 60 minutes, render the full clip and encode it with ffmpeg to H.264 as product.mp4.
5. Final reply, five lines or fewer: where the clip is, how many rounds you ran, the three biggest fixes, how many lines the script has, and any flaw you know of.
````

## Prompt 02: lighthouse in a storm

Night sea, a wave breaking on the rock, the lamp beam sweeping through rain.

````text
# A film shot made in Blender by code

I will show this clip to an audience, full screen on a phone. Quality is the goal, so take the time that quality needs.

## The shot

One cinematic shot, 7 seconds, vertical 1080x1920, 24 frames a second, rendered with Blender Cycles.

The subject: [a lighthouse on a rock in a storm at night]. Change the text in the square brackets to your own subject.

Heavy sea rolls in and a large wave breaks against the rock. The lamp turns, and its beam sweeps through rain and sea mist and passes across the camera once. The tower is old painted stone with a gallery and a lantern room with glass panes, and there is a small lit window half way up. The sky is dark storm cloud with a little moonlight behind it, so the shapes of the waves can be read. The camera is low over the water and pushes slowly toward the tower, with a slight roll as if it were on a boat.

Everything comes from Python that drives Blender (bpy): the tower, the rock, the sea, the spray and the rain, the mist, the sky, the lamp and its beam, the camera move and the colour grade. No downloaded models and no photographs. Aim for a frame that a viewer takes for a shot from a film: real scale, a sea surface with large swell and small detail, foam where the water meets the rock, a beam that is visible because the air is wet, and a dark picture that still shows detail in the shadows.

## Rules

- Work only in the current folder. One script builds the whole scene and saves it as a .blend file, so I can open it later and change the camera, the light or the weather.
- Original work only. No copy of a specific film, game or real lighthouse.
- Every frame must be a pure function of the frame number: keyframes, drivers and modifiers are fine (the ocean modifier with animated time is fine), but no physics caches and no simulation that has to be played from frame 1.

## Process

1. Build a complete first version. Render three test frames at small size with few samples (start, middle, end). Open the pictures and look at them.
2. Run at least 3 improvement rounds. In each round: render test frames of different moments, look at every one, and judge them as a strict art director who compares them with the best film photography of the sea. Name the three weakest things. Fix them. Render the test frames again and check that the fix shows.
3. Keep the test frames of every round in their own folder (round1, round2 and so on) and never overwrite them.
4. When one more round would not show on a phone, or after 60 minutes, render the full clip and encode it with ffmpeg to H.264 as lighthouse.mp4.
5. Final reply, five lines or fewer: where the clip is, how many rounds you ran, the three biggest fixes, how many lines the script has, and any flaw you know of.
````

## Credit

The improvement rounds idea comes from Nick Saraev's Fable 5.2 build pack. The showcase clips in the reel are by Riley Brown, Nick Saraev and Aidan Stanik.

License: MIT for the text in this repo.
