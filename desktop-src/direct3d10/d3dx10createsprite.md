---
description: Создайте спрайт для рисования двухмерной текстуры. Примечание. вместо использования этой функции рекомендуется использовать Direct2D и библиотеку Директкстк, класс SpriteBatch.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Функция D3DX10CreateSprite (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703713"
---
# <a name="d3dx10createsprite-function"></a>Функция D3DX10CreateSprite

Создайте спрайт для рисования двухмерной текстуры.

> [!Note]  
> Вместо использования этой функции рекомендуется использовать [Direct2D](../direct2d/direct2d-portal.md) и библиотеку [Директкстк](https://github.com/Microsoft/DirectXTK) , класс **SpriteBatch** .

 

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Указатель на устройство (см. [**интерфейс ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), который будет рисовать спрайт.

</dd> <dt>

*кдевицебуфферсизе* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Размер буфера вершин в числе спрайтов, который будет отправлен на устройство при вызове [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) или [**ID3DX10Sprite::D равспритесиммедиате**](id3dx10sprite-drawspritesimmediate.md) . Это должно быть небольшое число, если известно, что вы будете отображать небольшое количество спрайтов за раз (чтобы сэкономить память) и большое число, если известно, что в каждый момент времени будет отображено большое количество спрайтов. Максимальное значение — 4096. Если задано значение 0, размер буфера вершин будет автоматически установлен в 4096.

</dd> <dt>

*ппсприте* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Адрес указателя на интерфейс Sprite (см. [**интерфейс ID3DX10Sprite**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции общего назначения](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
