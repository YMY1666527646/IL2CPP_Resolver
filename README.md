## IL2CPP Resolver
A run-time API resolver for IL2CPP Unity.

### Quick Example
```cpp
#include "Main.hpp"

void SomeFunction()
{
    IL2CPP::Initialize(); // This needs to be called once!

    Unity::CGameObject* pLocal = Unity::GameObject::Find("LocalPlayer");
    Unity::CComponent* pLocalData = pLocal->GetComponent("PlayerData");
    pLocalData->SetMemberValue<bool>("CanFly", true);
}
```

### Creating Thread
```cpp
void ThreadStart()
{ 
    // Stuff ... Loop ... Smth
}

void ThreadEnd()
{
    // Called after ThreadStart
}

IL2CPP::Thread::Create(ThreadStart, ThreadEnd);
```