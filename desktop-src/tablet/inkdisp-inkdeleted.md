---
description: Происходит при удалении штриха из объекта Инкдисп.
ms.assetid: 59ada470-6620-411d-889e-882f41ccea3e
title: Событие Инкдисп. Инкделетед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9022b34b128f92530761a0093b2e7c1823dd88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682522"
---
# <a name="inkdispinkdeleted-event"></a>Инкдисп. Инкделетед, событие

Происходит при удалении штриха из объекта [**инкдисп**](inkdisp-class.md) .

## <a name="syntax"></a>Синтаксис


```C++
void InkDeleted(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Строкеидс* \[ окне\]
</dt> <dd>

Задает целочисленный массив сведений об ИДЕНТИФИКАТОРе штриха для всех штрихов, удаленных при возникновении этого события.

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Если вы используете объект [**InkOverlay**](inkoverlay-class.md) или элемент управления [InkPicture](inkpicture-control-reference.md) (где [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) равно [**Delete**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayeditingmode) и [**ерасермоде**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode) равно [**строкирасе**](/windows/desktop/api/msinkaut/ne-msinkaut-inkoverlayerasermode)) и передайте резинку по штриху, вы получаете следующую последовательность событий:

-   **инкделетед**
-   [**инкаддед**](inkdisp-inkadded.md)
-   **инкделетед**

Дополнительные события [**инкаддед**](inkdisp-inkadded.md) и **инкделетед** происходят потому, что базовый код добавляет внутренний невидимый росчерк для отслеживания ластика.

Этот метод события определен в \_ интерфейсе иинкевентс. \_Интерфейс иинкевентс реализует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иеинкделетед.

Событие **инкделетед** срабатывает даже в режиме выбора или стирания, а не только при вставке рукописного ввода. Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие. Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Инкдисп**](inkdisp-class.md)
</dt> <dt>

[**\[Класс InkOverlay свойства EditingMode\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode)
</dt> <dt>

[**\[Класс InkOverlay свойства ерасермоде\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_erasermode)
</dt> <dt>

[**Событие Инкаддед**](inkdisp-inkadded.md)
</dt> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[Справочник по элементу управления InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

