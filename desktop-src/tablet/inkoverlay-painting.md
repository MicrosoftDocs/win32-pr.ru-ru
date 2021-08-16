---
description: Происходит до завершения перерисовки объекта InkOverlay или InkPicture.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Событие InkOverlay. Painting (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42075f6ae8641c895611196b80a904228cc27c45e5d84bdc798b5cc9242e7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218946"
---
# <a name="inkoverlaypainting-event"></a>Событие InkOverlay. Paint

Происходит до завершения перерисовки объекта [**InkOverlay**](inkoverlay-class.md) или [InkPicture](inkpicture-control-reference.md) .

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

Прямоугольник, который необходимо перерисовать.

</dd> <dt>

*Разрешить* \[ в, out\]
</dt> <dd>

Будет ли происходить перерисовка.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоепаинтинг.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> </dl>

 

 




