---
description: Происходит при распознавании системного жеста.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: Событие InkCollector.SysТемжестуре (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282f28e5ef1bc3a86f51b6d345be6e00d78c8213
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541287"
---
# <a name="inkcollectorsystemgesture-event"></a>Событие InkCollector.SysТемжестуре

Происходит при распознавании системного жеста.

## <a name="syntax"></a>Синтаксис


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **системжестуре** .

</dd> <dt>

*Идентификатор* \[ в\]
</dt> <dd>

Значение системного жеста.

</dd> <dt>

*X* \[ в\]
</dt> <dd>

Координата по оси x расположения жеста.

</dd> <dt>

*Y* \[ в\]
</dt> <dd>

Координата по оси y расположения жеста.

</dd> <dt>

*Модификатор* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*Символ* \[ окне\]
</dt> <dd>

Зарезервировано.

</dd> <dt>

*Курсормоде* \[ окне\]
</dt> <dd>

Значение, указывающее, находится ли объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) в нормальном режиме или в режиме ластика. 1 предназначен для обычного режима, а 2 — для режима стирания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Системные жесты полезны, поскольку они предоставляют сведения об объекте [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , который используется для создания жеста. Они также предоставляют сочетания клавиш для сочетаний событий мыши и являются «более дешевыми» способами обнаружения событий мыши.

Например, вместо поиска пары событий [**MouseUp Event**](inkcollector-mouseup.md)  /  [**MouseDown**](inkcollector-mousedown.md) без других событий мыши в между ними можно найти системные жесты [**TAP**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) или **ригхттап** .

В качестве другого примера, вместо прослушивания событий [**MouseDown**](inkcollector-mousedown.md)Event  /  [**MouseMove**](inkcollector-mousemove.md) и получения многочисленных сообщений о **событиях MouseMove** , можно наблюдать за системными жестами [**перетаскивания**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) или **ригхтдраг** , если вы не заинтересованы в координатах (x, y) каждого положения мыши. Это позволяет получить только одно сообщение вместо многочисленных сообщений о **событиях MouseMove** .

Список конкретных системных жестов см. в описании типа перечисления [**инксистемжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) . Дополнительные сведения о системных жестах см. в разделе [Использование жестов](using-gestures.md) и [входных данных команды на планшетном ПК](/previous-versions//dd314533(v=vs.85)).

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицесистемжестуре.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkCollector**](inkcollector-class.md)
</dt> <dt>

[**Перечисление Инксистемжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[Использование жестов](using-gestures.md)
</dt> <dt>

[Ввод, ввод и распознавание с помощью пера](pen-input--ink--and-recognition.md)
</dt> <dt>

[Ввод команды на планшетном ПК](/previous-versions//dd314533(v=vs.85))
</dt> </dl>

 

