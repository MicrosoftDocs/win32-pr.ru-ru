---
description: Происходит, когда рукописный коллекто ррецеивес пакет.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: Событие InkOverlay. Невпаккетс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2571e7c8f97881da5bbbef6cdab093ce2d3107b5482def5b62d2dfa141c7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219203"
---
# <a name="inkoverlaynewpackets-event"></a>Событие InkOverlay. Невпаккетс

Происходит, когда рукописный коллекто ррецеивес пакет

## <a name="syntax"></a>Синтаксис


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**невинаирпаккетс**](inkcollector-newinairpackets.md) .

</dd> <dt>

*Штриховая линия* \[ окне\]
</dt> <dd>

Указывает объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*Паккеткаунт* \[ окне\]
</dt> <dd>

Число пакетов, полученных для объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*Паккетдата* \[ в, out\]
</dt> <dd>

Массив, содержащий выбранные данные для пакета.

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Пакеты получаются, пока выполняется сбор рукописных фрагментов. События пакетов происходят быстро, а обработчик событий [**невпаккетс**](inkcollector-newpackets.md) должен быть быстрым или отрицательным.

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ иценевпаккетс.

Это событие следует использовать осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода.

Чтобы задать, какие свойства содержатся в этом массиве, используйте свойство [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) объекта сборщика рукописных данных. Массив, возвращаемый параметром *паккетдата* , содержит данные для этих свойств.

> [!Note]  
> Хотя можно изменять данные пакета, эти изменения не сохраняются и не используются.

 

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
</dt> <dt>

[**Событие Невинаирпаккетс**](inkcollector-newinairpackets.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




