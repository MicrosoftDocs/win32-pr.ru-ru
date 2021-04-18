---
description: Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных ID3DXPRTCompBuffer и добавляет их в объект ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'Метод ID3DXPRTCompBuffer:: Екстракттомеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703689"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>Метод ID3DXPRTCompBuffer:: Екстракттомеш

Извлекает коэффициенты проекции на основе анализа основных компонентов (PCA) из буфера сжатых данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) и добавляет их в объект [**ID3DXMesh**](id3dxmesh.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нумпка* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество коэффициентов PCA для извлечения из буфера.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Описание использования вершин сетки. См. [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*Усажеиндексстарт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Начальный индекс для коэффициентов PCA должен храниться в сетке.

</dd> <dt>

*псцене* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на объект сетки [**ID3DXMesh**](id3dxmesh.md) , в котором будут храниться коэффициенты PCA.

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

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
