---
description: Возвращает количество цветовых каналов, используемых в памяти для хранения образцов.
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
ms.openlocfilehash: 99456c6386a822489eca6beef41f639008007778
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694338"
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
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
