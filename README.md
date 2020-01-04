ReplicatedTweening should be used when you want to use server code on a tween without having it be accompanied by the visible animation degredation casued by playing the tween from the server.

Based on [Steadyon's TweenServiceV2](https://github.com/Steadyon/TweenServiceV2).

Also available as a [library asset](https://www.roblox.com/library/4471346909/ReplicatedTweening).

# ReplicatedTweening
This is what is returned when you `require` the module.

- `ReplicatedTween ReplicatedTweening.new(Instance object, TweenInfo tweenInfo, table propertyTable)`
    - The parameters are the same as [TweenService/Create](https://developer.roblox.com/en-us/api-reference/function/TweenService/Create), returns a `ReplicatedTween` (see section ReplicatedTween)
- `ReplicatedTween ReplicatedTweening:Create(Instance object, TweenInfo tweenInfo, table propertyTable)`
    - Same as `ReplicatedTweening.new`

# ReplicatedTween

## Properties

- `Instance Instance`
    - The object being tweened
- `TweenInfo TweenInfo`
    - The TweenInfo the the tween
- `PlaybackState PlaybackState`
    - The playback state of the tween, see [the PlaybackState Enum](https://developer.roblox.com/en-us/api-reference/enum/PlaybackState)
- `table PropertyTable`
    - The table of properties to be tweened
- `string UniqueID`
    - A unique ID used to identify a specific tween

## Functions

- `ReplicatedTween:Play()`
    - Equivalent to [TweenBase/Play](https://developer.roblox.com/en-us/api-reference/function/TweenBase/Play)
- `ReplicatedTween:Pause()`
    - Equivalent to [TweenBase/Pause](https://developer.roblox.com/en-us/api-reference/function/TweenBase/Pause)
- `ReplicatedTween:Cancel()`
    - Equivalent to [TweenBase/Cancel](https://developer.roblox.com/en-us/api-reference/function/TweenBase/Cancel)
- `ReplicatedTween:Destroy()`
    - Destroys the tween

## Events

- `ReplicatedTween.Completed(PlaybackState playbackState)`
    - Equivalent to [TweenBase/Completed](https://developer.roblox.com/en-us/api-reference/event/TweenBase/Completed)
- `ReplicatedTween.PlaybackStateChanged(PlaybackState playbackState)`
    - Fires whenever the playback state of the tween changes, equivalent to `Tween:GetPropertyChangedSignal("PlaybackState")`
