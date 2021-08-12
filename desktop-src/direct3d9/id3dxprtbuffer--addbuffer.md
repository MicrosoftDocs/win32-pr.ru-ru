---
description: Добавляет еще один буфер в ID3DXPRTBuffer и сохраняет результаты в ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: 'Метод ID3DXPRTBuffer:: Аддбуффер (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffbaffbb47d91b18a6fad9bdee98012fa11fb923a7c7586acf7d7b0cd181bcc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294117"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>Метод ID3DXPRTBuffer:: Аддбуффер

Добавляет еще один буфер в [**ID3DXPRTBuffer**](id3dxprtbuffer.md) и сохраняет результаты в **ID3DXPRTBuffer**.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pBuffer* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Указатель на буфер, содержащий элементы, добавляемые в соответствующие элементы буфера [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение.

## <a name="remarks"></a>Remarks

pBuffer и [**ID3DXPRTBuffer**](id3dxprtbuffer.md) должны иметь одинаковое число выборок, коэффициентов и цветовых каналов. в противном случае метод завершится ошибкой.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




