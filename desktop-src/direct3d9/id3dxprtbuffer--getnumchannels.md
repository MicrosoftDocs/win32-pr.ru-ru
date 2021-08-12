---
description: 'Метод ID3DXPRTBuffer:: Жетнумчаннелс — получает количество цветовых каналов, используемых в памяти для хранения образцов.'
ms.assetid: dd1e3590-78e1-41a2-9f15-79389d9a210a
title: 'Метод ID3DXPRTBuffer:: Жетнумчаннелс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a86bac0a827839180cf746f762c39c583e64a4f80c4ebeac1d4e5e936ca69c51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294107"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a>Метод ID3DXPRTBuffer:: Жетнумчаннелс

Возвращает количество цветовых каналов, используемых в памяти для хранения образцов.

## <a name="syntax"></a>Синтаксис


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Возвращает количество цветовых каналов, используемых в памяти для хранения образцов. Обычно значение равно 1, чтобы представить значения светимости, или 3 для представления значений RGB.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
