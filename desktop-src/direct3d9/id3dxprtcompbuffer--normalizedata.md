---
description: Нормализует все весовые коэффициенты для анализа основных компонентов (PCA), чтобы они были в диапазоне от-1 до 1. Векторы базиса изменяются для отражения этой нормализации.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'Метод ID3DXPRTCompBuffer:: Нормализедата (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713933"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a>Метод ID3DXPRTCompBuffer:: Нормализедата

Нормализует все весовые коэффициенты для анализа основных компонентов (PCA), чтобы они были в диапазоне от-1 до 1. Векторы базиса изменяются для отражения этой нормализации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




