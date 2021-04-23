---
title: Метод Session. Where (Всмандисп. h)
description: Обновление ресурса.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Метод размещения служба удаленного управления Windows
- Метод размещения служба удаленного управления Windows, объект Session
- Объект Session служба удаленного управления Windows, метод размещения
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415824"
---
# <a name="sessionput-method"></a><span data-ttu-id="6b419-106">Метод Session. поместил</span><span class="sxs-lookup"><span data-stu-id="6b419-106">Session.Put method</span></span>

<span data-ttu-id="6b419-107">Обновление ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b419-107">Updates a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b419-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b419-108">Syntax</span></span>


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6b419-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b419-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b419-110">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b419-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b419-111">Идентификатор обновляемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b419-111">The identifier of the resource to be updated.</span></span>

<span data-ttu-id="6b419-112">Этот параметр может содержать один из элементов, содержащихся в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="6b419-112">This parameter can contain one of elements contained in the following list:</span></span>

-   <span data-ttu-id="6b419-113">URI с [*селекторами*](windows-remote-management-glossary.md)или без них.</span><span class="sxs-lookup"><span data-stu-id="6b419-113">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="6b419-114">При вызове метода **размещения** для получения ресурса WMI используйте ключевое свойство или свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="6b419-114">When calling the **Put** method to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="6b419-115">Например, в Visual Basic приведенном ниже примере кода сценария VBScript ключ задается с помощью `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="6b419-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="6b419-116">Объект [**ResourceLocator**](resourcelocator.md) , который может содержать селекторы, [*фрагменты*](windows-remote-management-glossary.md)или [*Параметры*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="6b419-116">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="6b419-117">Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте [протокол WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="6b419-117">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="6b419-118">Дополнительные сведения о общедоступной спецификации для протокола WS-Management см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="6b419-118">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="6b419-119">*ресурс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b419-119">*resource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b419-120">Обновленное содержимое ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b419-120">The updated resource content.</span></span>

</dd> <dt>

<span data-ttu-id="6b419-121">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="6b419-121">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6b419-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="6b419-122">Reserved.</span></span> <span data-ttu-id="6b419-123">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="6b419-123">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b419-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6b419-124">Return value</span></span>

<span data-ttu-id="6b419-125">XML-код, содержащий обновленное содержимое ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b419-125">The XML that contains the updated resource content.</span></span>

## <a name="examples"></a><span data-ttu-id="6b419-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="6b419-126">Examples</span></span>

<span data-ttu-id="6b419-127">В следующем примере кода VBScript данные записываются в объект [**Win32 \_ вмисеттинг**](/windows/desktop/CIMWin32Prov/win32-wmisetting) .</span><span class="sxs-lookup"><span data-stu-id="6b419-127">The following VBScript code example writes data to the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) object.</span></span> <span data-ttu-id="6b419-128">Необходимо включить все свойства объекта, не являющиеся массивами, в XML параметра *Resource* .</span><span class="sxs-lookup"><span data-stu-id="6b419-128">You must include all non-array properties of the object in the XML of the *Resource* parameter.</span></span> <span data-ttu-id="6b419-129">Порядок свойств не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="6b419-129">The order of the properties is not significant.</span></span>


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

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
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



## <a name="requirements"></a><span data-ttu-id="6b419-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6b419-130">Requirements</span></span>



| <span data-ttu-id="6b419-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6b419-131">Requirement</span></span> | <span data-ttu-id="6b419-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6b419-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b419-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b419-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b419-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b419-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6b419-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b419-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b419-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b419-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6b419-137">Header</span><span class="sxs-lookup"><span data-stu-id="6b419-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b419-138"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b419-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b419-139">IDL</span><span class="sxs-lookup"><span data-stu-id="6b419-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b419-140"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b419-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6b419-141">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6b419-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b419-142"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6b419-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6b419-143">DLL</span><span class="sxs-lookup"><span data-stu-id="6b419-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b419-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b419-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b419-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b419-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b419-146">**Session**</span><span class="sxs-lookup"><span data-stu-id="6b419-146">**Session**</span></span>](session.md)
</dt> </dl>

 

