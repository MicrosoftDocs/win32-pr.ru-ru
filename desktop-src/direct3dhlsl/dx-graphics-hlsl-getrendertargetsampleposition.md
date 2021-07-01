---
title: жетрендертаржетсамплепоситион
description: Возвращает позиции выборки (x, y) для данного образца индекса.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- Жетрендертаржетсамплепоситион HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120579"
---
# <a name="getrendertargetsampleposition"></a>жетрендертаржетсамплепоситион

Возвращает позиции выборки (x, y) для данного образца индекса.

float<2> Жетрендертаржетсамплепоситион (в int<1> индекс<br/>);



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                       | Описание                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Номер*<br/> | \[в \] индексе выборки с отсчетом от нуля.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Координата (x, y) данного образца.

## <a name="remarks"></a>Remarks

Используйте эту функцию и [**жетрендертаржетсамплекаунт**](dx-graphics-hlsl-getrendertargetsamplecount.md) , чтобы узнать число и положение местоположений выборки для целевого объекта прорисовки.

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров | yes       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Нет        |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





