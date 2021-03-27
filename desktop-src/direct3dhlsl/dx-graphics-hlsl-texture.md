---
title: Тип текстуры
description: Используйте следующий синтаксис для объявления переменной текстуры.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Тип текстуры HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2020
ms.locfileid: "103789133"
---
# <a name="texture-type"></a>Тип текстуры

Используйте следующий синтаксис для объявления переменной текстуры.

|                |
|----------------|
| **Имя типа;** |

## <a name="parameters"></a>Параметры
| Элемент                                                                                     | Описание                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Тип**<br/> | Один из следующих типов: текстура (нетипизированный, для обеспечения обратной совместимости), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Текстурекубе. Размер элемента должен соответствовать 4 32-разрядному количеству.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**<br/> | Строка ASCII, однозначно определяющая имя переменной.<br/>                                                                                                                                                   |
## <a name="remarks"></a>Примечания

Текстура состоит из трех частей.

1.  Объявление переменной текстуры. Это делается с помощью синтаксиса, показанного выше. Например, это допустимые объявления.

    ```
    texture g_MeshTexture;
    ```

    \- или -

    ```
    Texture2D g_MeshTexture;
    ```

2.  Объявление и инициализация объекта образца. Для этого используется немного другой синтаксис в Direct3D 9 и Direct3D 10. Дополнительные сведения о синтаксисе объектов образца см. в разделе [тип образца (DirectX HLSL)](dx-graphics-hlsl-sampler.md).
3.  Вызов функции текстуры в шейдере.

Различия между Direct3D 9 и Direct3D 10:

Direct3D 9 использует [встроенные функции текстуры](dx-graphics-hlsl-intrinsic-functions.md) для выполнения операций с текстурами. Этот пример взят из [примера басичлсл](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) и использует [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) для выполнения выборки текстур.

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

Вместо этого в Direct3D 10 используются [объекты текстур с шаблонами](dx-graphics-hlsl-to-type.md) . Ниже приведен пример эквивалентной операции текстуры.

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>См. также раздел

[Типы данных (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
