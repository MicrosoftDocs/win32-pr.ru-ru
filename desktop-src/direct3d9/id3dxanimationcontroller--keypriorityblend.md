---
description: Задает смешение ключей событий для указанной записи анимации.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'Метод ID3DXAnimationController:: Кэйприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d2b4e18fc93dff3054a98442c86a4c05467898afe09fc3bc82ccbd2f0ba456
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279044"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>Метод ID3DXAnimationController:: Кэйприоритибленд

Задает смешение ключей событий для указанной записи анимации.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Невблендвеигхт* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Число от 0 до 1, используемое для одновременного смешения дорожек.

</dd> <dt>

Время *начала* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Глобальное время для запуска Blend.

</dd> <dt>

*Длительность* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Глобальная длительность смешения времени.

</dd> <dt>

*Переход* \[ на окне\]
</dt> <dd>

Тип: **[ **D3DXTRANSITION \_ тип**](./d3dxtransition-type.md)**

Указывает тип перехода, используемый в течение смешения. См. раздел [**\_ тип D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события с приоритетом события Blend. Если один или несколько входных параметров являются недопустимыми, возвращается **значение NULL** , а событие Free не доступно.

## <a name="remarks"></a>Remarks

Контроллер анимации смешивается в три этапа: курсы с низким приоритетом смешиваются, сначала накладываются курсы с высоким приоритетом, а затем результаты обеих моделей смешиваются.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**сетприоритибленд**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
