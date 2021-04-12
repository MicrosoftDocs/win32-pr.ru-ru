---
description: 'Происходит, когда элемент управления InkEdit получает результаты вручную из вызова метода InkEdit:: Recognize или автоматически после срабатывания времени ожидания распознавания.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Событие InkEdit. Рекогнитионресулт (with. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272317"
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

## <a name="remarks"></a>Комментарии

Этот метод события определен в интерфейсе **\_ иинкедитевентс** . Интерфейс **\_ иинкедитевентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иирекогнитионресулт.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>«С». h (также требует \_ ввода i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> <dt>

[**Recognize \[ элемент управления InkEdit метода\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)
</dt> </dl>

 

