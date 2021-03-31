---
title: Метод Session. Invoke (Всмандисп. h)
description: Вызывает метод и возвращает результаты вызова метода.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Вызов метода служба удаленного управления Windows
- Метод Invoke служба удаленного управления Windows, объект Session
- Объект Session служба удаленного управления Windows, метод Invoke
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803568"
---
# <a name="sessioninvoke-method"></a><span data-ttu-id="c7b83-106">Session. Invoke, метод</span><span class="sxs-lookup"><span data-stu-id="c7b83-106">Session.Invoke method</span></span>

<span data-ttu-id="c7b83-107">Вызывает метод и возвращает результаты вызова метода.</span><span class="sxs-lookup"><span data-stu-id="c7b83-107">Invokes a method and returns the results of the method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b83-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7b83-108">Syntax</span></span>


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c7b83-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7b83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b83-110">*актионури* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7b83-110">*actionUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b83-111">URI вызываемого метода.</span><span class="sxs-lookup"><span data-stu-id="c7b83-111">The URI of the method to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="c7b83-112">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7b83-112">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b83-113">Идентификатор извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c7b83-113">The identifier of the resource to retrieve.</span></span>

<span data-ttu-id="c7b83-114">Этот параметр может содержать одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="c7b83-114">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="c7b83-115">URI с [*селекторами*](windows-remote-management-glossary.md)или без них.</span><span class="sxs-lookup"><span data-stu-id="c7b83-115">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="c7b83-116">В следующем примере Visual Basic Scripting Edition (VBScript) ключ задается параметром `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="c7b83-116">In the following Visual Basic Scripting Edition (VBScript) example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="c7b83-117">Объект [**ResourceLocator**](resourcelocator.md) , который может содержать селекторы, [*фрагменты*](windows-remote-management-glossary.md)или [*Параметры*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c7b83-117">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="c7b83-118">Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте [протокол WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="c7b83-118">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="c7b83-119">Дополнительные сведения о общедоступной спецификации для протокола WS-Management см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="c7b83-119">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="c7b83-120">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7b83-120">*parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b83-121">XML-представление входных данных для метода.</span><span class="sxs-lookup"><span data-stu-id="c7b83-121">The XML representation of the input for the method.</span></span> <span data-ttu-id="c7b83-122">Необходимо указать эту строку, иначе этот метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="c7b83-122">This string must be supplied or this method will fail.</span></span>

</dd> <dt>

<span data-ttu-id="c7b83-123">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c7b83-123">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7b83-124">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c7b83-124">Reserved.</span></span> <span data-ttu-id="c7b83-125">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="c7b83-125">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b83-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7b83-126">Return value</span></span>

<span data-ttu-id="c7b83-127">XML-представление выходных данных метода.</span><span class="sxs-lookup"><span data-stu-id="c7b83-127">The XML representation of the method output.</span></span>

## <a name="examples"></a><span data-ttu-id="c7b83-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="c7b83-128">Examples</span></span>

<span data-ttu-id="c7b83-129">Следующий пример кода VBScript запускает процесс Calc.exe.</span><span class="sxs-lookup"><span data-stu-id="c7b83-129">The following VBScript code example starts a Calc.exe process.</span></span> <span data-ttu-id="c7b83-130">Параметр *стринпутпараметерс* содержит входные параметры в формате XML.</span><span class="sxs-lookup"><span data-stu-id="c7b83-130">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="c7b83-131">Единственным обязательным входным параметром для метода [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) WMI является Командная строка для выполнения.</span><span class="sxs-lookup"><span data-stu-id="c7b83-131">The only required input parameter for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is the command line to execute.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



<span data-ttu-id="c7b83-132">В следующем примере кода VBScript вызывается метод **Session. Invoke** для выполнения метода [**«Начало**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) » [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="c7b83-132">The following VBScript code example calls the **Session.Invoke** method to execute the [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) method of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="c7b83-133">Метод **"** неуспешно" не имеет входных параметров.</span><span class="sxs-lookup"><span data-stu-id="c7b83-133">The **StopService** method does not have input parameters.</span></span> <span data-ttu-id="c7b83-134">Однако метод **Invoke** требует строку XML в параметре *Parameters* .</span><span class="sxs-lookup"><span data-stu-id="c7b83-134">However, the **Invoke** method requires an XML string in the *parameters* parameter.</span></span>


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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



## <a name="requirements"></a><span data-ttu-id="c7b83-135">Требования</span><span class="sxs-lookup"><span data-stu-id="c7b83-135">Requirements</span></span>



| <span data-ttu-id="c7b83-136">Требование</span><span class="sxs-lookup"><span data-stu-id="c7b83-136">Requirement</span></span> | <span data-ttu-id="c7b83-137">Значение</span><span class="sxs-lookup"><span data-stu-id="c7b83-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b83-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7b83-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b83-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7b83-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c7b83-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7b83-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b83-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7b83-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c7b83-142">Header</span><span class="sxs-lookup"><span data-stu-id="c7b83-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7b83-143"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7b83-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7b83-144">IDL</span><span class="sxs-lookup"><span data-stu-id="c7b83-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7b83-145"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7b83-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7b83-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7b83-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7b83-147"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7b83-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7b83-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c7b83-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7b83-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7b83-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c7b83-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7b83-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b83-151">**Session**</span><span class="sxs-lookup"><span data-stu-id="c7b83-151">**Session**</span></span>](session.md)
</dt> </dl>

 

