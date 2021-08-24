---
description: Задает набор доступных предупреждений, которые могут возникнуть во время анализа рукописного ввода.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: Перечисление Аналисисварнингкоде (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 48d03c0f4c479ddf6a3f1f9f371bc13b889641994f86df75b107b17ca081a97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660875"
---
# <a name="analysiswarningcode-enumeration"></a>Перечисление Аналисисварнингкоде

Задает набор доступных предупреждений, которые могут возникнуть во время анализа рукописного ввода.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**Аналисисварнингкоде \_ прервана**
</dt> <dd>

Операция анализа прервана.

Возвращается только при вызове операции синхронного анализа. Прерывание асинхронной операции не вызовет событие [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**Аналисисварнингкоде \_ номатчингинканалисисрекогнизерфаунд**
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) не удается найти распознаватель рукописного ввода, который соответствует требованиям к языку или возможности, необходимым для выполнения операции анализа.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**Аналисисварнингкоде \_ фактоиднотсуппортед**
</dt> <dd>

Распознаватель рукописного ввода не смог соблюдать указанный набор фактоид на узле указания по анализу (см. раздел свойства указания [**иконтекстноде:: GetType**](icontextnode-gettype.md) и указания по [анализу](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**Аналисисварнингкоде \_ фактоидкоерЦионнотсуппортед**
</dt> <dd>

Распознаватель рукописного ввода не смог привести свои результаты к указанному фактоид в узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**Аналисисварнингкоде \_ гуиденотсуппортед**
</dt> <dd>

Распознаватель рукописного ввода не смог соблюдать указанный набор руководств на узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**Аналисисварнингкоде \_ вордлистнотсуппортед**
</dt> <dd>

Распознаватель рукописного ввода не смог соблюдать указанный набор списков слов на узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**Аналисисварнингкоде \_ вордмоденотсуппортед**
</dt> <dd>

Распознаватель рукописного ввода не смог проанализировать указанный режим Word на узле указания по анализу (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md) и свойства указания по [анализу](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**Аналисисварнингкоде \_ партиалдиктионаритермснотсуппортед**
</dt> <dd>

Указывает, что часть словарных терминов не может быть возвращена из [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**Аналисисварнингкоде \_ текстрекогнитионпроцессфаилед**
</dt> <dd>

Указывает, что процесс распознавания текста завершился ошибкой.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**Аналисисварнингкоде \_ аддинкторекогнизерфаилед**
</dt> <dd>

Не удалось добавить рукописный ввод в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md). Например, добавление штрихов, собираемых с помощью мыши в распознавателе жестов, завершится ошибкой, так как для распознавателя жестов требуются штрихи, полученные от дигитайзера.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**Аналисисварнингкоде \_ сетпрефикссуффиксфаилед**
</dt> <dd>

[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) не удалось сособлюдать указанный префикс или текст суффикса узла указания анализа (см. раздел [Свойства подсказки](analysis-hint-properties.md) [**Иконтекстноде:: GetType**](icontextnode-gettype.md) и Analysis).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**Аналисисварнингкоде \_ инканалисисрекогнизеринитиализатионфаилед**
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) не удалось создать, клонировать или задать штрихи в [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**Аналисисварнингкоде \_ конфирмедвисаутинкрекогнитион**
</dt> <dd>

Указывает, что объект [**иконтекстноде**](icontextnode.md) подтвержден пользователем, но не имеет значений распознавания, вычисленных для узла.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**Аналисисварнингкоде \_ баккграундексцептион**
</dt> <dd>

Фоновая операция не была завершена из-за исключения. Это неустранимая ошибка, которая требует повторного создания экземпляра [**иинканализер**](iinkanalyzer.md) перед дальнейшим использованием.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**Аналисисварнингкоде \_ контекстноделокатионнотсет**
</dt> <dd>

Указывает, что объект [**иконтекстноде**](icontextnode.md) не имеет правильного набора местоположений (см. [**Иконтекстноде:: SetLocation**](icontextnode-setlocation.md)). Метод [**иконтекстноде::**](icontextnode-getlocation.md) GetObject должен возвращать непустое значение, если объект **иконтекстноде** не помечен как частично заполненный.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**Аналисисварнингкоде \_ лангуажеиднотреспектед**
</dt> <dd>

Идентификатор языка, заданный для штриха, связанного с узлом пользовательского распознавателя (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md)), не соответствует идентификатору языка используемого [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) . Рукописный ввод по-прежнему распознан указанным **иинканалисисрекогнизер**.

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**Аналисисварнингкоде \_ енаблеуникодечарактерранжеснотсуппортед**
</dt> <dd>

[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) не поддерживает включение диапазонов символов Юникода, как указано.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**Аналисисварнингкоде \_ топинкбреаксонлинотсуппортед**
</dt> <dd>

[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) не поддерживает топинкбреакс только в том случае, если указания содержали запрос только для топинкбреакс.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**Аналисисварнингкоде \_ аналисисалреадируннинг**
</dt> <dd>

[**Иинканализер**](iinkanalyzer.md) уже выполняет фоновый анализ.

</dd> </dl>

## <a name="remarks"></a>Remarks

**Аналисисварнингкоде \_ Баккграундексцептион** — это единственное значение кода предупреждения, которое требует повторного создания экземпляра объекта [**иинканализер**](iinkanalyzer.md) перед дальнейшим использованием.

Другие предупреждения, например **аналисисварнингкоде \_ Инканалисисрекогнизеринитиализатионфаилед** и **аналисисварнингкоде \_ NoMatchingInkAnalysisRecognizerFound**, могут потребовать, чтобы объект [**IInkAnalyzer**](iinkanalyzer.md) использовал другой распознаватель.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ианалисисварнинг:: Жетварнингкоде**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




