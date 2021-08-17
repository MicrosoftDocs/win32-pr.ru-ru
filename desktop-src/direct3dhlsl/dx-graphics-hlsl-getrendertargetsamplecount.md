---
title: жетрендертаржетсамплекаунт
description: Возвращает число выборок для целевого объекта прорисовки.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- Жетрендертаржетсамплекаунт HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54414d7af326c1a069585f9d5deaa3e728d421a65490c5b9f5322b98e06f531e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120138"
---
# <a name="getrendertargetsamplecount"></a>жетрендертаржетсамплекаунт

Возвращает число выборок для целевого объекта прорисовки.



| *Uint* Жетрендертаржетсамплекаунт () |
|-------------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                                                 | Описание |
|--------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>None<br/> |             |



 

## <a name="return-value"></a>Возвращаемое значение

Число выборок.

## <a name="remarks"></a>Remarks

Используйте эту функцию и [**жетрендертаржетсамплепоситион**](dx-graphics-hlsl-getrendertargetsampleposition.md) , чтобы узнать число и положение местоположений выборки для целевого объекта прорисовки.

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

 

 





