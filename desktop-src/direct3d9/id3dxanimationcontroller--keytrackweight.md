---
description: Задает ключ события, который изменяет вес анимированной анимации. Вес используется как множитель при объединении нескольких дорожек.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'Метод ID3DXAnimationController:: Кэйтракквеигхт (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 16bd95c675486b17f3071a279a01916e3db557c598830282f4d5b288dbc1f0fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026634"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>Метод ID3DXAnimationController:: Кэйтракквеигхт

Задает ключ события, который изменяет вес анимированной анимации. Вес используется как множитель при объединении нескольких дорожек.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор изменяемой записи.

</dd> <dt>

*Неввеигхт* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Новый вес курса.

</dd> <dt>

Время *начала* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Глобальный ключ времени. Указывает глобальное время, в которое будет происходить изменение.

</dd> <dt>

*Длительность* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Время перехода, которое указывает, как долго будет выполняться плавное преобразование.

</dd> <dt>

*Переход* \[ на окне\]
</dt> <dd>

Тип: **[ **D3DXTRANSITION \_ тип**](./d3dxtransition-type.md)**

Указывает тип перехода, используемый для перехода между весовыми коэффициентами. См. раздел [**\_ тип D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события с приоритетом события Blend. Если один или несколько входных параметров являются недопустимыми, возвращается **значение NULL** , а событие Free не доступно.

## <a name="remarks"></a>Remarks

Вес используется в качестве множителя для определения того, какую часть этой дорожки следует объединить с другими дорожками.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
