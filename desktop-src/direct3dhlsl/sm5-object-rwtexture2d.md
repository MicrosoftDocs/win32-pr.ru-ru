---
title: RWTexture2D
description: Ресурс, доступный для чтения и записи. | RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c015aaa8606f5d04386b7839584203c5672e4ac1bf031b89eb4c41ca69f7dd14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985934"
---
# <a name="rwtexture2d"></a>RWTexture2D

Ресурс, доступный для чтения и записи.



| Метод                                                        | Описание                   |
|---------------------------------------------------------------|-------------------------------|
| [**GetDimensions**](sm5-object-rwtexture2d-getdimensions.md) | Возвращает размеры ресурсов. |
| [**Загрузить**](rwtexture2d-load.md)                              | Считывает данные текстуры.           |
| [**Оператор\[\]**](sm5-object-rwtexture2d-operatorindex.md)  | Возвращает переменную ресурса.     |



 

Можно добавить префикс для объектов RWTexture2D с классом хранения **глобалликохерент**. Этот класс хранения вызывает барьеры памяти и выполняет синхронизацию для очистки данных во всем GPU, так что другие группы могут видеть операции записи. Без этого описателя барьер памяти или синхронизация выполнит очистку только неупорядоченного представления доступа (UAV) в текущей группе.

Для объекта RWTexture2D требуется тип элемента в операторе объявления для объекта. Например, следующее объявление является неправильным:


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



Следующее объявление верно:


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



Так как объект RWTexture2D является объектом UAV, его свойства отличаются от объекта типа представления ресурсов шейдера (SRV), такого как объект [Texture2D](sm5-object-texture2d.md) . Например, можно выполнять чтение из объекта RWTexture2D и запись в него, но можно только считывать объект Texture2D.

Объект RWTexture2D не может использовать методы из объекта [Texture2D](sm5-object-texture2d.md) , например [Sample](dx-graphics-hlsl-to-sample.md). Однако, поскольку можно создать несколько типов представлений для одного и того же ресурса, можно объявить несколько типов текстур как одну текстуру в нескольких шейдерах. Например, в следующих фрагментах кода показано, как можно объявить и использовать объект RWTexture2D как *Да* в шейдере вычислений, а затем объявить и использовать объект Texture2D как *Да* в шейдере пикселей.

> [!Note]  
> Среда выполнения применяет определенные шаблоны использования при создании нескольких типов представлений для одного и того же ресурса. Например, среда выполнения не позволяет одновременно использовать сопоставление UAV для ресурса и сопоставление SRV для одного и того же ресурса.

 

Следующий код предназначен для вычислений с шейдером:


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



Следующий код предназначен для построителя текстуры:


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Этот объект поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | Да       |



 

Этот объект поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты модели шейдеров 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




