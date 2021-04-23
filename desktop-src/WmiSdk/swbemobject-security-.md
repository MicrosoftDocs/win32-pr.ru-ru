---
description: Свойство безопасности \_ объекта SWbemObject используется для чтения или установки параметров безопасности для объекта SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: Свойство SWbemObject.Security_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349222"
---
# <a name="swbemobjectsecurity_-property"></a><span data-ttu-id="a7ceb-103">SWbemObject. Security, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="a7ceb-103">SWbemObject.Security\_ property</span></span>

<span data-ttu-id="a7ceb-104">Свойство **безопасности \_** объекта [**SWbemObject**](swbemobject.md) используется для чтения или установки параметров безопасности для объекта **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="a7ceb-104">The **Security\_** property of the [**SWbemObject**](swbemobject.md) object is used to read, or set the security settings for an **SWbemObject** object.</span></span> <span data-ttu-id="a7ceb-105">Это свойство является объектом [**свбемсекурити**](swbemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="a7ceb-105">This property is an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="a7ceb-106">Параметры безопасности в этом объекте не указывают параметры проверки подлинности, олицетворения или привилегии, сделанные для подключения к инструментарий управления Windows (WMI) (WMI), или безопасность, действующая для прокси-сервера, когда объект доставляется в приемник при асинхронном вызове.</span><span class="sxs-lookup"><span data-stu-id="a7ceb-106">The security settings in this object do not indicate the authentication, impersonation, or privilege settings made on a connection to Windows Management Instrumentation (WMI), or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="a7ceb-107">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="a7ceb-107">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

> [!Note]  
> <span data-ttu-id="a7ceb-108">Установка свойства **безопасности \_** объекта [**SWbemObject**](swbemobject.md) в **значение NULL** предоставляет всем всем времени неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="a7ceb-108">Setting the **Security\_** property of an [**SWbemObject**](swbemobject.md) object to **NULL** grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="a7ceb-109">Дополнительные сведения см. в разделе [**свбемсекурити**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="a7ceb-109">For more information, see [**SWbemSecurity**](swbemsecurity.md).</span></span>

 

<span data-ttu-id="a7ceb-110">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a7ceb-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="a7ceb-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a7ceb-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ceb-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7ceb-112">Syntax</span></span>


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a><span data-ttu-id="a7ceb-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a7ceb-113">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ceb-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a7ceb-114">Requirements</span></span>



| <span data-ttu-id="a7ceb-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a7ceb-115">Requirement</span></span> | <span data-ttu-id="a7ceb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a7ceb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ceb-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7ceb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ceb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7ceb-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7ceb-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7ceb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ceb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7ceb-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7ceb-121">Header</span><span class="sxs-lookup"><span data-stu-id="a7ceb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7ceb-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7ceb-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7ceb-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a7ceb-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="a7ceb-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a7ceb-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a7ceb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ceb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7ceb-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7ceb-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7ceb-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="a7ceb-127">CLSID</span></span><br/>                    | <span data-ttu-id="a7ceb-128">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="a7ceb-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="a7ceb-129">IID</span><span class="sxs-lookup"><span data-stu-id="a7ceb-129">IID</span></span><br/>                      | <span data-ttu-id="a7ceb-130">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="a7ceb-130">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="a7ceb-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7ceb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ceb-132">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="a7ceb-132">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="a7ceb-133">Создание приложения или скрипта WMI</span><span class="sxs-lookup"><span data-stu-id="a7ceb-133">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="a7ceb-134">Настройка \_ \_ безопасности процесса клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="a7ceb-134">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="a7ceb-135">**свбемсекурити**</span><span class="sxs-lookup"><span data-stu-id="a7ceb-135">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="a7ceb-136">**вбемаусентикатионлевеленум**</span><span class="sxs-lookup"><span data-stu-id="a7ceb-136">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="a7ceb-137">**вбемимперсонатионлевеленум**</span><span class="sxs-lookup"><span data-stu-id="a7ceb-137">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="a7ceb-138">**вбемпривилежеенум**</span><span class="sxs-lookup"><span data-stu-id="a7ceb-138">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="a7ceb-139">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="a7ceb-139">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 




