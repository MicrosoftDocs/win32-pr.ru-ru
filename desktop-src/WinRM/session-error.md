---
title: Свойство Session. Error (Всмандисп. h)
description: Возвращает дополнительные сведения об ошибке в потоке XML.
ms.assetid: f291c11c-012f-45eb-b851-5661d881ee79
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows свойства ошибки
- Служба удаленного управления Windows свойства ошибки, объект Session
- Объект Session служба удаленного управления Windows, свойство Error
topic_type:
- apiref
api_name:
- Session.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2568fb7f51d6970d3d98f8434357b22efb7793d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710559"
---
# <a name="sessionerror-property"></a><span data-ttu-id="54819-106">Свойство Session. Error</span><span class="sxs-lookup"><span data-stu-id="54819-106">Session.Error property</span></span>

<span data-ttu-id="54819-107">Возвращает дополнительные сведения об ошибке в потоке XML.</span><span class="sxs-lookup"><span data-stu-id="54819-107">Gets additional error information in an XML stream.</span></span> <span data-ttu-id="54819-108">Сведения об ошибках также можно получить из объекта VBScript [Err](/previous-versions//sbf5ze0e(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="54819-108">Error information can also be obtained from the VBScript [Err](/previous-versions//sbf5ze0e(v=vs.85)) object.</span></span>

<span data-ttu-id="54819-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="54819-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54819-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54819-110">Syntax</span></span>


```VB
Session.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="54819-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="54819-111">Property value</span></span>

<span data-ttu-id="54819-112">XML-представление сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="54819-112">XML representation of error information.</span></span>

## <a name="examples"></a><span data-ttu-id="54819-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="54819-113">Examples</span></span>

<span data-ttu-id="54819-114">В следующем примере кода VBScript показан скрипт, который содержит ошибку в [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="54819-114">The following VBScript code example shows a script that contains an error in the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="54819-115">Правильный URI ресурса — `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_QuotaSetting?VolumePath=c:\\` .</span><span class="sxs-lookup"><span data-stu-id="54819-115">The correct resource URI is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_QuotaSetting?VolumePath=c:\\`.</span></span>


```VB
'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_QuotaSetting"

On Error Resume Next
strResponse = objSession.Get( strResourceUri )
If Err.number <> 0 Then
    DisplayErrorInfo()
    strErrorXML = objSession.Error
    WScript.Echo strErrorXML
Else
    Call DisplayOutput(strResponse)
End If
On Error Goto 0

'*************************************************************
' Displays Error information from Err object and Session.Error
'*************************************************************
Sub DisplayErrorInfo()

    WScript.Echo "An error has occurred."     
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    Err.Clear
End Sub
```



<span data-ttu-id="54819-116">Следующий текст представляет собой вывод ошибок из скрипта.</span><span class="sxs-lookup"><span data-stu-id="54819-116">The following text is the error output from the script.</span></span>

``` syntax
Number      : 0x803380FA
Description : The WinRM client cannot process the request. 
The resource URI is not valid: it does not contain keys, but
the class selected is not a singleton. To access an instance which 
is not a singleton, keys must be provided. Use the following 
command to get more information about how to construct a 
resource URI: "winrm help uris".
Source      : Session
HelpFile    :
HelpContext : 0
<f:WSManFault 
xmlns:f="http://schemas.microsoft.com/wbem/wsman/1/wsmanfault" 
Code="2150859002" Machine="Server1" xml:lang="en-US">
<f:Message>
<f:ProviderFault provider="WMIv1 plugin for Windows Remote Management " 
path="%systemroot%\system32\WsmWmiPl.dll">
<f:WSManFault 
xmlns:f="http://schemas.microsoft.com/wbem/wsman/1/wsmanfault" 
Code="2150859002" Machine="" xml:lang="en-US">
<f:Message>The WinRM client cannot process the request. 
The resource URI is not valid: it does not contain keys, but the 
class selected is not a singleton. To access an instance which is 
not a singleton, keys must be provided. Use the following command 
to get more information in how to construct a resource URI: 
&quot;winrm help uris&quot;. 
</f:Message></f:WSManFault>
</f:ProviderFault>
</f:Message
></f:WSManFault>
```

## <a name="requirements"></a><span data-ttu-id="54819-117">Требования</span><span class="sxs-lookup"><span data-stu-id="54819-117">Requirements</span></span>



| <span data-ttu-id="54819-118">Требование</span><span class="sxs-lookup"><span data-stu-id="54819-118">Requirement</span></span> | <span data-ttu-id="54819-119">Значение</span><span class="sxs-lookup"><span data-stu-id="54819-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="54819-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54819-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54819-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54819-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="54819-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54819-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54819-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54819-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="54819-124">Header</span><span class="sxs-lookup"><span data-stu-id="54819-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54819-125"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="54819-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="54819-126">IDL</span><span class="sxs-lookup"><span data-stu-id="54819-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54819-127"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54819-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="54819-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="54819-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="54819-129"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54819-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54819-130">DLL</span><span class="sxs-lookup"><span data-stu-id="54819-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54819-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54819-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="54819-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54819-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54819-133">**Session**</span><span class="sxs-lookup"><span data-stu-id="54819-133">**Session**</span></span>](session.md)
</dt> </dl>

 

