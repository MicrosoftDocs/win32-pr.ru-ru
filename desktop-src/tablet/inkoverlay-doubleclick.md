---
description: Событие InkOverlay. DoubleClick — происходит при двойном щелчке объекта InkCollector или InkOverlay.
ms.assetid: 76ea40d4-82cf-420a-a9eb-66cb0492b43b
title: Событие InkOverlay. DoubleClick (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf670c191f06e53effa0a59a078a70d7c9d096d72d2ed49a387ffa933eb7bae1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219379"
---
# <a name="inkoverlaydoubleclick-event"></a>Событие InkOverlay. DoubleClick

Происходит при двойном щелчке объекта [**InkCollector**](inkcollector-class.md) или [**InkOverlay**](inkoverlay-class.md) .

## <a name="syntax"></a>Синтаксис


```C++
void DoubleClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

Следует ли отменять событие для родительского элемента управления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ипедблкликк.

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

 

 




