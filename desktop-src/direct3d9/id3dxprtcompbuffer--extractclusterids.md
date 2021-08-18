---
description: Извлекает идентификаторы кластеров по образцу из сжатого буфера данных ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'Метод ID3DXPRTCompBuffer:: Екстрактклустеридс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94cbf51aaedd8cc0d5505ca91663eb014e2a3d417a631e93d71b8a0ebc600ceb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987184"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a>Метод ID3DXPRTCompBuffer:: Екстрактклустеридс

Извлекает идентификаторы кластеров по образцу из сжатого буфера данных [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклустеридс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на расположение в памяти, где записываются идентификаторы. Требуемая длина памяти — это значение, возвращаемое функцией [**ID3DXPRTCompBuffer:: жетнумсамплес**](id3dxprtcompbuffer--getnumsamples.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
