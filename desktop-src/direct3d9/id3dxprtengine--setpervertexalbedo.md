---
description: Задает значение албедо для каждой вершины сетки, перезаписывая предыдущие значения албедо.
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'Метод ID3DXPRTEngine:: Сетпервертексалбедо (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647855"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a>Метод ID3DXPRTEngine:: Сетпервертексалбедо

Задает значение албедо для каждой вершины сетки, перезаписывая предыдущие значения албедо.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **константа \* void**

Указатель на данные типа FLOAT албедо первого образца.

</dd> <dt>

*Нумчаннелс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число устанавливаемых цветовых каналов. Задайте значение 1, чтобы указать серые материалы (R = G = B), или 3, чтобы включить эффекты цвета суперсовременные.

</dd> <dt>

*Шаг с шагом* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Шаг в байтах, необходимый для перехода к значению албедо следующей выборки. См. раздел [Ширина и шаг (Direct3D 9)](width-vs--pitch.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
