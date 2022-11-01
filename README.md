## Getting Started

Inside of Unreal go to Tools.

Select New C++ Class.

Select Actor.

Rename the actor (MovingPlatform).

Press Create Class.

Close UE Editor.

Open VS Code.

<a name="compiling-the-editor"></a>
## Compiling The Editor

Inside VS Code Select Terminal.

Run Build Task (Ctrl + Shift + B).

Select [Project Name + Win64 Development Build].

Wait for Terminal to finish compiling.

Reopen UE Editor.

Drag C++ Actor (MovingPlatform) on to scene.

Inside VS Code under MovingPlatform.h add: 

``` C
// Fill out your copyright notice in the Description page of Project Settings.

#pragma once

#include "CoreMinimal.h"
#include "GameFramework/Actor.h"
#include "MovingPlatform.generated.h"

UCLASS()
class UNREALLEARNINGKIT_API AMovingPlatform : public AActor
{
	GENERATED_BODY()
	
public:	
	// Sets default values for this actor's properties
	AMovingPlatform();

protected:
	// Called when the game starts or when spawned
	virtual void BeginPlay() override;

public:	
	// Called every frame
	virtual void Tick(float DeltaTime) override;

	UPROPERTY(EditAnywhere)
	int32 MyInt = 99;

	UPROPERTY(EditAnywhere)
	float MyFloat = 1;

	UPROPERTY(EditAnywhere)
	bool MyBool = true;

};

```
Save the script.

Inside of UE, bottom right, press Live Coding.

Wait for recompile.

Check on the actor's Detail panel to see if the variables are added onto MyFirstActor.

## Common Issues with Live Coding

Data is lost when reloading project.

Close UE Editor.

Repeat <a href="#compiling-the-editor">Compiling The Editor</a>
