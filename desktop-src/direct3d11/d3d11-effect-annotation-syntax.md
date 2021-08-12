---
title: Синтаксис аннотации (Direct3D 11)
description: Заметка — это определяемая пользователем часть данных, объявленная с синтаксисом, описанным в этом разделе.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1109695f6239708e8f241b796b888b8d494acd7ab806b98c08352dbe3aeaee3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538568"
---
# <a name="annotation-syntax-direct3d-11"></a>Синтаксис аннотации (Direct3D 11)

Заметка — это определяемая пользователем часть данных, объявленная с синтаксисом, описанным в этом разделе.



| <Значение имени *типа данных*   =  ; *...* ; > |
|----------------------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                                   | Описание                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Заданий*<br/> | \[в \] типе данных, который включает любой [скалярный тип HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , а также [строковый тип](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Безымян*<br/>                 | \[в \] строке ASCII, представляющей имя заметки.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Значений*<br/>             | \[в \] начальном значении заметки.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[в \] дополнительных аннотациях (пар "имя-значение").<br/>                                                                                                                     |



 

## <a name="remarks"></a>Remarks

В угловые скобки можно добавить несколько аннотаций, каждое из которых отделяется точкой с запятой. Интерфейсы API платформы эффектов распознавать заметки в глобальных переменных. все остальные заметки игнорируются.

## <a name="example"></a>Пример

Рассмотрим некоторые примеры.


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Формат эффектов](d3d11-effect-format.md)
</dt> <dt>

[Синтаксис переменной Effect](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

