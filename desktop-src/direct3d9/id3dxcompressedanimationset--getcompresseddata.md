---
description: Возвращает буфер данных, в котором хранятся сжатые данные анимации с помощью ключевых кадров.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: 'Метод ID3DXCompressedAnimationSet:: Жеткомпресседдата (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7907daf5db2d03afca310a630f6aeb2dc16c4f22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674706"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a>Метод ID3DXCompressedAnimationSet:: Жеткомпресседдата

Возвращает буфер данных, в котором хранятся сжатые данные анимации с помощью ключевых кадров.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппкомпресседдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на буфер данных [**ID3DXBuffer**](id3dxbuffer.md) , который получает сжатые данные анимации по ключевым кадрам.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




