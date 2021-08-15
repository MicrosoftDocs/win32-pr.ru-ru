---
description: Масштабирует все выборки, связанные с заданной подсетью. Метод полезен для вычисления рассеивания подповерхности.
ms.assetid: abb9ca6a-5fc2-4986-8a38-29998fe5e537
title: 'Метод ID3DXPRTEngine:: Скалемешчунк (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ScaleMeshChunk
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a42046678ef0b44f011c8440cd3456dc9ff236ec0f7a280b4650b49aa53c10d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729588"
---
# <a name="id3dxprtenginescalemeshchunk-method"></a>Метод ID3DXPRTEngine:: Скалемешчунк

Масштабирует все выборки, связанные с заданной подсетью. Метод полезен для вычисления рассеивания подповерхности.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ScaleMeshChunk(
  [in]      UINT            uMeshChunk,
  [in]      FLOAT           fScale,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*умешчунк* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Расположение в сетке, с которого начинается масштабирование выборок.

</dd> <dt>

*фскале* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Значение, на которое умножается каждый вектор в подсети.

</dd> <dt>

*pData* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на объект [**ID3DXPRTBuffer**](id3dxprtbuffer.md) для получения масштабируемых образцов во вложенной сетке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
