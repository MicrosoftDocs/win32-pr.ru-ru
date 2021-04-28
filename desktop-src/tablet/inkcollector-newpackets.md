---
description: Событие InkCollector. Невпаккетс — возникает, когда сборщик рукописных данных получает пакет.
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: Событие InkCollector. Невпаккетс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bab9d13dd2f33689700ef4a9aee2ed5059403e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110122"
---
# <a name="inkcollectornewpackets-event"></a>Событие InkCollector. Невпаккетс

Происходит, когда сборщик рукописных данных получает пакет.

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

При возврате из этого метода содержит массив, который содержит выбранные данные для пакета.

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Пакеты получаются, пока выполняется сбор рукописных фрагментов. События пакетов происходят быстро, а обработчик событий **невпаккетс** должен быть быстрым или отрицательным.

Метод события TЭтот определен в \_ интерфейсах иинкколлекторевентс, \_ иинковерлайевентс и \_ иинкпиктуривентс (DISP) с идентификатором DISPID \_ иценевпаккетс.

Это событие следует использовать осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода.

Чтобы задать, какие свойства содержатся в этом массиве, используйте свойство [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) объекта сборщика рукописных данных. Массив, возвращаемый параметром *паккетдата* , содержит данные для этих свойств.

> [!Note]  
> Хотя можно изменять данные пакета, эти изменения не сохраняются и не используются.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Событие Невинаирпаккетс**](inkcollector-newinairpackets.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




