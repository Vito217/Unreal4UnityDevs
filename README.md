# The Unreal Guide for Unity devs

A Unreal Engine guide for Unity developers. I'm slowly learning Unreal, so please, tell me if some information is wrong.

| Unity class/method/property | Unreal equivalent | Description | Differences |
--- | --- | --- | ---
| Behaviour.enabled | PrimaryActorTick.bCanEverTick | If true, the object can call Update/Tick every frame | |
| CharacterController | APlayerController | |
| GameObject.AddComponent("Component") | #include "ComponentGroup/Component.h" | Adds a component class to the object/actor. | In C++, ComponentGroup is similar to "using ComponentGroup" and then calling the Component class (or rather ComponentGroup.Component) in C#. |
| GameObject.GetComponent("Desired") | AActorChildClass::GetDesiredComponent() | Returns the desired component | |
| GameOBject.tag | UPTOPERTY(Category = "tagName") | |
| [HideInInspector] | UPROPERTY(VisibleAnywhere) | While opposites, both serve as annotations for hiding/showing properties in the inspector/editor | |
| MonoBehaviour | AActor | Both represent an object | The AActor object has a UCLASS() annotation. |
| MonoBehaviour.Awake() | AActorObject::AActorObject() | Used to initialize properties before Play | While Awake is commonly used in Unity, Unreal uses constructors. |
| MonoBehaviour.Start() | AActor::BeginPlay() | Called when Play happens | |
| MonoBehaviour.Update() | AActor::Tick(float DeltaTime) | Called every frame on the MonoBehaviour/Actor object | |
| Physics.Raycast(Vector3 origin, Vector3 direction, out RaycastHit hit, float maxDistance, int layerMask, QueryTriggerInteraction qti) | UWorld::LineTraceSingleByChannel(FHitResult hit, FVector origin, FVector end, ECollisionChannel ch, ECollisionQueryParams params) | |
| Quaternion.Euler | FRotator | |
| RaycastHit.Coliider.gameObject | FHitRestult.Actor | The object/actor that was hit. |
| RaycastResult | FHitResult | |
| Transform.forward | FRotator.Vector() | |
| Vector3 | FVector | |
| Vector3.zero| FVector::ZeroVector | |
