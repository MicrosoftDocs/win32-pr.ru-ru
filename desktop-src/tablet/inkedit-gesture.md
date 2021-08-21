---
description: Происходит при распознавании жеста приложения.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Событие InkEdit. жеста (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a718106f4485682a1b6267f942ec3ef0f5a9fb670449e1f6023d86a5b03af56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032082"
---
# <a name="inkeditgesture-event"></a>Событие InkEdit. жест

Происходит при распознавании жеста приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Gesture(
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

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , который использовался для создания этого жеста.

</dd> <dt>

*Штрихи* \[ окне\]
</dt> <dd>

Коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , содержащая объекты [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , которые составляют этот жест.

</dd> <dt>

*Жесты* \[ окне\]
</dt> <dd>

Массив объектов [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) в порядке уверенности.

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

Следует ли отменять коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , составляющую этот жест, и не стирать рукописные данные и вызывать событие [**Stroke**](inkedit-stroke.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это событие завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс IDispatch с идентификатором DISPID \_ иижестуре.

Событие **жеста** создается только в том случае, если [**Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) для объекта [**иинкжестуре**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) является первым объектом **иинкстрокедисп** с момента последнего вызова метода [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) или последнего срабатывания времени ожидания распознавания.

Если событие **жеста** отменено, то для коллекции [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , вызвавшей событие **жеста** , возникает событие [**Stroke**](inkedit-stroke.md) .

Чтобы это событие произошло, элемент управления [InkEdit](inkedit-control-reference.md) должен подписываться на набор жестов приложения. Чтобы задать интерес к элементу управления InkEdit в наборе жестов, вызовите метод [**сетжестурестатус**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .

Список жестов приложений см. в описании типа перечисления [**инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .

Элемент управления [InkEdit](inkedit-control-reference.md) не распознает несколько жестов росчерка.

Элемент управления [InkEdit](inkedit-control-reference.md) подписывается на следующие жесты.



| жесты                              | Действие               |
|--------------------------------------|----------------------|
| Вниз, вниз, слева направо<br/> | ВВОД<br/>     |
| Правый<br/>                     | Пробел<br/>     |
| Левый<br/>                      | Отмена<br/> |
| Вверх, справа, справа надолго<br/>   | Вкладка<br/>       |



 

Чтобы изменить действие по умолчанию для жеста, выполните следующие действия.

1.  Добавьте обработчики событий для **жестов** и событий [**Stroke**](inkedit-stroke.md) .
2.  В обработчике событий **жеста** отмените событие **жеста** для жеста и выполните альтернативное действие для жеста.
3.  В обработчике событий [**Stroke**](inkedit-stroke.md) отмените событие **Stroke** для объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , вызвавшего отмененное событие **жеста** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>«С». h (также требует \_ ввода i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Перечисление Инкаппликатионжестуре**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[**\[Элемент управления InkEdit метода сетжестурестатус\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)
</dt> <dt>

[**Рекотимеаут, свойство**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

[**\[Элемент управления InkEdit для события Stroke\]**](inkedit-stroke.md)
</dt> <dt>

[Использование жестов](using-gestures.md)
</dt> </dl>

 

