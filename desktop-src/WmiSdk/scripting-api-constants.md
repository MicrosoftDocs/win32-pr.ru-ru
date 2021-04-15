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
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701995"
---
# <a name="scripting-api-constants"></a><span data-ttu-id="ffee5-103">Константы API скриптов</span><span class="sxs-lookup"><span data-stu-id="ffee5-103">Scripting API Constants</span></span>

<span data-ttu-id="ffee5-104">Инструментарий WMI использует несколько типов констант в параметре *ифлагс* вызовов методов в [API скриптов для WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-104">WMI uses several types of constants in the *iflags* parameter of method calls in the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="ffee5-105">Visual Basic приложения могут включать библиотеку типов для API скриптов Wbemdisp. tlb.</span><span class="sxs-lookup"><span data-stu-id="ffee5-105">Visual Basic applications can include the type library for the scripting API, Wbemdisp.tlb.</span></span> <span data-ttu-id="ffee5-106">Скрипты не могут получить доступ к константам в библиотеке типов, если они не используют <REFERENCE> <OBJECT> теги или из формата XML-файлов сценариев Windows (WSH), как описано в разделе [Использование библиотеки типов сценариев WMI](using-the-wmi-scripting-type-library.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-106">Scripts are unable to access constants in the type library unless they use the <REFERENCE> or <OBJECT> tags from the Windows Script Host (WSH) XML file format as described in [Using the WMI Scripting Type Library](using-the-wmi-scripting-type-library.md).</span></span> <span data-ttu-id="ffee5-107">В противном случае скрипт должен использовать значение константы.</span><span class="sxs-lookup"><span data-stu-id="ffee5-107">Otherwise, a script must use the value of the constant.</span></span>

## <a name="constants"></a><span data-ttu-id="ffee5-108">Константы</span><span class="sxs-lookup"><span data-stu-id="ffee5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ffee5-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**вбемаусентикатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-110">Определите уровни проверки подлинности безопасности.</span><span class="sxs-lookup"><span data-stu-id="ffee5-110">Define the security authentication levels.</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**вбемчанжефлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-112">Определите, как выполняется операция записи в класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ffee5-112">Define how a write operation to a class or an instance is carried out.</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**вбемЦимтипинум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-114">Определите допустимые типы CIM для значения свойства.</span><span class="sxs-lookup"><span data-stu-id="ffee5-114">Define the valid CIM types of a property value.</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**вбемкомпарисонфлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-116">Определите параметры сравнения объектов и используются [**SWbemObject. CompareTo \_**](swbemobject-compareto-.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-116">Define the settings for object comparison and are used by [**SWbemObject.CompareTo\_**](swbemobject-compareto-.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**вбемконнектоптионсенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-118">Определяет флаг безопасности, используемый в качестве параметра в вызовах метода [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) , когда происходит сбой подключения к WMI на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ffee5-118">Defines a security flag that is used as a parameter in calls to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method when a connection to WMI on a remote machine is failing.</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**вбемерроренум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-120">Определите ошибки, которые могут возвращаться [API скриптов для вызовов WMI](scripting-api-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="ffee5-120">Define the errors that may be returned by [Scripting API for WMI](scripting-api-for-wmi.md) calls.</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**вбемфлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-122">Определяет константы, используемые [**SWbemServices.Exeккуери**](swbemservices-execquery.md), [**SWbemServices.Exeккуерясинк**](swbemservices-execqueryasync.md), [**SwbemServices. субклассесоф**](swbemservices-subclassesof.md)и [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-122">Defines constants that are used by [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md), and [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**вбемимперсонатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-124">Определите уровни олицетворения безопасности.</span><span class="sxs-lookup"><span data-stu-id="ffee5-124">Define the security impersonation levels.</span></span> <span data-ttu-id="ffee5-125">Эти константы используются с [**свбемсекурити**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-125">These constants are used with [**SWbemSecurity**](swbemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**вбемобжекттекстформатенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-127">Определите допустимые текстовые форматы объекта, которые будут использоваться в [**свбемобжектекс. gettext \_**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-127">Define the valid object text formats to be used by [**SWbemObjectEx.GetText\_**](swbemobjectex-gettext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-129">Определите привилегии.</span><span class="sxs-lookup"><span data-stu-id="ffee5-129">Define privileges.</span></span> <span data-ttu-id="ffee5-130">Эти константы используются с [**свбемсекурити**](swbemsecurity.md) , чтобы предоставить привилегии, необходимые для некоторых операций.</span><span class="sxs-lookup"><span data-stu-id="ffee5-130">These constants are used with [**SWbemSecurity**](swbemsecurity.md) to grant the privileges required for some operations.</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**вбемкуерифлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-132">Определите глубину перечисления или запроса, определяющего количество объектов, возвращаемых вызовом.</span><span class="sxs-lookup"><span data-stu-id="ffee5-132">Define the depth of enumeration or query, which determines how many objects are returned by a call.</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**вбемтекстфлаженум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span><span class="sxs-lookup"><span data-stu-id="ffee5-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-134">Определяет содержимое сгенерированного текста объекта и используется [**SWbemObject. жетобжекттекст \_**](swbemobject-getobjecttext-.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-134">Defines the content of generated object text and is used by [**SWbemObject.GetObjectText\_**](swbemobject-getobjecttext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffee5-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**вбемтимеаут**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span><span class="sxs-lookup"><span data-stu-id="ffee5-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span></span>
</dt> <dd>

<span data-ttu-id="ffee5-136">Определяет константы времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="ffee5-136">Defines the time-out constants.</span></span> <span data-ttu-id="ffee5-137">Эта константа используется [**свбемевентсаурце. некстевент**](swbemeventsource-nextevent.md).</span><span class="sxs-lookup"><span data-stu-id="ffee5-137">This constant is used by [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).</span></span>

</dd> </dl>

## <a name="combining-flags"></a><span data-ttu-id="ffee5-138">Объединение флагов</span><span class="sxs-lookup"><span data-stu-id="ffee5-138">Combining Flags</span></span>

<span data-ttu-id="ffee5-139">Можно сочетать флаги, чтобы повлиять на более чем один аспект вызова API.</span><span class="sxs-lookup"><span data-stu-id="ffee5-139">You can combine flags to affect more than one aspect of the API call.</span></span>

<span data-ttu-id="ffee5-140">Например, чтобы создать вызов [*семисинчронаус*](gloss-s.md) , параметр *ифлагс* в вызове [**ккуери \_SWbemServices.Exe**](swbemservices-execquery.md) должен содержать два флага: **вбемфлагретурниммедиатели** и **вбемфлагфорвардонли**.</span><span class="sxs-lookup"><span data-stu-id="ffee5-140">For example, to create a [*semisynchronous*](gloss-s.md) call, the *iFlags* parameter in an [**SWbemServices.ExecQuery\_**](swbemservices-execquery.md) call must contain two flags: **WbemFlagReturnImmediately** and **WbemFlagForwardOnly**.</span></span> <span data-ttu-id="ffee5-141">Значение **вбемфлагретурниммедиатели** равно 16, а значение **вбемфлагфорвардонли** — 32.</span><span class="sxs-lookup"><span data-stu-id="ffee5-141">The value of **WbemFlagReturnImmediately** is 16 and the value of **WbemFlagForwardOnly** is 32.</span></span> <span data-ttu-id="ffee5-142">Так как к константам нельзя получить доступ по имени, значения этих флагов объединяются, что дает значение *ифлагс* , равное 48.</span><span class="sxs-lookup"><span data-stu-id="ffee5-142">Because the constants cannot be accessed by name, the values of these flags are combined, producing an *iFlags* value of 48.</span></span>

<span data-ttu-id="ffee5-143">В следующем примере скрипта показан вызов.</span><span class="sxs-lookup"><span data-stu-id="ffee5-143">The following script example shows the call.</span></span>


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



<span data-ttu-id="ffee5-144">Не все флаги можно объединить, так как многие из них являются взаимоисключающими и могут привести к непредсказуемым результатам.</span><span class="sxs-lookup"><span data-stu-id="ffee5-144">Not all flags can be combined since many are mutually exclusive and may produce unpredictable results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffee5-145">См. также</span><span class="sxs-lookup"><span data-stu-id="ffee5-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffee5-146">API сценариев для инструментария WMI</span><span class="sxs-lookup"><span data-stu-id="ffee5-146">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 



