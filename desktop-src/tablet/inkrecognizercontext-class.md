---
description: Позволяет выполнять распознавание рукописного ввода, получать результаты распознавания и получать альтернативные варианты. Инкрекогнизерконтекст позволяет различным распознавателям, установленным в системе, использовать распознавание рукописного ввода для правильной обработки входных данных.
ms.assetid: 2b39fd32-831d-4606-8600-b52aaa7ed882
title: Класс Инкрекогнизерконтекст (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerContext
- InkRecognizerContext.IInkRecognizerContext
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 781d1b440f1287b22d5c3ddf7ecf7132f7311fc5f48da5da20e4145717f65bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218405"
---
# <a name="inkrecognizercontext-class"></a>Класс Инкрекогнизерконтекст

Позволяет выполнять распознавание рукописного ввода, получать результаты распознавания и получать альтернативные варианты. **Инкрекогнизерконтекст** позволяет различным распознавателям, установленным в системе, использовать распознавание рукописного ввода для правильной обработки входных данных.

**Инкрекогнизерконтекст** имеет следующие типы членов:

-   [События](#events)
-   [Интерфейсы](#interfaces)
-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="events"></a>События

Класс **инкрекогнизерконтекст** содержит следующие события.



| Событие                                                                               | Описание                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Распознавание**](inkrecognizercontext-recognition.md)                             | Происходит, когда Инкрекогнизерконтекст создает результаты из метода Баккграундрекогнизе.<br/>                                                                                             |
| [**рекогнитионвисалтернатес**](inkrecognizercontext-recognitionwithalternates.md) | Происходит, когда **инкрекогнизерконтекст** создает результаты после вызова метода [**баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)<br/> |



 

### <a name="interfaces"></a>Интерфейсы

Класс **инкрекогнизерконтекст** определяет эти интерфейсы.



| Интерфейс                 | Описание                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| **иинкрекогнизерконтекст** | Этот объект реализует COM-интерфейс **иинкрекогнизерконтекст** .<br/> |



 

### <a name="methods"></a>Методы

Класс **инкрекогнизерконтекст** содержит следующие методы.



| Метод                                                                                              | Описание                                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)                             | Указывает, что распознаватель должен распознать связанные штрихи и запустить событие [**распознавания**](inkrecognizercontext-recognition.md) после завершения распознавания.<br/>                                                                |
| [**баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) | Указывает, что распознаватель должен распознать связанные штрихи и запустить событие [**рекогнитионвисалтернатес**](inkrecognizercontext-recognitionwithalternates.md) после завершения распознавания.<br/>                                    |
| [**Клонировать**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                                                      | Создает дубликат **инкрекогнизерконтекст**.<br/>                                                                                                                                                                                               |
| [**ендинкинпут**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput)                                             | Завершает ввод рукописного ввода в **инкрекогнизерконтекст**.<br/>                                                                                                                                                                                             |
| [**исстрингсуппортед**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)                                 | Указывает, содержит ли заданную строку системный словарь, Пользовательский словарь или [**список слов**](inkwordlist-class.md) .<br/>                                                                                                             |
| [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)                                                 | Выполняет распознавание в коллекции [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) и возвращает результаты распознавания.<br/>                                                                                                                          |
| [**стопбаккграундрекогнитион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition)                 | Завершает распознавание фона, которое было запущено с помощью вызова [**баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) или [**баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates).<br/> |



 

### <a name="properties"></a>Свойства

Класс **инкрекогнизерконтекст** имеет следующие свойства.



| Свойство                                                                                   | Тип доступа           | Описание                                                                                                                                                |
|:-------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**чарактераутокомплетион**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode)<br/> | Чтение/запись<br/> | Возвращает или задает режим автозаполнения символов, определяющий, когда распознаются символы или слова.<br/>                                         |
| [**фактоид**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)<br/>                                 | Чтение/запись<br/> | Возвращает или задает строковое имя фактоид, используемое объектом **инкрекогнизерконтекст** .<br/>                                                        |
| [**Руководство**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide)<br/>                                     | Чтение/запись<br/> | Возвращает или задает [**инкрекогнизергуиде**](inkrecognizerguide-class.md) , используемый для ввода рукописных данных.<br/>                                                   |
| [**префикстекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext)<br/>                           | Чтение/запись<br/> | Возвращает или задает символы, которые предшествуют коллекции [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) в объекте **инкрекогнизерконтекст** .<br/> |
| [**рекогнитионфлагс**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags)<br/>               | Чтение/запись<br/> | Возвращает или задает флаги, указывающие, как распознаватель интерпретирует рукописный ввод и определяет результирующую строку.<br/>                                     |
| [**Распознавателя**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognizer)<br/>                           | Чтение/запись<br/> | Возвращает или задает объект [**иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) , используемый объектом **инкрекогнизерконтекст** .<br/>                                   |
| [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes)<br/>                                 | Чтение/запись<br/> | Возвращает или задает коллекцию [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , связанную с объектом **инкрекогнизерконтекст** .<br/>                    |
| [**суффикстекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext)<br/>                           | Чтение/запись<br/> | Возвращает или задает символы, которые поступают после коллекции [**инкстрокес**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) в объекте **инкрекогнизерконтекст** .<br/>  |
| [**Составлен**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)<br/>                               | Чтение/запись<br/> | Возвращает или задает объект [**инквордлист**](inkwordlist-class.md) , используемый для улучшения результатов распознавания.<br/>                               |



 

## <a name="remarks"></a>Remarks

Для создания экземпляра этого объекта можно вызвать метод [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) в C++.

Существует два типа распознавания: фоновый (асинхронный) или передний план (синхронный). Распознавание фона начинается с вызова методов [**баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) или [**баккграундрекогнизевисалтернатес**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) , выполняется в фоновом потоке и передает результаты в приложение с помощью механизма событий. Распознавание переднего плана не возвращает значение до тех пор, пока не будет завершено распознавание, что делает результаты распознавания доступными вызывающему потоку без прослушивания события распознавания.

Рукописные данные обрабатываются непрерывно в фоновом режиме. Если [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) добавляется в коллекцию [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , на которую ссылается **инкрекогнизерконтекст** , то **иинкстрокедисп** распознается немедленно. Дополнительные сведения см. в разделе Примечания в методе [**ендинкинпут**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-endinkinput) .

Все распознавание выполняется с помощью контекста распознавателя. Контекст определяет параметры для одного сеанса распознавания. Он получает рукописный ввод, который должен быть распознан, и определяет ограничения на ввод рукописных данных и на выходе распознавания. Ограничения, которые могут быть установлены в контексте, включают язык, словарь и грамматику, которая используется.

> [!Note]  
> Установка свойств, отличных от [**штрихов**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_strokes) или свойств [**чарактераутокомплетион**](/windows/win32/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode) , завершилась только в том случае, если коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) имеет **значение NULL**. Прежде чем присоединить коллекцию Инкстрокес к **инкрекогнизерконтекст**, необходимо задать другие свойства или задать для коллекции Инкстрокес **значение NULL** , а затем задать другие свойства. Если для коллекции Инкстрокес задано **значение NULL** , а затем заданы другие свойства, может потребоваться повторное подключение коллекции инкстрокес. Это связано с тем, что распознавание начинается сразу после назначения Инкстрокес **инкрекогнизерконтекст**. Когда выполняется вызов [**метода распознавания \[ класса \] инкрекогнизеконтекст**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) или [**баккграундрекогнизе**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize), результаты вызова могут быть уже доступны.

 

Чтобы повысить производительность приложения, удалите объект **инкрекогнизерконтекст** , когда он больше не нужен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Иинкрекогнизер**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[Коллекция Инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

