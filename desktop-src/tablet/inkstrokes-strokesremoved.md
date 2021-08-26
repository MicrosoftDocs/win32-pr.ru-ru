---
description: Происходит при удалении одного или нескольких штрихов из коллекции Инкстрокес.
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: Событие Инкстрокес. Строкесремовед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69a5c4f7d53f88c50efd77e537cfa311f08ab168abdb4a05392286fb6c0b6b4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934864"
---
# <a name="inkstrokesstrokesremoved-event"></a>Инкстрокес. Строкесремовед, событие

Происходит при удалении одного или нескольких штрихов из коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

## <a name="syntax"></a>Синтаксис


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Строкеидс* \[ окне\]
</dt> <dd>

Целочисленный массив идентификаторов для каждого объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , удаляемого при возникновении этого события.

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ интерфейсе иинкевентс. \_Интерфейс иинкевентс реализует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ сестрокесремовед.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коллекция Инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> <dt>

[**Удалить метод \[ Инкстрокес Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)
</dt> <dt>

[**Класс Инкдисп**](inkdisp-class.md)
</dt> </dl>

 

