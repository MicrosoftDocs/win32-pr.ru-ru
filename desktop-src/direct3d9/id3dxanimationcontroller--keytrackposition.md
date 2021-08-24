---
description: Задает ключ события, который изменяет местное время анимации.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'Метод ID3DXAnimationController:: Кэйтраккпоситион (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9e66bac7b5aaa8da87b0cb88e3bfd12469d8aa8b6ec755eaa47268c70da5eadf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791234"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>Метод ID3DXAnimationController:: Кэйтраккпоситион

Задает ключ события, который изменяет местное время анимации.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор изменяемой записи.

</dd> <dt>

*Невпоситион* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Новое местное время в дорожке анимации.

</dd> <dt>

Время *начала* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Глобальный ключ времени. Указывает глобальное время, в которое будет происходить изменение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события с приоритетом события Blend. **Значение NULL** возвращается, если трассировка недопустима, или если событие Free недоступно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
