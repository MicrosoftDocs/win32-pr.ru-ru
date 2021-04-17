---
description: Происходит при распознавании жеста конкретного приложения.
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: Событие InkCollector. жест (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb68add1a3fbba5781624f1df98c3a637745b95a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701459"
---
# <a name="inkcollectorgesture-event"></a>Событие InkCollector. жест

Происходит при распознавании жеста конкретного приложения.

## <a name="syntax"></a>Синтаксис


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **жеста** .

</dd> <dt>

*Штрихи* \[ окне\]
</dt> <dd>

Коллекция [иинкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которую распознаватель вернул в качестве жеста.

</dd> <dt>

*Жесты* \[ окне\]
</dt> <dd>

Массив объектов [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) (в порядке уверенности) от распознавателя.

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

**Вариант \_ Значение TRUE** , если этот жест следует отменить; в противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицежестуре.

Если свойство [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) имеет значение [**жестуреонли**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), время ожидания между добавлением пользователем жеста и событием **жеста** является фиксированным значением, которое нельзя изменить программными средствами. Распознавание жестов выполняется быстрее в режиме **инканджестуре** .

Чтобы предотвратить сбор рукописных данных в режиме [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :

-   Задайте для [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) значение [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Удалите штрих в событии [**Stroke**](inkcollector-stroke.md) .
-   Обработка жеста в событии **жеста** .

Чтобы предотвратить поток рукописного ввода во время жестуринг, задайте для свойства [**Динамикрендеринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) **значение false**.

В дополнение к вставке рукописного ввода событие **жеста** срабатывает в режиме выборки или стирания. Вы несете ответственность за отслеживание режима редактирования и должны знать режим перед интерпретацией события.

> [!Note]  
> Для распознавания жестов необходимо использовать объект или элемент управления, который может выполнять накопление рукописного ввода.

 

Жесты приложения определяются как жесты, поддерживаемые в приложении.

Чтобы это событие произошло, объект или элемент управления должен представлять интерес в наборе жестов приложения. Чтобы задать объекты или элементы управления, представляющие интерес в наборе жестов, вызовите метод [**сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) объекта или элемента управления.

Список специальных жестов приложения см. в описании типа перечисления [**инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

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

[**Перечисление Инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Метод Сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[Использование жестов](using-gestures.md)
</dt> </dl>

 

