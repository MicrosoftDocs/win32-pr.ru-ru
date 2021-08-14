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
ms.openlocfilehash: 8a406fcbd023d0688baf51cabbfea53438f3d58a6fba4d1fc7d1bf8d33077262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514338"
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
| [Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров | Да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Нет        |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





