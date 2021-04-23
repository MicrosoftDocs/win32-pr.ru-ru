---
title: Метод Session. reenumerate (Всмандисп. h)
description: Перечисляет таблицу, коллекцию данных или ресурс журнала.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода перечисления
- Служба удаленного управления Windows метода перечисления, объект Session
- Объект Session служба удаленного управления Windows, Enumerate, метод
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071395"
---
# <a name="sessionenumerate-method"></a><span data-ttu-id="fb807-106">Session. Enumerate, метод</span><span class="sxs-lookup"><span data-stu-id="fb807-106">Session.Enumerate method</span></span>

<span data-ttu-id="fb807-107">Перечисляет таблицу, коллекцию данных или ресурс журнала.</span><span class="sxs-lookup"><span data-stu-id="fb807-107">Enumerates a table, data collection, or log resource.</span></span> <span data-ttu-id="fb807-108">Чтобы создать запрос, включите параметр *фильтра* и параметр- *диалект* в перечисление.</span><span class="sxs-lookup"><span data-stu-id="fb807-108">To create a query, include a *filter* parameter and a *dialect* parameter in an enumeration.</span></span> <span data-ttu-id="fb807-109">Для создания запросов также можно использовать объект [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="fb807-109">You can also use a [**ResourceLocator**](resourcelocator.md) object to create queries.</span></span> <span data-ttu-id="fb807-110">Дополнительные сведения см. [в разделе перечисление или составление списка всех экземпляров ресурса](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="fb807-110">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb807-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb807-111">Syntax</span></span>


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="fb807-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb807-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb807-113">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb807-113">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb807-114">Идентификатор извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="fb807-114">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="fb807-115">Этот параметр может содержать одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="fb807-115">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="fb807-116">Универсальный код ресурса (URI) для данного ресурса.</span><span class="sxs-lookup"><span data-stu-id="fb807-116">The URI of the resource.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   <span data-ttu-id="fb807-117">Объект [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="fb807-117">A [**ResourceLocator**](resourcelocator.md) object.</span></span>
-   <span data-ttu-id="fb807-118">Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="fb807-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="fb807-119">Дополнительные сведения о общедоступной спецификации для [протокол WS-Management](ws-management-protocol.md)см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="fb807-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="fb807-120">*Фильтр* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fb807-120">*filter* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb807-121">Фильтр, который определяет, какие элементы в ресурсе возвращаются перечислением.</span><span class="sxs-lookup"><span data-stu-id="fb807-121">A filter that defines what items in the resource are returned by the enumeration.</span></span> <span data-ttu-id="fb807-122">При перечислении ресурса возвращаются только те элементы, которые соответствуют условиям фильтра.</span><span class="sxs-lookup"><span data-stu-id="fb807-122">When the resource is enumerated, only those items that match the filter criteria are returned.</span></span> <span data-ttu-id="fb807-123">Включение параметра *фильтра* и параметра *диалекта* в перечисление преобразует перечисление в запрос.</span><span class="sxs-lookup"><span data-stu-id="fb807-123">Including a *filter* parameter and a *dialect* parameter in an enumeration converts the enumeration into a query.</span></span> <span data-ttu-id="fb807-124">Пример см. в разделе [запрос конкретных экземпляров ресурса](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="fb807-124">For an example, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

<span data-ttu-id="fb807-125">Если у вас есть объект [**ResourceLocator**](resourcelocator.md) для параметра *resourceURI* , этот параметр использовать не следует.</span><span class="sxs-lookup"><span data-stu-id="fb807-125">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="fb807-126">*диалект* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fb807-126">*dialect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb807-127">Язык, используемый фильтром.</span><span class="sxs-lookup"><span data-stu-id="fb807-127">The language used by the filter.</span></span> <span data-ttu-id="fb807-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), подмножество SQL, используемое WMI, является единственным поддерживаемым языком.</span><span class="sxs-lookup"><span data-stu-id="fb807-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), a subset of SQL used by WMI, is the only language supported.</span></span>

<span data-ttu-id="fb807-129">Если у вас есть объект [**ResourceLocator**](resourcelocator.md) для параметра *resourceURI* , этот параметр использовать не следует.</span><span class="sxs-lookup"><span data-stu-id="fb807-129">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="fb807-130">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fb807-130">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb807-131">Параметр, который должен содержать флаг в перечислении **\_ \_ всманенумфлагс** .</span><span class="sxs-lookup"><span data-stu-id="fb807-131">A parameter that must contain a flag in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="fb807-132">Дополнительные сведения см. в разделе [константы перечисления](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fb807-132">For more information, see [Enumeration Constants](enumeration-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb807-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb807-133">Return value</span></span>

<span data-ttu-id="fb807-134">Объект [**перечислителя**](enumerator.md) , содержащий результаты перечисления.</span><span class="sxs-lookup"><span data-stu-id="fb807-134">An [**Enumerator**](enumerator.md) object that contains the results of the enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb807-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb807-135">Remarks</span></span>

<span data-ttu-id="fb807-136">Дополнительные сведения об ограничении сетевых вызовов во время перечисления см. в описании свойства [**батчитемс**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="fb807-136">For more information about limiting network calls during an enumeration, see the [**BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="fb807-137">Имейте в виду, что если флаги содержат [**константы перечисления**](enumeration-constants.md) **всманфлагхиерарчидипбасепропсонли** или **всманфлагхиерарчишаллов** , то служба удаленного управления Windows служба возвращает код ошибки, **\_ \_ \_ \_ не поддерживаемый режимом полиморфизма WSMan**.</span><span class="sxs-lookup"><span data-stu-id="fb807-137">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then Windows Remote Management service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

<span data-ttu-id="fb807-138">Если задан фильтр, он должен быть допустимым документом в отношении схемы ресурса.</span><span class="sxs-lookup"><span data-stu-id="fb807-138">If a filter is specified, it must be a valid document with respect to the schema of the resource.</span></span> <span data-ttu-id="fb807-139">Параметр диалекта является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fb807-139">The dialect parameter is optional.</span></span> <span data-ttu-id="fb807-140">Однако если строка фильтра начинается с <, но не является фрагментом XML, следует либо включить параметр *диалекта* , либо установить флаг **всманфлагнонксмлтекст** в параметре *flags* .</span><span class="sxs-lookup"><span data-stu-id="fb807-140">However, if the filter string begins with <, but is not an XML fragment, then either include the *dialect* parameter or set the **WSManFlagNonXmlText** flag in the *flags* parameter.</span></span> <span data-ttu-id="fb807-141">Дополнительные сведения см. в разделе [**константы перечисления**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fb807-141">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

<span data-ttu-id="fb807-142">Соответствующий метод C++ — [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="fb807-142">The corresponding C++ method is [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

## <a name="examples"></a><span data-ttu-id="fb807-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="fb807-143">Examples</span></span>

<span data-ttu-id="fb807-144">Следующий пример кода VBScript перечисляет экземпляры [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) на удаленном компьютере, указанном в полном доменном имени (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="fb807-144">The following VBScript code example enumerates the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instances on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="fb807-145">Имейте в виду, что освобождение объектов перечисления, ожидающих запросов перечисления.</span><span class="sxs-lookup"><span data-stu-id="fb807-145">Be aware that freeing the enumeration object clears pending enumeration requests.</span></span> <span data-ttu-id="fb807-146">Подпрограмма DisplayOutput использует XML-файл преобразования средства командной строки WinRM (Всмткст. xsl) для вывода данных в табличной форме.</span><span class="sxs-lookup"><span data-stu-id="fb807-146">The DisplayOutput subroutine uses the Winrm command-line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fb807-147">Требования</span><span class="sxs-lookup"><span data-stu-id="fb807-147">Requirements</span></span>



| <span data-ttu-id="fb807-148">Требование</span><span class="sxs-lookup"><span data-stu-id="fb807-148">Requirement</span></span> | <span data-ttu-id="fb807-149">Значение</span><span class="sxs-lookup"><span data-stu-id="fb807-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb807-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb807-150">Minimum supported client</span></span><br/> | <span data-ttu-id="fb807-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb807-151">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fb807-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb807-152">Minimum supported server</span></span><br/> | <span data-ttu-id="fb807-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb807-153">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fb807-154">Header</span><span class="sxs-lookup"><span data-stu-id="fb807-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb807-155"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb807-155"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb807-156">IDL</span><span class="sxs-lookup"><span data-stu-id="fb807-156">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb807-157"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb807-157"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="fb807-158">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb807-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb807-159"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb807-159"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb807-160">DLL</span><span class="sxs-lookup"><span data-stu-id="fb807-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb807-161"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb807-161"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb807-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb807-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb807-163">**Session**</span><span class="sxs-lookup"><span data-stu-id="fb807-163">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="fb807-164">Запрос конкретных экземпляров ресурса</span><span class="sxs-lookup"><span data-stu-id="fb807-164">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="fb807-165">**батчитемс**</span><span class="sxs-lookup"><span data-stu-id="fb807-165">**BatchItems**</span></span>](session-batchitems.md)
</dt> <dt>

[<span data-ttu-id="fb807-166">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="fb807-166">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

