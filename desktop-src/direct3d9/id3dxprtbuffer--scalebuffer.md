---
description: Умножает каждое значение в буфере на постоянное значение.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'Метод ID3DXPRTBuffer:: Скалебуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5cba39f6816e301f2d36e21e6f81c7bb1f6bb4792fe4ea8017de5d452faf357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118801492"
---
# <a name="id3dxprtbufferscalebuffer-method"></a>Метод ID3DXPRTBuffer:: Скалебуффер

Умножает каждое значение в буфере на постоянное значение.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Масштаб* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Постоянное значение, используемое для масштабирования буфера. Каждое значение в буфере заменяется произведением этого значения и исходного значения буфера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
