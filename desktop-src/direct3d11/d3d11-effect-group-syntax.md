---
title: Синтаксис группы эффектов (Direct3D 11)
description: Группа эффектов объявляется с использованием синтаксиса, описанного в этом разделе.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104487185"
---
# <a name="effect-group-syntax-direct3d-11"></a><span data-ttu-id="99af4-103">Синтаксис группы эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="99af4-103">Effect Group Syntax (Direct3D 11)</span></span>

<span data-ttu-id="99af4-104">Группа эффектов объявляется с использованием синтаксиса, описанного в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="99af4-104">An effect group is declared with the syntax described in this section.</span></span>


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a><span data-ttu-id="99af4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="99af4-105">Parameters</span></span>



| <span data-ttu-id="99af4-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="99af4-106">Item</span></span>                                                                                                                                                                           | <span data-ttu-id="99af4-107">Описание</span><span class="sxs-lookup"><span data-stu-id="99af4-107">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99af4-108"><span id="fxgroup"></span><span id="FXGROUP"></span>фксграуп</span><span class="sxs-lookup"><span data-stu-id="99af4-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span></span><br/>                                                                                                         | <span data-ttu-id="99af4-109">ключевое слово мые.</span><span class="sxs-lookup"><span data-stu-id="99af4-109">equired keyword.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="99af4-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>Группа</span><span class="sxs-lookup"><span data-stu-id="99af4-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span></span><br/>                                                                       | <span data-ttu-id="99af4-111">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="99af4-111">Required.</span></span> <span data-ttu-id="99af4-112">Строка ASCII, однозначно определяющая имя группы эффектов.</span><span class="sxs-lookup"><span data-stu-id="99af4-112">An ASCII string that uniquely identifies the name of the effect group.</span></span> <span data-ttu-id="99af4-113">В отличие от методов, группы должны иметь имена, чтобы гарантировать, что методы имеют уникальный идентификатор (см. раздел группы и методики ниже).</span><span class="sxs-lookup"><span data-stu-id="99af4-113">Unlike techniques, groups must have names to ensure that techniques have a unique identifier (see Groups and Techniques section below).</span></span><br/> |
| <span data-ttu-id="99af4-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < аннотации ></span><span class="sxs-lookup"><span data-stu-id="99af4-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Annotations ></span></span><br/> | <span data-ttu-id="99af4-115">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="99af4-115">\[in\] Optional.</span></span> <span data-ttu-id="99af4-116">Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов.</span><span class="sxs-lookup"><span data-stu-id="99af4-116">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="99af4-117">Синтаксис см. в разделе синтаксис аннотации (Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="99af4-117">For syntax, see Annotation Syntax (Direct3D 11).</span></span> <br/>                                                      |
| <span data-ttu-id="99af4-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>течникуеверсион</span><span class="sxs-lookup"><span data-stu-id="99af4-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/>                                           | <span data-ttu-id="99af4-119">Либо "technique10", либо "technique11".</span><span class="sxs-lookup"><span data-stu-id="99af4-119">Either "technique10" or "technique11".</span></span> <span data-ttu-id="99af4-120">Методы, которые используют новые возможности Direct3D 11 ( \_ биндинтерфацес шейдеров и т. д.), должны использовать "technique11".</span><span class="sxs-lookup"><span data-stu-id="99af4-120">Techniques which use functionality new to Direct3D 11 (5\_0 shaders, BindInterfaces, etc) must use "technique11".</span></span><br/>                                                                 |
| <span data-ttu-id="99af4-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>течникуенаме</span><span class="sxs-lookup"><span data-stu-id="99af4-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span></span><br/>                                                       | <span data-ttu-id="99af4-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="99af4-122">Optional.</span></span> <span data-ttu-id="99af4-123">Строка ASCII, однозначно определяющая имя метода воздействия.</span><span class="sxs-lookup"><span data-stu-id="99af4-123">An ASCII string that uniquely identifies the name of the effect technique.</span></span> <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a><span data-ttu-id="99af4-124">Группы и методики</span><span class="sxs-lookup"><span data-stu-id="99af4-124">Groups and Techniques</span></span>

<span data-ttu-id="99af4-125">Чтобы обеспечить совместимость с \_ эффектами FX 4 \_ 0, группы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="99af4-125">In order to maintain compatibility with fx\_4\_0 effects, groups are optional.</span></span> <span data-ttu-id="99af4-126">Существует неявная группа с именем NULL, окружающая все глобальные методы.</span><span class="sxs-lookup"><span data-stu-id="99af4-126">There is an implicit NULL-named group surrounding all global techniques.</span></span>

<span data-ttu-id="99af4-127">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="99af4-127">Consider the following example:</span></span>


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



<span data-ttu-id="99af4-128">В C++ один способ можно получить по имени двумя способами.</span><span class="sxs-lookup"><span data-stu-id="99af4-128">In C++, one can get a technique by name in two ways.</span></span> <span data-ttu-id="99af4-129">Следующие команды найдут очевидные методы:</span><span class="sxs-lookup"><span data-stu-id="99af4-129">The following commands will find the obvious techniques:</span></span>


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



<span data-ttu-id="99af4-130">Чтобы гарантировать, что [**ID3DX11Effect:: жеттечникуебинаме**](id3dx11effect-gettechniquebyname.md) работает аналогично результатам 10, все определенные группы должны иметь имя.</span><span class="sxs-lookup"><span data-stu-id="99af4-130">In order to ensure that [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) works similarly to Effects 10, all defined groups must have a name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99af4-131">См. также</span><span class="sxs-lookup"><span data-stu-id="99af4-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99af4-132">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="99af4-132">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="99af4-133">Синтаксис методики влияния (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="99af4-133">Effect Technique Syntax (Direct3D 11)</span></span>](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





