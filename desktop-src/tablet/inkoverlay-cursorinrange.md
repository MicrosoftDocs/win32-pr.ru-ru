---
description: Событие InkOverlay. Курсоринранже возникает, когда курсор попадает в диапазон физического обнаружения (близость) контекста планшета.
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Событие InkOverlay. Курсоринранже (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94bcf773a3fcb0b23d26912b6b338c1741c0d9d3e5bded84759cafc1f15506c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220767"
---
# <a name="inkoverlaycursorinrange-event"></a>Событие InkOverlay. Курсоринранже

Происходит при входе курсора в диапазон физического обнаружения (близость) контекста планшета.

## <a name="syntax"></a>Синтаксис


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Курсор* \[ окне\]
</dt> <dd>

Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**курсоринранже**](inkcollector-cursorinrange.md) .

</dd> <dt>

*Невкурсор* \[ окне\]
</dt> <dd>

Будет ли этот сборщик рукописных данных впервые подключен к объекту [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавшему событие [**курсоринранже**](inkcollector-cursorinrange.md) .

</dd> <dt>

*Буттонсстате* \[ окне\]
</dt> <dd>

Состояние кнопок для курсора, создавшего событие [**курсоринранже**](inkcollector-cursorinrange.md) .

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ ицекурсоринранже.

Событие [**курсоринранже**](inkcollector-cursorinrange.md) срабатывает даже в режиме выбора или стирания, а не только в режиме рукописного ввода. Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие. Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.

## <a name="requirements"></a>Requirements (Требования)



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

[**Событие Курсораутофранже**](inkcollector-cursoroutofrange.md)
</dt> <dt>

[**Перечисление Инккурсорбуттонстате**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[**Интерфейс Иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




