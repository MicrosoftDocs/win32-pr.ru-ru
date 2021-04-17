---
description: Извлекает коэффициенты из одноканального буфера и добавляет данные в объект ID3DXMesh.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'Метод ID3DXPRTBuffer:: Екстракттомеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704023"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>Метод ID3DXPRTBuffer:: Екстракттомеш

Извлекает коэффициенты из одноканального буфера и добавляет данные в объект [**ID3DXMesh**](id3dxmesh.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*НумкоеффиЦиентс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество коэффициентов, которые необходимо извлечь из буфера. При использовании радианценого (PRT) предварительно вычисленного коэффициента просчетного гармонического (SH) число коэффективных должно быть Order ². Порядок должен находиться в диапазоне от [D3DXSH \_ МИНОРДЕР](other-d3dx-constants.md) до D3DXSH \_ максордер, включительно.

</dd> <dt>

*Использование* \[ окне\]
</dt> <dd>

Тип: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Описание использования вершин сетки. См. [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*Усажеиндексстарт* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Начальный индекс для коэффициентов хранится в сетке.

</dd> <dt>

*псцене* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на объект сетки [**ID3DXMesh**](id3dxmesh.md) , который будет хранить коэффициенты.

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

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
