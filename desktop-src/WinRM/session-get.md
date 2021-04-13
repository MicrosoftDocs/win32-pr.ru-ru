---
title: Метод Session. Get (Всмандисп. h)
description: Извлекает ресурс, указанный с помощью URI, и возвращает XML-представление текущего экземпляра ресурса.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Получение метода служба удаленного управления Windows
- Получение метода служба удаленного управления Windows, объект Session
- Объект Session служба удаленного управления Windows, метод Get
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341020"
---
# <a name="sessionget-method"></a><span data-ttu-id="21de6-106">Session. Get, метод</span><span class="sxs-lookup"><span data-stu-id="21de6-106">Session.Get method</span></span>

<span data-ttu-id="21de6-107">Извлекает ресурс, указанный с помощью [*URI*](windows-remote-management-glossary.md) , и возвращает XML-представление текущего экземпляра ресурса.</span><span class="sxs-lookup"><span data-stu-id="21de6-107">Retrieves the resource specified by the [*URI*](windows-remote-management-glossary.md) and returns an XML representation of the current instance of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="21de6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21de6-108">Syntax</span></span>


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="21de6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="21de6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21de6-110">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="21de6-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21de6-111">Идентификатор извлекаемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="21de6-111">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="21de6-112">Этот параметр может содержать одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="21de6-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="21de6-113">Универсальный код ресурса (URI) с [*селекторами*](windows-remote-management-glossary.md)или без них.</span><span class="sxs-lookup"><span data-stu-id="21de6-113">A URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="21de6-114">При вызове метода **Get** с селектором для получения ресурса WMI используйте ключевое свойство или свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="21de6-114">When calling the **Get** method with a selector to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="21de6-115">Например, в Visual Basic приведенном ниже примере кода сценария VBScript ключ задается с помощью `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="21de6-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span> <span data-ttu-id="21de6-116">Для одноэлементных классов, таких как [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), нельзя использовать селектор.</span><span class="sxs-lookup"><span data-stu-id="21de6-116">For singleton classes, such as [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), you cannot use a selector.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   <span data-ttu-id="21de6-117">Объект [**ResourceLocator**](resourcelocator.md) , который может содержать селекторы, [*фрагменты*](windows-remote-management-glossary.md)или [*Параметры*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="21de6-117">A [**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="21de6-118">Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="21de6-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="21de6-119">Дополнительные сведения о общедоступной спецификации для [протокол WS-Management](ws-management-protocol.md)см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="21de6-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="21de6-120">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="21de6-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="21de6-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="21de6-121">Reserved.</span></span> <span data-ttu-id="21de6-122">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="21de6-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21de6-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="21de6-123">Return value</span></span>

<span data-ttu-id="21de6-124">XML-представление ресурса.</span><span class="sxs-lookup"><span data-stu-id="21de6-124">An XML representation of the resource.</span></span>

## <a name="examples"></a><span data-ttu-id="21de6-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="21de6-125">Examples</span></span>

<span data-ttu-id="21de6-126">В следующем примере кода VBScript извлекается XML-представление экземпляра [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , представляющего службу WMI Winmgmt на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="21de6-126">The following VBScript code example retrieves the XML representation of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instance that represents the WMI Winmgmt service on the local computer.</span></span>


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


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub

```



<span data-ttu-id="21de6-127">Следующий пример кода VBScript извлекает экземпляр службы WMI Winmgmt с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="21de6-127">The following VBScript code example retrieves the WMI Winmgmt service instance from a remote computer.</span></span> <span data-ttu-id="21de6-128">Удаленный компьютер определяется полным доменным именем (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="21de6-128">The remote computer is identified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="21de6-129">Единственное различие между локальной и удаленной версиями — спецификация удаленного компьютера в вызове [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="21de6-129">The only difference between the local and remote version is the specification of the remote computer in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a><span data-ttu-id="21de6-130">Требования</span><span class="sxs-lookup"><span data-stu-id="21de6-130">Requirements</span></span>



| <span data-ttu-id="21de6-131">Требование</span><span class="sxs-lookup"><span data-stu-id="21de6-131">Requirement</span></span> | <span data-ttu-id="21de6-132">Значение</span><span class="sxs-lookup"><span data-stu-id="21de6-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21de6-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21de6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="21de6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="21de6-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="21de6-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21de6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="21de6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21de6-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="21de6-137">Header</span><span class="sxs-lookup"><span data-stu-id="21de6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="21de6-138"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="21de6-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="21de6-139">IDL</span><span class="sxs-lookup"><span data-stu-id="21de6-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21de6-140"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21de6-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="21de6-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21de6-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="21de6-142"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="21de6-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="21de6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="21de6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21de6-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21de6-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21de6-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21de6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21de6-146">**Session**</span><span class="sxs-lookup"><span data-stu-id="21de6-146">**Session**</span></span>](session.md)
</dt> </dl>

 

