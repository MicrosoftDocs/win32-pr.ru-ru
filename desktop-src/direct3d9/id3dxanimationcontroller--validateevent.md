---
description: Проверяет, является ли указанный обработчик событий допустимым, а событие анимации еще не завершено.
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'Метод ID3DXAnimationController:: ValidateEvent (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647895"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a>Метод ID3DXAnimationController:: ValidateEvent

Проверяет, является ли указанный обработчик событий допустимым, а событие анимации еще не завершено.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Хевент* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик события анимации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает значение \_ ОК, если маркер события является допустимым и событие еще не завершено.

Возвращает значение E \_ Fail, если недопустимый маркер события и (или) событие завершено.

## <a name="remarks"></a>Комментарии

Метод будет указывать, что обработчик событий допустим, даже если событие выполняется, но еще не завершено.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




