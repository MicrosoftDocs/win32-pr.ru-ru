---
description: Копирует значения албедо на уровне вершины из сетки.
ms.assetid: 3a6f1cc2-a870-4463-98df-599d9fbd9d78
title: 'Метод ID3DXPRTEngine:: Екстрактпервертексалбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ExtractPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e094a7681c13e21cdaab71648b3733749fc179f845e23496a07f3c2b7b99234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747754"
---
# <a name="id3dxprtengineextractpervertexalbedo-method"></a>Метод ID3DXPRTEngine:: Екстрактпервертексалбедо

Копирует значения албедо на уровне вершины из сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExtractPerVertexAlbedo(
  [in] LPD3DXMESH   pMesh,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         NumChanIn
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на объект сетки [**ID3DXMesh**](id3dxmesh.md) , используемый в [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) для создания объекта [**ID3DXPRTEngine**](id3dxprtengine.md) .

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Описания использования вершин для копирования из сетки. См. [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*Нумчанин* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число цветовых каналов для копирования из сетки. Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
