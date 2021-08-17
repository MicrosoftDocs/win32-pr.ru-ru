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
ms.openlocfilehash: 24c5195d38aeaebefd1713df31f23b6b2ec7b2324a31381027f3442b541678c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094181"
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

## <a name="remarks"></a>Remarks

Метод будет указывать, что обработчик событий допустим, даже если событие выполняется, но еще не завершено.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




