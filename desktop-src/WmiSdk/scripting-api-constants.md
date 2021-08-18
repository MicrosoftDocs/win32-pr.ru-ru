---
description: API скриптов для WMI содержит флаги, общие значения и коды ошибок.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Константы API скриптов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84e52c329fc311e7f99a6564ac51f90574308e31fa1eaa90bfb6d0bcdddc69b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130876"
---
# <a name="scripting-api-constants"></a>Константы API скриптов

Инструментарий WMI использует несколько типов констант в параметре *ифлагс* вызовов методов в [API скриптов для WMI](scripting-api-for-wmi.md).

Visual Basic приложения могут включать библиотеку типов для API скриптов Wbemdisp. tlb. скрипты не могут получить доступ к константам в библиотеке типов, если они не используют <REFERENCE> <OBJECT> теги или из формата XML-файла сценария Windows (WSH), как описано в разделе [использование библиотеки типов сценариев WMI](using-the-wmi-scripting-type-library.md). В противном случае скрипт должен использовать значение константы.

## <a name="constants"></a>Константы

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**вбемаусентикатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Определите уровни проверки подлинности безопасности.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**вбемчанжефлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Определите, как выполняется операция записи в класс или экземпляр.

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**вбемЦимтипинум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Определите допустимые типы CIM для значения свойства.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**вбемкомпарисонфлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Определите параметры сравнения объектов и используются [**SWbemObject. CompareTo \_**](swbemobject-compareto-.md).

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**вбемконнектоптионсенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Определяет флаг безопасности, используемый в качестве параметра в вызовах метода [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) , когда происходит сбой подключения к WMI на удаленном компьютере.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**вбемерроренум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Определите ошибки, которые могут возвращаться [API скриптов для вызовов WMI](scripting-api-for-wmi.md) .

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**вбемфлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Определяет константы, используемые [**SWbemServices.Exeккуери**](swbemservices-execquery.md), [**SWbemServices.Exeккуерясинк**](swbemservices-execqueryasync.md), [**SwbemServices. субклассесоф**](swbemservices-subclassesof.md)и [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md).

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**вбемимперсонатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Определите уровни олицетворения безопасности. Эти константы используются с [**свбемсекурити**](swbemsecurity.md).

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**вбемобжекттекстформатенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Определите допустимые текстовые форматы объекта, которые будут использоваться в [**свбемобжектекс. gettext \_**](swbemobjectex-gettext-.md).

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

Определите привилегии. Эти константы используются с [**свбемсекурити**](swbemsecurity.md) , чтобы предоставить привилегии, необходимые для некоторых операций.

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**вбемкуерифлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

Определите глубину перечисления или запроса, определяющего количество объектов, возвращаемых вызовом.

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**вбемтекстфлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

Определяет содержимое сгенерированного текста объекта и используется [**SWbemObject. жетобжекттекст \_**](swbemobject-getobjecttext-.md).

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**вбемтимеаут**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Определяет константы времени ожидания. Эта константа используется [**свбемевентсаурце. некстевент**](swbemeventsource-nextevent.md).

</dd> </dl>

## <a name="combining-flags"></a>Объединение флагов

Можно сочетать флаги, чтобы повлиять на более чем один аспект вызова API.

Например, чтобы создать вызов [*семисинчронаус*](gloss-s.md) , параметр *ифлагс* в вызове [**ккуери \_SWbemServices.Exe**](swbemservices-execquery.md) должен содержать два флага: **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли**. Значение **вбемфлагретурниммедиатели** равно 16, а значение **вбемфлагфорвардонли** — 32. Так как к константам нельзя получить доступ по имени, значения этих флагов объединяются, что дает значение *ифлагс* , равное 48.

В следующем примере скрипта показан вызов.


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



Не все флаги можно объединить, так как многие из них являются взаимоисключающими и могут привести к непредсказуемым результатам.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[API сценариев для инструментария WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



