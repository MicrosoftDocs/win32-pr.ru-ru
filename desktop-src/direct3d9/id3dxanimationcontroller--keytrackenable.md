---
description: Задает ключ события, который включает или отключает запись анимации.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'Метод ID3DXAnimationController:: Кэйтраккенабле (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354253"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a>Метод ID3DXAnimationController:: Кэйтраккенабле

Задает ключ события, который включает или отключает запись анимации.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор изменяемой анимации.

</dd> <dt>

*Невенабле* \[ окне\]
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Включить флаг. Задайте значение **true** , чтобы включить анимацию анимации, или **значение false** , чтобы отключить эту запись.

</dd> <dt>

Время *начала* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Глобальный ключ времени. Указывает глобальное время, в которое будет происходить изменение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события с приоритетом события Blend. Если трассировка недопустима, возвращается **значение NULL** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
