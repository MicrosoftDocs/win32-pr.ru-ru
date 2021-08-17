---
description: Событие InkPicture. жеста — происходит при распознавании жеста конкретного приложения.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Событие InkPicture. жест (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18c0307397fc5a197666894d40adce6f4a579e22d896df8df645b053580ee94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451071"
---
# <a name="inkpicturegesture-event"></a>Событие InkPicture. жест

Происходит при распознавании *жеста* конкретного приложения.

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

**Вариант \_ Значение TRUE** , если это событие должно быть отменено, например не стереть рукописные данные и инициировать событие [**Stroke**](inkpicture-stroke.md) . В противном случае — **\_ значение false**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ ицежестуре.

Если свойство [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) имеет значение [**жестуреонли**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), время ожидания между добавлением пользователем жеста и событием **жеста** является фиксированным значением, которое нельзя изменить программными средствами. Распознавание жестов выполняется быстрее в режиме **инканджестуре** .

Чтобы предотвратить сбор рукописных данных в режиме [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :

-   Задайте для [**режиме CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) значение [**инканджестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).
-   Удалите штрих в событии [**Stroke**](inkpicture-stroke.md) .
-   Обработка жеста в событии **жеста** .

Чтобы предотвратить поток рукописного ввода во время жестуринг, задайте для свойства [**Динамикрендеринг**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) **значение false**.

В дополнение к вставке рукописного ввода событие **жеста** срабатывает в режиме выборки или стирания. Вы несете ответственность за отслеживание режима редактирования и должны знать режим перед интерпретацией события.

> [!Note]  
> Для распознавания жестов необходимо использовать объект или элемент управления, который может выполнять накопление рукописного ввода.

 

Жесты приложения определяются как жесты, поддерживаемые в приложении.

Чтобы это событие произошло, объект или элемент управления должен представлять интерес в наборе жестов приложения. Чтобы задать объекты или элементы управления, представляющие интерес в наборе жестов, вызовите метод [**сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) объекта или элемента управления.

Список специальных жестов приложения см. в описании типа перечисления [**инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> <dt>

[**Перечисление Инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**Метод Сетжестурестатус**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[Использование жестов](using-gestures.md)
</dt> </dl>

 

