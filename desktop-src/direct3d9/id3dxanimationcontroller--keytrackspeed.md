---
description: Задает ключ события, который изменяет частоту воспроизведения анимированной записи.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: 'Метод ID3DXAnimationController:: Кэйтраккспид (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21ad7b0b1423a25ede319a623cad0a8b453af481d4aac5fae4e5bcce252dd31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791194"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>Метод ID3DXAnimationController:: Кэйтраккспид

Задает ключ события, который изменяет частоту воспроизведения анимированной записи.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
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

*Невспид* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Новая скорость анимации.

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

Указывает тип перехода, используемый для перехода между скоростями. См. раздел [**\_ тип D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события с приоритетом события Blend. Если один или несколько входных параметров являются недопустимыми, возвращается **значение NULL** , а событие Free не доступно.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
