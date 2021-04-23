---
title: Метод Session. Create (Всмандисп. h)
description: Создает новый экземпляр ресурса и возвращает ссылку на конечную точку (EPR) нового объекта.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода Create
- Создание служба удаленного управления Windows метода, объект Session
- Объект Session служба удаленного управления Windows, метод Create
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491577"
---
# <a name="sessioncreate-method"></a><span data-ttu-id="0c943-106">Метод Session. Create</span><span class="sxs-lookup"><span data-stu-id="0c943-106">Session.Create method</span></span>

<span data-ttu-id="0c943-107">Создает новый экземпляр ресурса и возвращает [*ссылку на конечную точку (EPR)*](windows-remote-management-glossary.md) нового объекта.</span><span class="sxs-lookup"><span data-stu-id="0c943-107">Creates a new instance of a resource and returns the [*endpoint reference (EPR)*](windows-remote-management-glossary.md) of the new object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c943-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c943-108">Syntax</span></span>


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0c943-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c943-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c943-110">*resourceUri* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c943-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c943-111">Идентификатор создаваемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c943-111">Identifier of the resource to create.</span></span>

<span data-ttu-id="0c943-112">Этот параметр может содержать одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="0c943-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="0c943-113">Универсальный код ресурса (URI) с одним или несколькими [*селекторами*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0c943-113">URI with one or more [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="0c943-114">Имейте в виду, что [*подключаемый модуль WMI*](windows-remote-management-glossary.md) не поддерживает создание ресурсов, отличных от прослушивателя [протокол WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="0c943-114">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a [WS-Management Protocol](ws-management-protocol.md) listener.</span></span>
-   <span data-ttu-id="0c943-115">Объект [**ResourceLocator**](resourcelocator.md) , который может содержать селекторы, [*фрагменты*](windows-remote-management-glossary.md)или [*Параметры*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="0c943-115">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="0c943-116">Ссылка на конечную точку [*WS-Addressing*](windows-remote-management-glossary.md) , как описано в стандарте протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="0c943-116">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="0c943-117">Дополнительные сведения о общедоступной спецификации для протокола WS-Management см. на [странице индекс спецификаций управления](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="0c943-117">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="0c943-118">*ресурсов*</span><span class="sxs-lookup"><span data-stu-id="0c943-118">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="0c943-119">XML-код, содержащий содержимое ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c943-119">The XML that contains resource content.</span></span>

</dd> <dt>

<span data-ttu-id="0c943-120">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0c943-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c943-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="0c943-121">Reserved.</span></span> <span data-ttu-id="0c943-122">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="0c943-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c943-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c943-123">Return value</span></span>

<span data-ttu-id="0c943-124">EPR нового ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c943-124">The EPR of the new resource.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c943-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c943-125">Remarks</span></span>

<span data-ttu-id="0c943-126">**Сеанс. Create** используется только для создания новых экземпляров ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c943-126">**Session.Create** is only used for creating new instances of a resource.</span></span> <span data-ttu-id="0c943-127">Используйте метод [**Session. помещаем**](session-put.md) для обновления существующих экземпляров ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c943-127">Use the [**Session.Put**](session-put.md) method to update existing instances of a resource.</span></span> <span data-ttu-id="0c943-128">После получения нового универсального кода ресурса (URI) можно вызвать [**сеанс. Get**](session-get.md) , чтобы получить новый объект.</span><span class="sxs-lookup"><span data-stu-id="0c943-128">After you obtain the new resource URI, you can call [**Session.Get**](session-get.md) to retrieve the new object.</span></span> <span data-ttu-id="0c943-129">Новый объект содержит все свойства, назначаемые поставщиком ресурсов при создании нового объекта.</span><span class="sxs-lookup"><span data-stu-id="0c943-129">The new object contains any properties that the resource provider assigns when creating the new object.</span></span> <span data-ttu-id="0c943-130">Например, если создать новый [*прослушиватель*](windows-remote-management-glossary.md) протокола WS-Management и получить объект прослушивателя с помощью **сеанса. Get**, то вы получаете также свойства **Port**, **Enabled** и **листенингон** .</span><span class="sxs-lookup"><span data-stu-id="0c943-130">For example, if you create a new WS-Management protocol [*listener*](windows-remote-management-glossary.md) and retrieve the listener object using **Session.Get**, then you also obtain the **Port**, **Enabled**, and **ListeningOn** properties.</span></span>

<span data-ttu-id="0c943-131">Имейте в виду, что [*подключаемый модуль WMI*](windows-remote-management-glossary.md) не поддерживает создание каких-либо ресурсов, кроме прослушивателя протокола WS-Management.</span><span class="sxs-lookup"><span data-stu-id="0c943-131">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a WS-Management protocol listener.</span></span>

<span data-ttu-id="0c943-132">Для вызова этого метода используется следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="0c943-132">The following syntax is used to call this method.</span></span>


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a><span data-ttu-id="0c943-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="0c943-133">Examples</span></span>

<span data-ttu-id="0c943-134">В следующем примере кода на языке VBScript вызывается **сеанс. Create** для создания прослушивателя на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="0c943-134">The following VBScript code example calls **Session.Create** to create a listener on the local computer.</span></span>


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a><span data-ttu-id="0c943-135">Требования</span><span class="sxs-lookup"><span data-stu-id="0c943-135">Requirements</span></span>



| <span data-ttu-id="0c943-136">Требование</span><span class="sxs-lookup"><span data-stu-id="0c943-136">Requirement</span></span> | <span data-ttu-id="0c943-137">Значение</span><span class="sxs-lookup"><span data-stu-id="0c943-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c943-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c943-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0c943-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c943-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0c943-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c943-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0c943-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c943-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0c943-142">Header</span><span class="sxs-lookup"><span data-stu-id="0c943-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c943-143"><dt>Всмандисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c943-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c943-144">IDL</span><span class="sxs-lookup"><span data-stu-id="0c943-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c943-145"><dt>Всмандисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c943-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0c943-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0c943-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c943-147"><dt>Всмандисп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0c943-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0c943-148">DLL</span><span class="sxs-lookup"><span data-stu-id="0c943-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c943-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c943-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0c943-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c943-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c943-151">**Session**</span><span class="sxs-lookup"><span data-stu-id="0c943-151">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="0c943-152">Протокол WS-Management</span><span class="sxs-lookup"><span data-stu-id="0c943-152">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

