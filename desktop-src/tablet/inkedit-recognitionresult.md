---
description: 'Происходит, когда элемент управления InkEdit получает результаты вручную из вызова метода InkEdit:: Recognize или автоматически после срабатывания времени ожидания распознавания.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Событие InkEdit. Рекогнитионресулт (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef71d38be31f32c59919a9ce4f24fd90b2d188d86a26e81821f6f7987da31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939084"
---
# <a name="inkeditrecognitionresult-event"></a>Событие InkEdit. Рекогнитионресулт

Происходит, когда элемент управления [InkEdit](inkedit-control-reference.md) получает результаты вручную из вызова метода [**InkEdit:: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) или автоматически после срабатывания времени ожидания распознавания.

## <a name="syntax"></a>Синтаксис


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Рекогнитионресулт* \[ окне\]
</dt> <dd>

Объект [**иинкрекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , содержащий результат распознавания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иирекогнитионресулт.

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

[**Recognize \[ элемент управления InkEdit метода\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

