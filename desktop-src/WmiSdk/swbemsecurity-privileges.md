---
description: Свойство Privileges является объектом Свбемпривилежесет. Это свойство используется для включения или отключения конкретных привилегий Windows. Может потребоваться установить одно из этих привилегий для выполнения конкретных задач с помощью API инструментарий управления Windows (WMI) (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: Свойство Свбемсекурити. Privileges (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263788"
---
# <a name="swbemsecurityprivileges-property"></a><span data-ttu-id="9d8af-105">Свбемсекурити. Privileges, свойство</span><span class="sxs-lookup"><span data-stu-id="9d8af-105">SWbemSecurity.Privileges property</span></span>

<span data-ttu-id="9d8af-106">Свойство **Privileges** является объектом [**свбемпривилежесет**](swbemprivilegeset.md) .</span><span class="sxs-lookup"><span data-stu-id="9d8af-106">The **Privileges** property is an [**SWbemPrivilegeSet**](swbemprivilegeset.md) object.</span></span> <span data-ttu-id="9d8af-107">Это свойство используется для включения или отключения конкретных привилегий Windows.</span><span class="sxs-lookup"><span data-stu-id="9d8af-107">This property is used to enable or disable specific Windows privileges.</span></span> <span data-ttu-id="9d8af-108">Может потребоваться установить одно из этих привилегий для выполнения конкретных задач с помощью API инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9d8af-108">You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.</span></span>

<span data-ttu-id="9d8af-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9d8af-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9d8af-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9d8af-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d8af-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d8af-111">Syntax</span></span>


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a><span data-ttu-id="9d8af-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9d8af-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="9d8af-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d8af-113">Remarks</span></span>

<span data-ttu-id="9d8af-114">Этот параметр позволяет предоставлять или отзывать привилегии как часть строки моникера WMI.</span><span class="sxs-lookup"><span data-stu-id="9d8af-114">This setting allows you to grant or revoke privileges as part of a WMI moniker string.</span></span> <span data-ttu-id="9d8af-115">Полный список применимых значений см. в разделе константы [**вбемпривилежеенум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) и [**Privileges**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9d8af-115">For the complete list of applicable values, see [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) and [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="9d8af-116">Можно изменить привилегии, определенные для объектов [**SwbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**свбемобжектпас**](swbemobjectpath.md)и [**SwbemLocator**](swbemlocator.md) , добавив [**свбемпривилеже**](swbemprivilege.md) объекты в свойство **Privileges** .</span><span class="sxs-lookup"><span data-stu-id="9d8af-116">You can change the privileges defined for the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by adding [**SWbemPrivilege**](swbemprivilege.md) objects to the **Privileges** property.</span></span>

<span data-ttu-id="9d8af-117">Существуют фундаментальные различия в том, как различные версии Windows обрабатывают изменения в привилегиях.</span><span class="sxs-lookup"><span data-stu-id="9d8af-117">There are fundamental differences in how different versions of Windows handle changes to privileges.</span></span> <span data-ttu-id="9d8af-118">Если вы разрабатываете приложение, которое используется только на платформах Windows, вы можете установить или отозвать привилегии в любое время.</span><span class="sxs-lookup"><span data-stu-id="9d8af-118">If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.</span></span>

<span data-ttu-id="9d8af-119">В следующем примере задается **SeDebugPrivilege** для первого подключения моникера, чтобы получить объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="9d8af-119">The following example sets the **SeDebugPrivilege** on the initial moniker connection to obtain an [**SWbemServices**](swbemservices.md) object.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



<span data-ttu-id="9d8af-120">Дополнительные сведения о форматировании строки безопасности для подключения моникера см. в разделе [**константы прав**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9d8af-120">For more information about how to format the security string for a moniker connection, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="9d8af-121">В следующем примере выполняется та же задача, но она устанавливает привилегию после первоначального входа в WMI.</span><span class="sxs-lookup"><span data-stu-id="9d8af-121">The following example performs the same task, but it sets the privilege after the initial log on to WMI.</span></span>


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



<span data-ttu-id="9d8af-122">Обратите внимание, что для вызовов [**свбемпривилежесет. аддасстринг**](swbemprivilegeset-addasstring.md)необходимо использовать полное имя права доступа, например "SeDebugPrivilege", а не "Debug".</span><span class="sxs-lookup"><span data-stu-id="9d8af-122">Note that for calls to [**SwbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md), you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".</span></span>

## <a name="requirements"></a><span data-ttu-id="9d8af-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9d8af-123">Requirements</span></span>



| <span data-ttu-id="9d8af-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9d8af-124">Requirement</span></span> | <span data-ttu-id="9d8af-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9d8af-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8af-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d8af-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d8af-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9d8af-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9d8af-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d8af-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d8af-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9d8af-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9d8af-130">Header</span><span class="sxs-lookup"><span data-stu-id="9d8af-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d8af-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d8af-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d8af-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9d8af-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="9d8af-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9d8af-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9d8af-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9d8af-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d8af-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d8af-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9d8af-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="9d8af-136">CLSID</span></span><br/>                    | <span data-ttu-id="9d8af-137">\_СВБЕМСЕКУРИТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="9d8af-137">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="9d8af-138">IID</span><span class="sxs-lookup"><span data-stu-id="9d8af-138">IID</span></span><br/>                      | <span data-ttu-id="9d8af-139">IID \_ исвбемсекурити</span><span class="sxs-lookup"><span data-stu-id="9d8af-139">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9d8af-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d8af-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d8af-141">**свбемсекурити**</span><span class="sxs-lookup"><span data-stu-id="9d8af-141">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="9d8af-142">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="9d8af-142">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="9d8af-143">**свбемпривилежесет**</span><span class="sxs-lookup"><span data-stu-id="9d8af-143">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> </dl>

 

 




