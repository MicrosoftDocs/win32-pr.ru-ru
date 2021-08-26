---
title: Синтаксис группы эффектов (Direct3D 11)
description: Группа эффектов объявляется с использованием синтаксиса, описанного в этом разделе.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1b2c72b0a67a31911a0f2c9f9ae6ac0e9e20463a850c303dab4a208401d1c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069754"
---
# <a name="effect-group-syntax-direct3d-11"></a>Синтаксис группы эффектов (Direct3D 11)

Группа эффектов объявляется с использованием синтаксиса, описанного в этом разделе.


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



## <a name="parameters"></a>Параметры



| Элемент                                                                                                                                                                           | Описание                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fxgroup"></span><span id="FXGROUP"></span>фксграуп<br/>                                                                                                         | ключевое слово мые.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>Группа<br/>                                                                       | Обязательный. Строка ASCII, однозначно определяющая имя группы эффектов. В отличие от методов, группы должны иметь имена, чтобы гарантировать, что методы имеют уникальный идентификатор (см. раздел группы и методики ниже).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < аннотации ><br/> | \[\]необязательно. Один или несколько фрагментов предоставленных пользователем данных (метаданных), которые игнорируются системой эффектов. Синтаксис см. в разделе синтаксис аннотации (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>течникуеверсион<br/>                                           | Либо "technique10", либо "technique11". Методы, которые используют новые возможности Direct3D 11 ( \_ биндинтерфацес шейдеров и т. д.), должны использовать "technique11".<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>течникуенаме<br/>                                                       | Необязательный элемент. Строка ASCII, однозначно определяющая имя метода воздействия. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Группы и методики

Чтобы обеспечить совместимость с \_ эффектами FX 4 \_ 0, группы являются необязательными. Существует неявная группа с именем NULL, окружающая все глобальные методы.

Рассмотрим следующий пример.


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



В C++ один способ можно получить по имени двумя способами. Следующие команды найдут очевидные методы:


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



Чтобы гарантировать, что [**ID3DX11Effect:: жеттечникуебинаме**](id3dx11effect-gettechniquebyname.md) работает аналогично результатам 10, все определенные группы должны иметь имя.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Формат эффектов](d3d11-effect-format.md)
</dt> <dt>

[Синтаксис методики влияния (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





