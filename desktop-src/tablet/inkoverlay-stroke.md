---
description: Событие InkOverlay. Stroke — происходит, когда пользователь рисует новый штрих на любом планшете.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Событие InkOverlay. Stroke (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2836699591b4f1a87ce3d206a795eb13be188def28ea3eadef687a1d96024ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712634"
---
# <a name="inkoverlaystroke-event"></a>Событие InkOverlay. Stroke

Происходит, когда пользователь рисует новый штрих на любом планшете.

## <a name="syntax"></a>Синтаксис


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**Stroke**](inkcollector-stroke.md) .

</dd> <dt>

*Штриховая линия* \[ окне\]
</dt> <dd>

Собранный объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*Отмена* \[ в, out\]
</dt> <dd>

Указывает, следует ли отменять событие. Если **значение — true**, коллекция штрихов отменяется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицестроке.

Событие [**Stroke**](inkcollector-stroke.md) срабатывает в режиме выборки или стирания, а не только при вставке рукописного ввода. Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и знать о режиме, прежде чем интерпретировать событие. Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.

> [!Note]  
> Событие [**Stroke**](inkcollector-stroke.md) срабатывает, когда пользователь завершает рисование штриха, а не при добавлении штриха в коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Когда пользователь впервые начинает рисовать штрих, он сразу же добавляется в коллекцию Инкстрокес; Однако событие **Stroke** не срабатывает до завершения штриха. Таким образом, штрихи могут существовать в коллекции Инкстрокес, которая не видна обработчику событий **Stroke** .

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс InkOverlay**](inkoverlay-class.md)
</dt> <dt>

[**\[Коллекция Инкстрокес событий строкесаддед\]**](inkstrokes-strokesadded.md)
</dt> <dt>

[**\[Класс InkOverlay события строкесделетед\]**](inkoverlay-strokesdeleted.md)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**Интерфейс Иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

