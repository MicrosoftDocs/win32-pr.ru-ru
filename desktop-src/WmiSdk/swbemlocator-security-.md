---
description: Свойство безопасности \_ объекта SWbemLocator используется для чтения или установки параметров безопасности объекта SWbemLocator. Это свойство является объектом Свбемсекурити.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: Свойство SWbemLocator.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812419"
---
# <a name="swbemlocatorsecurity_-property"></a><span data-ttu-id="fc20b-104">SWbemLocator. Security, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="fc20b-104">SWbemLocator.Security\_ property</span></span>

<span data-ttu-id="fc20b-105">Свойство **безопасности \_** объекта [**SWbemLocator**](swbemlocator.md) используется для чтения или установки параметров безопасности объекта **SWbemLocator** .</span><span class="sxs-lookup"><span data-stu-id="fc20b-105">The **Security\_** property of the [**SWbemLocator**](swbemlocator.md) object is used to read or set the security settings for an **SWbemLocator** object.</span></span> <span data-ttu-id="fc20b-106">Это свойство является объектом [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="fc20b-106">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="fc20b-107">Установка свойства **безопасности \_** объекта [**SWbemLocator**](swbemlocator.md) в **значение NULL** предоставляет всем пользователям неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="fc20b-107">Setting the **Security\_** property of an [**SWbemLocator**](swbemlocator.md) object to **NULL** grants unlimited access to everyone at all times.</span></span> <span data-ttu-id="fc20b-108">Дополнительные сведения см. в разделе [**свбемсекурити**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="fc20b-108">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="fc20b-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fc20b-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="fc20b-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fc20b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc20b-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc20b-111">Syntax</span></span>


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="fc20b-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fc20b-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="fc20b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc20b-113">Remarks</span></span>

<span data-ttu-id="fc20b-114">Свойства объекта **SWbemLocator. Security \_** не имеют значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fc20b-114">The properties of an **SWbemLocator.Security\_** object have no default values.</span></span> <span data-ttu-id="fc20b-115">Если вы попытаетесь получить значение [**свбемсекурити. аусентикатионлевел**](swbemsecurity-authenticationlevel.md) или [**свбемсекурити. Имперсонатионлевел**](swbemsecurity-impersonationlevel.md) в объекте [**SWbemLocator**](swbemlocator.md) , прежде чем приступать к его заданию, возникает ошибка [вбемеррфаилед](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) .</span><span class="sxs-lookup"><span data-stu-id="fc20b-115">If you attempt to get the value of [**SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) or [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) on an [**SWbemLocator**](swbemlocator.md) object before you have set it, an [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) error results.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc20b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="fc20b-116">Requirements</span></span>



| <span data-ttu-id="fc20b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="fc20b-117">Requirement</span></span> | <span data-ttu-id="fc20b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fc20b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc20b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc20b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc20b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc20b-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc20b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc20b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc20b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc20b-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc20b-123">Header</span><span class="sxs-lookup"><span data-stu-id="fc20b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc20b-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc20b-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fc20b-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fc20b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="fc20b-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fc20b-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fc20b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fc20b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc20b-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc20b-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fc20b-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="fc20b-129">CLSID</span></span><br/>                    | <span data-ttu-id="fc20b-130">\_SWBEMLOCATOR CLSID</span><span class="sxs-lookup"><span data-stu-id="fc20b-130">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="fc20b-131">IID</span><span class="sxs-lookup"><span data-stu-id="fc20b-131">IID</span></span><br/>                      | <span data-ttu-id="fc20b-132">IID \_ исвбемлокатор</span><span class="sxs-lookup"><span data-stu-id="fc20b-132">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="fc20b-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc20b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc20b-134">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="fc20b-134">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="fc20b-135">Создание приложения или скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="fc20b-135">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="fc20b-136">Выполнение привилегированных операций с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="fc20b-136">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="fc20b-137">Настройка \_ \_ безопасности процесса клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="fc20b-137">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="fc20b-138">**Объект Свбемсекурити**</span><span class="sxs-lookup"><span data-stu-id="fc20b-138">**SWbemSecurity object**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="fc20b-139">Защита удаленного WMI-подключения</span><span class="sxs-lookup"><span data-stu-id="fc20b-139">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




