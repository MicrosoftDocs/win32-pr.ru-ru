---
description: Происходит, когда Инкрекогнизерконтекст создает результаты из метода Баккграундрекогнизе.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Событие Инкрекогнизерконтекст. Recognition (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719658"
---
# <a name="inkrecognizercontextrecognition-event"></a>Событие Инкрекогнизерконтекст. Recognition

Происходит, когда [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) создает результаты из метода [**баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .

## <a name="syntax"></a>Синтаксис


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Рекогнизедстринг* \[ окне\]
</dt> <dd>

Текст результата распознавания с наибольшей достоверностью.

Дополнительные сведения о типе данных BSTR см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> <dt>

*CustomData* \[ окне\]
</dt> <dd>

Объект, содержащий пользовательские данные для результата распознавания.

Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).

</dd> <dt>

*Рекогнитионстатус* \[ окне\]
</dt> <dd>

Состояние распознавания на самый последний результат распознавания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Поведение прикладного программного интерфейса (API) непредсказуемо, если вы попытаетесь получить доступ к исходному объекту [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) из обработчика событий распознавания. Не пытайтесь это сделать. Вместо этого, если это необходимо, создайте флаг и задайте его в обработчике событий [распознавания](ink-recognition.md) . Затем можно опросить этот флаг, чтобы определить, когда следует изменять свойства **инкрекогнизерконтекст** за пределами обработчика событий.

Этот метод события определен в \_ интерфейсе иинкевентс. \_Интерфейс иинкевентс реализует интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ иререкогнитион.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Инкрекогнизерконтекст**](inkrecognizercontext-class.md)
</dt> <dt>

[**Метод Баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[**Перечисление Инкрекогнитионстатус**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[**Метод распознавания**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[**Интерфейс Иинкрекогнитионресулт**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

