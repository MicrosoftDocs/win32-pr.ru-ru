---
description: Применяет сохраненные данные для переплета текстуры в буфер текстуры ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'Метод ID3DXPRTBuffer:: Евалгх (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704024"
---
# <a name="id3dxprtbufferevalgh-method"></a>Метод ID3DXPRTBuffer:: Евалгх

Применяет сохраненные данные для переплета текстуры в буфер текстуры [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение.

## <a name="remarks"></a>Комментарии

Этот метод выполняет внутренний вызов [**ID3DXTextureGutterHelper:: апплигуттерсфлоат**](id3dxtexturegutterhelper--applyguttersfloat.md) для получения и применения данных для переплета текстуры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




