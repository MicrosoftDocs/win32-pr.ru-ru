---
description: Объект Свбемсекурити Возвращает или задает параметры безопасности, такие как привилегии, олицетворения COM и уровни проверки подлинности, назначенные объекту.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Объект Свбемсекурити (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662729"
---
# <a name="swbemsecurity-object"></a><span data-ttu-id="84190-103">Объект Свбемсекурити</span><span class="sxs-lookup"><span data-stu-id="84190-103">SWbemSecurity object</span></span>

<span data-ttu-id="84190-104">Объект **свбемсекурити** Возвращает или задает параметры безопасности, такие как привилегии, олицетворения COM и уровни проверки подлинности, назначенные объекту.</span><span class="sxs-lookup"><span data-stu-id="84190-104">The **SWbemSecurity** object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.</span></span> <span data-ttu-id="84190-105">Объекты [**SWbemLocator**](swbemlocator.md), [**SwbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**свбемобжектпас**](swbemobjectpath.md), [**свбемластеррор**](swbemlasterror.md)и [**свбемевентсаурце**](swbemeventsource.md) имеют свойство **безопасности \_** , которое является объектом **свбемсекурити** .</span><span class="sxs-lookup"><span data-stu-id="84190-105">The [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md), and [**SWbemEventSource**](swbemeventsource.md) objects have a **Security\_** property, which is the **SWbemSecurity** object.</span></span> <span data-ttu-id="84190-106">При получении экземпляра или просмотре журнала безопасности WMI может потребоваться задать свойства объекта **безопасности \_** .</span><span class="sxs-lookup"><span data-stu-id="84190-106">When you retrieve an instance or view the WMI security log, you might need to set the properties of the **Security\_** object.</span></span>

<span data-ttu-id="84190-107">Вызов функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) VBScript не может создать объект безопасности.</span><span class="sxs-lookup"><span data-stu-id="84190-107">The VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call cannot create the Security object.</span></span> <span data-ttu-id="84190-108">Параметры безопасности в этом объекте не указывают параметры проверки подлинности, олицетворения или привилегии для соединения с WMI или безопасность, действующая для прокси-сервера, когда объект доставляется в приемник при асинхронном вызове.</span><span class="sxs-lookup"><span data-stu-id="84190-108">The security settings in this object do not identify the authentication, impersonation, or privilege settings on a connection to WMI, or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="84190-109">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="84190-109">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

## <a name="members"></a><span data-ttu-id="84190-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="84190-110">Members</span></span>

<span data-ttu-id="84190-111">Объект **свбемсекурити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="84190-111">The **SWbemSecurity** object has these types of members:</span></span>

-   [<span data-ttu-id="84190-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="84190-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="84190-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="84190-113">Properties</span></span>

<span data-ttu-id="84190-114">Объект **свбемсекурити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="84190-114">The **SWbemSecurity** object has these properties.</span></span>



| <span data-ttu-id="84190-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="84190-115">Property</span></span>                                                                    | <span data-ttu-id="84190-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="84190-116">Access type</span></span>           | <span data-ttu-id="84190-117">Описание</span><span class="sxs-lookup"><span data-stu-id="84190-117">Description</span></span>                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84190-118">**аусентикатионлевел**</span><span class="sxs-lookup"><span data-stu-id="84190-118">**AuthenticationLevel**</span></span>](swbemsecurity-authenticationlevel.md)<br/> | <span data-ttu-id="84190-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="84190-119">Read/write</span></span><br/> | <span data-ttu-id="84190-120">Числовое значение, определяющее уровень проверки подлинности COM, назначенный этому объекту.</span><span class="sxs-lookup"><span data-stu-id="84190-120">Numeric value that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="84190-121">Этот параметр определяет, как вы защищаете данные, отправляемые из WMI.</span><span class="sxs-lookup"><span data-stu-id="84190-121">This setting determines how you protect information sent from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="84190-122">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="84190-122">**ImpersonationLevel**</span></span>](swbemsecurity-impersonationlevel.md)<br/>   | <span data-ttu-id="84190-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="84190-123">Read/write</span></span><br/> | <span data-ttu-id="84190-124">Числовое значение, определяющее уровень олицетворения COM, назначенный этому объекту.</span><span class="sxs-lookup"><span data-stu-id="84190-124">Numeric value that defines the COM Impersonation level that is assigned to this object.</span></span> <span data-ttu-id="84190-125">Этот параметр определяет, могут ли процессы, которыми владеет WMI, обнаруживать или использовать учетные данные безопасности при вызове других процессов.</span><span class="sxs-lookup"><span data-stu-id="84190-125">This setting determines if processes owned by WMI can detect or use your security credentials when making calls to other processes.</span></span><br/> |
| [<span data-ttu-id="84190-126">**Права**</span><span class="sxs-lookup"><span data-stu-id="84190-126">**Privileges**</span></span>](swbemsecurity-privileges.md)<br/>                   | <span data-ttu-id="84190-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="84190-127">Read-only</span></span><br/>  | <span data-ttu-id="84190-128">Объект [**свбемпривилежесет**](swbemprivilegeset.md) , определяющий привилегии для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="84190-128">An [**SWbemPrivilegeSet**](swbemprivilegeset.md) object that defines privileges for this object.</span></span> <span data-ttu-id="84190-129">Дополнительные сведения см. [в разделе выполнение с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="84190-129">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="84190-130">Требования</span><span class="sxs-lookup"><span data-stu-id="84190-130">Requirements</span></span>



| <span data-ttu-id="84190-131">Требование</span><span class="sxs-lookup"><span data-stu-id="84190-131">Requirement</span></span> | <span data-ttu-id="84190-132">Значение</span><span class="sxs-lookup"><span data-stu-id="84190-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84190-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84190-133">Minimum supported client</span></span><br/> | <span data-ttu-id="84190-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84190-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84190-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84190-135">Minimum supported server</span></span><br/> | <span data-ttu-id="84190-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84190-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84190-137">Header</span><span class="sxs-lookup"><span data-stu-id="84190-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="84190-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="84190-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="84190-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="84190-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="84190-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="84190-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="84190-141">DLL</span><span class="sxs-lookup"><span data-stu-id="84190-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84190-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84190-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="84190-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="84190-143">CLSID</span></span><br/>                    | <span data-ttu-id="84190-144">\_СВБЕМСЕКУРИТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="84190-144">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="84190-145">IID</span><span class="sxs-lookup"><span data-stu-id="84190-145">IID</span></span><br/>                      | <span data-ttu-id="84190-146">IID \_ исвбемсекурити</span><span class="sxs-lookup"><span data-stu-id="84190-146">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="84190-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84190-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84190-148">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="84190-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="84190-149">Поддержание безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="84190-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="84190-150">Настройка \_ \_ безопасности процесса клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="84190-150">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="84190-151">**вбемаусентикатионлевеленум**</span><span class="sxs-lookup"><span data-stu-id="84190-151">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="84190-152">**вбемимперсонатионлевеленум**</span><span class="sxs-lookup"><span data-stu-id="84190-152">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="84190-153">**вбемпривилежеенум**</span><span class="sxs-lookup"><span data-stu-id="84190-153">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

