---
description: Происходит перед перерисовкой элемента управления InkPicture.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Событие InkPicture. Painting (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129e5f74ee8097794112b70fb709ab9b9a3b8fadc9f3e5a2fd7d874c65c0d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966973"
---
# <a name="inkpicturepainting-event"></a>Событие InkPicture. Paint

Происходит перед перерисовкой элемента управления [InkPicture](inkpicture-control-reference.md) .

## <a name="syntax"></a>Синтаксис


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HDC* \[ окне\]
</dt> <dd>

Контекст устройства, на котором будет происходить рисование.

</dd> <dt>

*Rect* \[ окне\]
</dt> <dd>

Прямоугольник рукописного ввода, который необходимо перерисовать.

</dd> <dt>

*Разрешить* \[ в, out\]
</dt> <dd>

Будет ли происходить перерисовка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоепаинтинг.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




