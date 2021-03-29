---
description: Изменяет код локали для указанного штриха.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'Метод Иинканализер:: Сетстрокелангуажеид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541991"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a>Метод Иинканализер:: Сетстрокелангуажеид

Изменяет код локали для указанного штриха.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лстрокеид* \[ окне\]
</dt> <dd>

Идентификатор штриха, которому присваивается идентификатор локали.

</dd> <dt>

*лстрокелЦид* \[ окне\]
</dt> <dd>

Идентификатор локали, присваиваемый штриху.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Комментарии

Языковой стандарт штриха задается при добавлении росчерка путем вызова метода [**иинканализер:: аддстроке**](iinkanalyzer-addstroke.md), метода [**Иинканализер:: аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md), [**Иинканализер:: аддстрокес**](iinkanalyzer-addstrokes.md)или [**метода IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md). Чтобы получить языковой стандарт, назначенный для штриха, вызовите [**метод иинканализер:: жетстрокелангуажеид**](iinkanalyzer-getstrokelanguageid.md).

Указанный росчерк перемещается в неклассифицированный узел рукописного ввода (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md)), содержащий штрихи того же языка. Если такой [**иконтекстноде**](icontextnode.md) не существует, этот метод создает новый неклассифицированный узел рукописного ввода и перемещает в него штрих. Неклассифицированный узел рукописного ввода — это **иконтекстноде** с типом унклассифиединк.

Если этот метод перемещает росчерк из [**иконтекстноде**](icontextnode.md) , который не является неклассифицированным узлом рукописного ввода, этот метод также добавляет ограничивающий прямоугольник обводки в «грязную» область анализатора рукописного ввода (см. [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).

Этот метод не перемещает штрих, если параметр *лстрокелЦид* соответствует текущему идентификатору языка Stroke.

Если указанный росчерк не связан с [**иинканализер**](iinkanalyzer.md), этот метод возвращает значение без обновления **иинканализер**.

Дополнительные сведения об идентификаторах языков см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстроке**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокес**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Аддстрокесфорлангуаже**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Метод Иинканализер:: Жетстрокелангуажеид**](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[**Метод Иинканализер:: Сетстрокеслангуажеид**](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

