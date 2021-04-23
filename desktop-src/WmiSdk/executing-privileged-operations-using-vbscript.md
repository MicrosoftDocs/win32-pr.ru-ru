---
description: При использовании API скриптов для WMI можно задать определенные привилегии безопасности.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Выполнение привилегированных операций с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156822"
---
# <a name="executing-privileged-operations-using-vbscript"></a><span data-ttu-id="b04f5-103">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="b04f5-103">Executing Privileged Operations Using VBScript</span></span>

<span data-ttu-id="b04f5-104">При использовании API скриптов для WMI можно задать определенные привилегии безопасности.</span><span class="sxs-lookup"><span data-stu-id="b04f5-104">If you use the scripting API for WMI, you can set specific security privileges.</span></span> <span data-ttu-id="b04f5-105">Например, можно задать привилегии безопасности для запроса завершения работы операционной системы или проверить журнал событий безопасности.</span><span class="sxs-lookup"><span data-stu-id="b04f5-105">For example, you can set the security privileges to request an operating system shutdown, or to examine the security event log.</span></span> <span data-ttu-id="b04f5-106">Дополнительные сведения см. [в разделе выполнение с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="b04f5-106">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="b04f5-107">При доступе к инструментарию WMI на компьютере необходимо установить только привилегии.</span><span class="sxs-lookup"><span data-stu-id="b04f5-107">You only need to set privileges when you are accessing WMI on your computer.</span></span> <span data-ttu-id="b04f5-108">При обращении к удаленному узлу COM RPC автоматически устанавливает привилегии.</span><span class="sxs-lookup"><span data-stu-id="b04f5-108">When you are accessing a remote host, COM RPC automatically sets the privileges.</span></span> <span data-ttu-id="b04f5-109">Чтобы определить все необходимые привилегии, обратитесь к документации по конкретным классам WMI, к которым вы хотите получить доступ, например Win32 с именем [**\_ операционной**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)системы.</span><span class="sxs-lookup"><span data-stu-id="b04f5-109">To determine all the required privileges, consult the documentation for the specific WMI classes that you want to access, such as [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span> <span data-ttu-id="b04f5-110">Дополнительные сведения см. в разделе [вбемпривилежеенум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="b04f5-110">For more information, see [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>

<span data-ttu-id="b04f5-111">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="b04f5-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="b04f5-112">Установка привилегий из объекта безопасности \_</span><span class="sxs-lookup"><span data-stu-id="b04f5-112">Setting a Privilege from the Security\_ Object</span></span>](/windows)
-   [<span data-ttu-id="b04f5-113">Настройка привилегий как части моникера</span><span class="sxs-lookup"><span data-stu-id="b04f5-113">Setting a Privilege as Part of a Moniker</span></span>](#setting-a-privilege-as-part-of-a-moniker)
-   [<span data-ttu-id="b04f5-114">Отмена и сброс привилегий</span><span class="sxs-lookup"><span data-stu-id="b04f5-114">Revoking and Resetting Privileges</span></span>](#revoking-and-resetting-privileges)
-   [<span data-ttu-id="b04f5-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b04f5-115">Related topics</span></span>](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a><span data-ttu-id="b04f5-116">Установка привилегий из объекта безопасности \_</span><span class="sxs-lookup"><span data-stu-id="b04f5-116">Setting a Privilege from the Security\_ Object</span></span>

<span data-ttu-id="b04f5-117">Используйте следующую процедуру, чтобы задать привилегии безопасности в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b04f5-117">Use the following procedure to set security privileges in Visual Basic.</span></span>

<span data-ttu-id="b04f5-118">**Установка привилегий в Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="b04f5-118">**To set privileges in Visual Basic**</span></span>

1.  <span data-ttu-id="b04f5-119">Создайте объект типа [**SWbemLocator**](swbemlocator.md).</span><span class="sxs-lookup"><span data-stu-id="b04f5-119">Create an object of type [**SWbemLocator**](swbemlocator.md).</span></span>
2.  <span data-ttu-id="b04f5-120">Добавьте новую привилегию в объект [**SWbemLocator. Security \_**](swbemlocator-security-.md) .</span><span class="sxs-lookup"><span data-stu-id="b04f5-120">Add the new privilege to the [**SWbemLocator.Security\_**](swbemlocator-security-.md) object.</span></span>

    <span data-ttu-id="b04f5-121">Объект [**безопасности \_**](swbemlocator-security-.md) содержит коллекцию [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="b04f5-121">The [**Security\_**](swbemlocator-security-.md) object contains an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="b04f5-122">Объекты в наборе являются объектами [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="b04f5-122">The objects in the set are [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="b04f5-123">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="b04f5-123">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

3.  <span data-ttu-id="b04f5-124">Войдите в WMI и получите объект [**SwbemServices**](swbemservices.md) .</span><span class="sxs-lookup"><span data-stu-id="b04f5-124">Log on to WMI and retrieve an [**SWbemServices**](swbemservices.md) object.</span></span>

    <span data-ttu-id="b04f5-125">Объект [**SwbemServices**](swbemservices.md) наследует привилегию, заданную на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="b04f5-125">The [**SWbemServices**](swbemservices.md) object inherits the privilege that is set in the previous step.</span></span>

<span data-ttu-id="b04f5-126">Вы также можете задать привилегию с помощью метода [**свбемпривилежесет. аддасстринг**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="b04f5-126">You can also set a privilege using the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method.</span></span>

## <a name="setting-a-privilege-as-part-of-a-moniker"></a><span data-ttu-id="b04f5-127">Настройка привилегий как части моникера</span><span class="sxs-lookup"><span data-stu-id="b04f5-127">Setting a Privilege as Part of a Moniker</span></span>

<span data-ttu-id="b04f5-128">Вы можете задать привилегию как часть моникера.</span><span class="sxs-lookup"><span data-stu-id="b04f5-128">You can set a privilege as part of a moniker.</span></span>

<span data-ttu-id="b04f5-129">В следующем примере показано, как добавить в моникер привилегию отладки.</span><span class="sxs-lookup"><span data-stu-id="b04f5-129">The following example shows you how to add a debug privilege to a moniker.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a><span data-ttu-id="b04f5-130">Отмена и сброс привилегий</span><span class="sxs-lookup"><span data-stu-id="b04f5-130">Revoking and Resetting Privileges</span></span>

<span data-ttu-id="b04f5-131">В следующем примере показано, как задать привилегию **SeDebugPrivilege** и отозвать привилегию **серемотешутдовнпривилеже** .</span><span class="sxs-lookup"><span data-stu-id="b04f5-131">The following example shows you how to set the **SeDebugPrivilege** privilege, and revoke the **SeRemoteShutdownPrivilege** privilege.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a><span data-ttu-id="b04f5-132">См. также</span><span class="sxs-lookup"><span data-stu-id="b04f5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b04f5-133">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="b04f5-133">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="b04f5-134">Выполнение привилегированных операций</span><span class="sxs-lookup"><span data-stu-id="b04f5-134">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> </dl>

 

 
