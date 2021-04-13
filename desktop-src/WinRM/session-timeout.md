---
title: Свойство Session. timeout (Всмандисп. h)
description: Задает и возвращает максимальное время (в миллисекундах), в течение которого клиентское приложение ожидает служба удаленного управления Windows завершения операций.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства времени ожидания
- Служба удаленного управления Windows свойства времени ожидания, объект сеанса
- Служба удаленного управления Windows объекта сеанса, свойство Timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341360"
---
# <a name="sessiontimeout-property"></a><span data-ttu-id="bdfbd-106">Свойство Session. timeout</span><span class="sxs-lookup"><span data-stu-id="bdfbd-106">Session.Timeout property</span></span>

<span data-ttu-id="bdfbd-107">Задает и возвращает максимальное время (в миллисекундах), в течение которого клиентское приложение ожидает служба удаленного управления Windows завершения операций.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-107">Sets and gets the maximum amount of time, in milliseconds, that the client application waits for Windows Remote Management to complete its operations.</span></span>

<span data-ttu-id="bdfbd-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdfbd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdfbd-109">Syntax</span></span>


```VB
Session.Timeout As long
```



## <a name="property-value"></a><span data-ttu-id="bdfbd-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bdfbd-110">Property value</span></span>

<span data-ttu-id="bdfbd-111">Значение времени ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-111">Time-out value, in milliseconds.</span></span> <span data-ttu-id="bdfbd-112">При превышении значения времени ожидания возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-112">When the time-out value is exceeded, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdfbd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdfbd-113">Remarks</span></span>

<span data-ttu-id="bdfbd-114">Значение времени ожидания можно задать до каждой операции, выполняемой агентом.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-114">The time-out value can be set before each operation performed by the agent.</span></span> <span data-ttu-id="bdfbd-115">Если значение времени ожидания не указано, агент устанавливает значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-115">If a time-out value is not specified, the agent sets the time-out value.</span></span>

<span data-ttu-id="bdfbd-116">Во время операции перечисления значение времени ожидания не может быть сброшено во время перечисления ресурса.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-116">During an enumerate operation, the time-out value cannot be reset while the resource is being enumerated.</span></span>

## <a name="examples"></a><span data-ttu-id="bdfbd-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="bdfbd-117">Examples</span></span>

<span data-ttu-id="bdfbd-118">Следующий пример кода VBScript запускает Calc.exe процесс с помощью метода [**CREATE**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) класса [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) WMI.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-118">The following VBScript code example starts a Calc.exe process using the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span> <span data-ttu-id="bdfbd-119">Параметр *стринпутпараметерс* содержит входные параметры в формате XML.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-119">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="bdfbd-120">Скрипт задает время ожидания для сеанса.</span><span class="sxs-lookup"><span data-stu-id="bdfbd-120">The script specifies a time-out for the session.</span></span>


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

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

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



## <a name="requirements"></a><span data-ttu-id="bdfbd-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bdfbd-121">Requirements</span></span>



| <span data-ttu-id="bdfbd-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bdfbd-122">Requirement</span></span> | <span data-ttu-id="bdfbd-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bdfbd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfbd-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdfbd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bdfbd-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bdfbd-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bdfbd-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdfbd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bdfbd-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdfbd-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bdfbd-128">Header</span><span class="sxs-lookup"><span data-stu-id="bdfbd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdfbd-129"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdfbd-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdfbd-130">IDL</span><span class="sxs-lookup"><span data-stu-id="bdfbd-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bdfbd-131"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bdfbd-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="bdfbd-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bdfbd-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdfbd-133"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bdfbd-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bdfbd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bdfbd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdfbd-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdfbd-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bdfbd-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdfbd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdfbd-137">**Session**</span><span class="sxs-lookup"><span data-stu-id="bdfbd-137">**Session**</span></span>](session.md)
</dt> </dl>

 

