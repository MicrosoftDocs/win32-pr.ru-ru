---
description: Свойство Аусентикатионлевел — это целое число, определяющее уровень проверки подлинности COM, назначенный этому объекту.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Свбемсекурити. Аусентикатионлевел, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344712"
---
# <a name="swbemsecurityauthenticationlevel-property"></a><span data-ttu-id="5c049-103">Свбемсекурити. Аусентикатионлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="5c049-103">SWbemSecurity.AuthenticationLevel property</span></span>

<span data-ttu-id="5c049-104">Свойство **аусентикатионлевел** — это целое число, определяющее уровень проверки подлинности COM, назначенный этому объекту.</span><span class="sxs-lookup"><span data-stu-id="5c049-104">The **AuthenticationLevel** property is an integer that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="5c049-105">Этот параметр определяет, как вы защищаете данные, отправляемые из WMI.</span><span class="sxs-lookup"><span data-stu-id="5c049-105">This setting determines how you protect information sent from WMI.</span></span> <span data-ttu-id="5c049-106">Дополнительные сведения об уровнях проверки подлинности см. в разделе [Установка параметров \_ \_ безопасности процессов для клиентских приложений](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="5c049-106">For more information about authentication levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="5c049-107">Как правило, при выполнении вызовов API WMI не требуется устанавливать уровень проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5c049-107">In general, it is not necessary to set the authentication level when making WMI API calls.</span></span> <span data-ttu-id="5c049-108">Если это свойство не задано, используется уровень проверки подлинности COM по умолчанию для системы.</span><span class="sxs-lookup"><span data-stu-id="5c049-108">If you do not set this property, the default COM Authentication level for your system is used.</span></span>

<span data-ttu-id="5c049-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5c049-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5c049-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5c049-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c049-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c049-111">Syntax</span></span>


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="5c049-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5c049-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5c049-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5c049-113">Remarks</span></span>

<span data-ttu-id="5c049-114">Параметр Аусентикатионлевел позволяет запрашивать уровень проверки подлинности и конфиденциальности DCOM для использования в рамках всего соединения.</span><span class="sxs-lookup"><span data-stu-id="5c049-114">The authenticationLevel setting enables you to request the level of DCOM authentication and privacy to be used throughout a connection.</span></span> <span data-ttu-id="5c049-115">Параметры находятся в диапазоне от без проверки подлинности до зашифрованной проверки подлинности для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="5c049-115">Settings range from no authentication to per-packet encrypted authentication.</span></span>



| <span data-ttu-id="5c049-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5c049-116">Value</span></span>        | <span data-ttu-id="5c049-117">Описание</span><span class="sxs-lookup"><span data-stu-id="5c049-117">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c049-118">Нет</span><span class="sxs-lookup"><span data-stu-id="5c049-118">None</span></span>         | <span data-ttu-id="5c049-119">Не использует проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="5c049-119">Does not use any authentication.</span></span> <span data-ttu-id="5c049-120">Все параметры безопасности игнорируются.</span><span class="sxs-lookup"><span data-stu-id="5c049-120">All security settings are ignored.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="5c049-121">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5c049-121">Default</span></span>      | <span data-ttu-id="5c049-122">Использует стандартное согласование безопасности для выбора уровня проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5c049-122">Uses a standard security negotiation to select an authentication level.</span></span> <span data-ttu-id="5c049-123">Это рекомендуемый параметр, так как клиент, вовлеченный в транзакцию, будет согласовываться с уровнем проверки подлинности, указанным на сервере.</span><span class="sxs-lookup"><span data-stu-id="5c049-123">This is the recommended setting because the client involved in the transaction will be negotiated to the authentication level specified by the server.</span></span><br/> <span data-ttu-id="5c049-124">DCOM не будет выбирать значение None во время сеанса согласования.</span><span class="sxs-lookup"><span data-stu-id="5c049-124">DCOM will not select the value None during a negotiation session.</span></span><br/> |
| <span data-ttu-id="5c049-125">Подключение</span><span class="sxs-lookup"><span data-stu-id="5c049-125">Connect</span></span>      | <span data-ttu-id="5c049-126">Проверяет подлинность учетных данных клиента только в том случае, если клиент пытается подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="5c049-126">Authenticates the credentials of the client only when the client tries to connect to the server.</span></span> <span data-ttu-id="5c049-127">После установки соединения дополнительные проверки подлинности не выполняются.</span><span class="sxs-lookup"><span data-stu-id="5c049-127">After a connection has been made, no additional authentication checks take place.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="5c049-128">Вызов</span><span class="sxs-lookup"><span data-stu-id="5c049-128">Call</span></span>         | <span data-ttu-id="5c049-129">Проверяет подлинность учетных данных клиента только в начале каждого вызова, когда сервер получает запрос.</span><span class="sxs-lookup"><span data-stu-id="5c049-129">Authenticates the credentials of the client only at the beginning of each call, when the server receives the request.</span></span> <span data-ttu-id="5c049-130">Заголовки пакетов подписываются, но пакеты данных, которыми обмениваются клиент и сервер, не подписываются и не шифруются.</span><span class="sxs-lookup"><span data-stu-id="5c049-130">The packet headers are signed, but the data packets exchanged between the client and the server are neither signed nor encrypted.</span></span><br/>                                                     |
| <span data-ttu-id="5c049-131">PKT</span><span class="sxs-lookup"><span data-stu-id="5c049-131">Pkt</span></span>          | <span data-ttu-id="5c049-132">Проверяет, что все пакеты данных получены от ожидаемого клиента.</span><span class="sxs-lookup"><span data-stu-id="5c049-132">Authenticates that all data packets are received from the expected client.</span></span> <span data-ttu-id="5c049-133">Аналогично вызову; заголовки пакетов подписываются, но не шифруются.</span><span class="sxs-lookup"><span data-stu-id="5c049-133">Similar to Call; packet headers are signed but not encrypted.</span></span> <span data-ttu-id="5c049-134">Сами пакеты не подписаны и не зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="5c049-134">Packets themselves are neither signed nor encrypted.</span></span><br/>                                                                                                               |
| <span data-ttu-id="5c049-135">пктинтегрити</span><span class="sxs-lookup"><span data-stu-id="5c049-135">PktIntegrity</span></span> | <span data-ttu-id="5c049-136">Проверка подлинности и проверка того, что ни один из пакетов данных, передаваемых между клиентом и сервером, не был изменен.</span><span class="sxs-lookup"><span data-stu-id="5c049-136">Authenticates and verifies that none of the data packets transferred between the client and the server have been modified.</span></span> <span data-ttu-id="5c049-137">Каждый пакет данных подписывается, гарантируя, что пакеты не были изменены во время передачи.</span><span class="sxs-lookup"><span data-stu-id="5c049-137">Every data packet is signed, ensuring that the packets have not been modified during transit.</span></span> <span data-ttu-id="5c049-138">Ни один из пакетов данных не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="5c049-138">None of the data packets are encrypted.</span></span><br/>                                            |
| <span data-ttu-id="5c049-139">пктприваци</span><span class="sxs-lookup"><span data-stu-id="5c049-139">PktPrivacy</span></span>   | <span data-ttu-id="5c049-140">Проверяет подлинность всех предыдущих уровней олицетворения и подписывает и шифрует каждый пакет данных.</span><span class="sxs-lookup"><span data-stu-id="5c049-140">Authenticates all previous impersonation levels and signs and encrypts each data packet.</span></span> <span data-ttu-id="5c049-141">Это гарантирует, что весь обмен данными между клиентом и сервером будет конфиденциальным.</span><span class="sxs-lookup"><span data-stu-id="5c049-141">This ensures that all communication between the client and the server is confidential.</span></span><br/>                                                                                                                             |



 

<span data-ttu-id="5c049-142">Можно задать уровень проверки подлинности объектов [**SwbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**Свбемобжектпас**](swbemobjectpath.md)и [**SwbemLocator**](swbemlocator.md) , задав для свойства **аусентикатионлевел** нужное значение.</span><span class="sxs-lookup"><span data-stu-id="5c049-142">You can set the authentication level of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by setting the **AuthenticationLevel** property to the desired value.</span></span>

<span data-ttu-id="5c049-143">В следующем примере показано, как задать уровень проверки подлинности для объекта **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="5c049-143">The following example shows how to set the authentication level for an **SwbemObject** object.</span></span>


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



<span data-ttu-id="5c049-144">Можно также указать уровни проверки подлинности как часть моникера.</span><span class="sxs-lookup"><span data-stu-id="5c049-144">You can also specify authentication levels as part of a moniker.</span></span> <span data-ttu-id="5c049-145">В следующем примере задается уровень проверки подлинности и уровень олицетворения, а также извлекается экземпляр [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="5c049-145">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a><span data-ttu-id="5c049-146">Требования</span><span class="sxs-lookup"><span data-stu-id="5c049-146">Requirements</span></span>



| <span data-ttu-id="5c049-147">Требование</span><span class="sxs-lookup"><span data-stu-id="5c049-147">Requirement</span></span> | <span data-ttu-id="5c049-148">Значение</span><span class="sxs-lookup"><span data-stu-id="5c049-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c049-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c049-149">Minimum supported client</span></span><br/> | <span data-ttu-id="5c049-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c049-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c049-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c049-151">Minimum supported server</span></span><br/> | <span data-ttu-id="5c049-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c049-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c049-153">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5c049-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c049-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c049-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c049-155">DLL</span><span class="sxs-lookup"><span data-stu-id="5c049-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c049-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c049-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c049-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="5c049-157">CLSID</span></span><br/>                    | <span data-ttu-id="5c049-158">\_СВБЕМСЕКУРИТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="5c049-158">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="5c049-159">IID</span><span class="sxs-lookup"><span data-stu-id="5c049-159">IID</span></span><br/>                      | <span data-ttu-id="5c049-160">IID \_ исвбемсекурити</span><span class="sxs-lookup"><span data-stu-id="5c049-160">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5c049-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c049-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c049-162">Настройка \_ \_ безопасности процесса клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="5c049-162">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="5c049-163">**вбемаусентикатионлевеленум**</span><span class="sxs-lookup"><span data-stu-id="5c049-163">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="5c049-164">**свбемсекурити**</span><span class="sxs-lookup"><span data-stu-id="5c049-164">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> </dl>

 

