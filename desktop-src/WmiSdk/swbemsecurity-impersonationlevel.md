---
description: Свойство Имперсонатионлевел — это целое число, определяющее уровень олицетворения COM, назначенный этому объекту.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Свбемсекурити. Имперсонатионлевел, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913360"
---
# <a name="swbemsecurityimpersonationlevel-property"></a><span data-ttu-id="5526c-103">Свбемсекурити. Имперсонатионлевел, свойство</span><span class="sxs-lookup"><span data-stu-id="5526c-103">SWbemSecurity.ImpersonationLevel property</span></span>

<span data-ttu-id="5526c-104">Свойство **имперсонатионлевел** — это целое число, определяющее уровень олицетворения COM, назначенный этому объекту.</span><span class="sxs-lookup"><span data-stu-id="5526c-104">The **ImpersonationLevel** property is an integer that defines the COM impersonation level that is assigned to this object.</span></span> <span data-ttu-id="5526c-105">Этот параметр определяет, могут ли процессы, принадлежащие инструментарий управления Windows (WMI) (WMI), обнаруживать или использовать учетные данные безопасности при вызове других процессов.</span><span class="sxs-lookup"><span data-stu-id="5526c-105">This setting determines if processes owned by Windows Management Instrumentation (WMI) can detect or use your security credentials when making calls to other processes.</span></span> <span data-ttu-id="5526c-106">Дополнительные сведения об уровнях олицетворения см. в разделе [Настройка \_ \_ безопасности процесса обработки клиентских приложений](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="5526c-106">For more information about impersonation levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="5526c-107">Если уровень олицетворения не задан специально в моникере или при установке свойства **свбемсекурити. имперсонатионлевел** защищаемого объекта, WMI устанавливает для уровня олицетворения по умолчанию значение, указанное в [разделе реестра уровня олицетворения по умолчанию](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="5526c-107">If you do not set the impersonation level specifically in either a moniker, or by setting the **SWBemSecurity.ImpersonationLevel** property on a securable object, WMI sets the default impersonation level to the value specified in the [default impersonation level registry key](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="5526c-108">Если этот параметр недостаточен, поставщик не будет обслуживать запрос, а вызов API WMI может завершиться с кодом ошибки **вбемерракцессдениед** (2147749891/0x80041003).</span><span class="sxs-lookup"><span data-stu-id="5526c-108">If this setting is not sufficient, the provider does not service your request, and the call to the WMI API can fail with an error code of **wbemErrAccessDenied** (2147749891/0x80041003).</span></span>

<span data-ttu-id="5526c-109">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5526c-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5526c-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5526c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5526c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5526c-111">Syntax</span></span>


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="5526c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5526c-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5526c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5526c-113">Remarks</span></span>

<span data-ttu-id="5526c-114">В качестве уровня олицетворения DCOM этому свойству может быть присвоено одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="5526c-114">As a DCOM impersonation level, this property can be set to one of the following values:</span></span>



| <span data-ttu-id="5526c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5526c-115">Value</span></span>           | <span data-ttu-id="5526c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5526c-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5526c-117">**Анонимный**</span><span class="sxs-lookup"><span data-stu-id="5526c-117">**Anonymous**</span></span>   | <span data-ttu-id="5526c-118">Скрывает учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="5526c-118">Hides the credentials of the caller.</span></span> <span data-ttu-id="5526c-119">Инструментарий WMI на самом деле не поддерживает этот уровень олицетворения. Если скрипт указывает Имперсонатионлевел = Anonymous, WMI автоматически обновит уровень олицетворения, чтобы он определялся.</span><span class="sxs-lookup"><span data-stu-id="5526c-119">WMI does not actually support this impersonation level; if a script specifies impersonationLevel=Anonymous, WMI will silently upgrade the impersonation level to Identify.</span></span> <span data-ttu-id="5526c-120">Тем не менее, это может быть вызвано небессмысленным упражнением, так как сценарии, использующие уровень Identify, скорее всего, завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5526c-120">This is in some ways a meaningless exercise, however, because scripts using the Identify level are likely to fail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="5526c-121">**Указывается**</span><span class="sxs-lookup"><span data-stu-id="5526c-121">**Identify**</span></span>    | <span data-ttu-id="5526c-122">Позволяет объектам запрашивать учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="5526c-122">Enables objects to query the credentials of the caller.</span></span> <span data-ttu-id="5526c-123">Вероятнее всего, скрипты, использующие этот уровень олицетворения, будут завершаться ошибкой. уровень Identify обычно позволяет не только проверять списки управления доступом.</span><span class="sxs-lookup"><span data-stu-id="5526c-123">Scripts using this impersonation level are likely to fail; the Identify level typically lets you do no more than check access control lists.</span></span> <span data-ttu-id="5526c-124">Вы не сможете выполнять сценарии на удаленных компьютерах с помощью команды Identify.</span><span class="sxs-lookup"><span data-stu-id="5526c-124">You will not be able to run scripts against remote computers using Identify.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="5526c-125">**Impersonate**</span><span class="sxs-lookup"><span data-stu-id="5526c-125">**Impersonate**</span></span> | <span data-ttu-id="5526c-126">Позволяет объектам использовать учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="5526c-126">Enables objects to use the credentials of the caller.</span></span> <span data-ttu-id="5526c-127">Рекомендуется использовать этот уровень олицетворения с помощью скриптов WMI.</span><span class="sxs-lookup"><span data-stu-id="5526c-127">It is recommended that you use this impersonation level with WMI scripts.</span></span> <span data-ttu-id="5526c-128">При этом сценарий WMI будет использовать ваши учетные данные пользователя. в результате он сможет выполнять любые задачи, которые вы можете выполнить.</span><span class="sxs-lookup"><span data-stu-id="5526c-128">When you do so, the WMI script will use your user credentials; as a result, it will be able to perform any tasks that you are able to perform.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="5526c-129">**Делегат**</span><span class="sxs-lookup"><span data-stu-id="5526c-129">**Delegate**</span></span>    | <span data-ttu-id="5526c-130">Позволяет объектам разрешающим другим объектам использовать учетные данные вызывающей стороны.</span><span class="sxs-lookup"><span data-stu-id="5526c-130">Enables objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="5526c-131">Делегирование позволяет сценарию использовать ваши учетные данные на удаленном компьютере, а затем позволяет этому удаленному компьютеру использовать ваши учетные данные на другом удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5526c-131">Delegation allows a script to use your credentials on a remote computer and then enables that remote computer to use your credentials on another remote computer.</span></span> <span data-ttu-id="5526c-132">Хотя этот уровень олицетворения можно использовать в сценариях WMI, это необходимо сделать только при необходимости, так как это может представлять угрозу безопасности.</span><span class="sxs-lookup"><span data-stu-id="5526c-132">While you can use this impersonation level within WMI scripts, you should do so only if necessary because it might pose a security risk.</span></span><br/> <span data-ttu-id="5526c-133">Нельзя использовать уровень олицетворения делегирования, если все учетные записи пользователей и компьютеры, вовлеченные в транзакцию, не помечены как доверенные для делегирования в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5526c-133">You cannot use the Delegate impersonation level unless all the user accounts and computer accounts involved in the transaction have all been marked as Trusted for delegation in Active Directory.</span></span> <span data-ttu-id="5526c-134">Это помогает снизить риски безопасности.</span><span class="sxs-lookup"><span data-stu-id="5526c-134">This helps minimize the security risks.</span></span> <span data-ttu-id="5526c-135">Хотя удаленный компьютер может использовать ваши учетные данные, он может сделать это только в том случае, если он и другие компьютеры, вовлеченные в транзакцию, являются доверенными для делегирования.</span><span class="sxs-lookup"><span data-stu-id="5526c-135">Although a remote computer can use your credentials, it can do so only if both it and any other computers involved in the transaction are trusted for delegation.</span></span><br/> |



 

<span data-ttu-id="5526c-136">Как уже отмечалось, анонимное олицетворение скрывает учетные данные и позволяет удаленному объекту запрашивать учетные данные, но удаленный объект не может олицетворять контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="5526c-136">As noted, Anonymous impersonation hides your credentials and Identify permits a remote object to query your credentials, but the remote object cannot impersonate your security context.</span></span> <span data-ttu-id="5526c-137">(Иными словами, несмотря на то, что удаленный объект знает, что у вас есть, он не может полагаться на вас.) Сценарии WMI, обращающиеся к удаленным компьютерам с помощью одного из этих двух параметров, обычно завершаются ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5526c-137">(In other words, although the remote object knows who you are, it cannot "pretend" to be you.) WMI scripts accessing remote computers using one of these two settings will generally fail.</span></span> <span data-ttu-id="5526c-138">На самом деле большинство сценариев, выполняемых на локальном компьютере с использованием одного из этих двух параметров, также завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="5526c-138">In fact, most scripts run on the local computer using one of these two settings will also fail.</span></span>

<span data-ttu-id="5526c-139">Олицетворение позволяет удаленной службе WMI использовать контекст безопасности для выполнения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="5526c-139">Impersonate permits the remote WMI service to use your security context to perform the requested operation.</span></span> <span data-ttu-id="5526c-140">Удаленный запрос WMI, использующий параметр олицетворения, обычно выполняется успешно, если учетные данные имеют достаточные привилегии для выполнения требуемой операции.</span><span class="sxs-lookup"><span data-stu-id="5526c-140">A remote WMI request that uses the Impersonate setting typically succeeds, provided your credentials have sufficient privileges to perform the intended operation.</span></span> <span data-ttu-id="5526c-141">Иными словами, вы не можете использовать инструментарий WMI для выполнения действий (удаленно или иным образом), которые не имеют разрешения на выполнение вне инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="5526c-141">In other words, you cannot use WMI to perform an action (remotely or otherwise) that you do not have permission to perform outside WMI.</span></span>

<span data-ttu-id="5526c-142">Установка параметра Имперсонатионлевел в значение Delegate позволяет удаленной службе WMI передавать ваши учетные данные другим объектам и обычно считается угрозой безопасности.</span><span class="sxs-lookup"><span data-stu-id="5526c-142">Setting impersonationLevel to Delegate permits the remote WMI service to pass your credentials on to other objects and is generally considered a security risk.</span></span>

<span data-ttu-id="5526c-143">Можно задать уровень олицетворения объекта [**SwbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**Свбемобжектпас**](swbemobjectpath.md)и [**SwbemLocator**](swbemlocator.md) , задав для свойства **имперсонатионлевел** нужное значение.</span><span class="sxs-lookup"><span data-stu-id="5526c-143">You can set the impersonation level of an [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) object by setting the **ImpersonationLevel** property to the desired value.</span></span> <span data-ttu-id="5526c-144">В следующем примере показано, как задать уровень олицетворения для объекта **SWbemObject** :</span><span class="sxs-lookup"><span data-stu-id="5526c-144">The following example shows you how to set the impersonation level for an **SWbemObject** object:</span></span>


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



<span data-ttu-id="5526c-145">Кроме того, можно указать уровни олицетворения как часть моникера.</span><span class="sxs-lookup"><span data-stu-id="5526c-145">You can also specify impersonation levels as part of a moniker.</span></span> <span data-ttu-id="5526c-146">В следующем примере задается уровень проверки подлинности и уровень олицетворения, а также извлекается экземпляр [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="5526c-146">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a><span data-ttu-id="5526c-147">Требования</span><span class="sxs-lookup"><span data-stu-id="5526c-147">Requirements</span></span>



| <span data-ttu-id="5526c-148">Требование</span><span class="sxs-lookup"><span data-stu-id="5526c-148">Requirement</span></span> | <span data-ttu-id="5526c-149">Значение</span><span class="sxs-lookup"><span data-stu-id="5526c-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5526c-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5526c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5526c-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5526c-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5526c-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5526c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5526c-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5526c-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5526c-154">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5526c-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="5526c-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5526c-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5526c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="5526c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5526c-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5526c-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5526c-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="5526c-158">CLSID</span></span><br/>                    | <span data-ttu-id="5526c-159">\_СВБЕМСЕКУРИТИ CLSID</span><span class="sxs-lookup"><span data-stu-id="5526c-159">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="5526c-160">IID</span><span class="sxs-lookup"><span data-stu-id="5526c-160">IID</span></span><br/>                      | <span data-ttu-id="5526c-161">IID \_ исвбемсекурити</span><span class="sxs-lookup"><span data-stu-id="5526c-161">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="5526c-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5526c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5526c-163">**свбемсекурити**</span><span class="sxs-lookup"><span data-stu-id="5526c-163">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="5526c-164">Настройка \_ \_ безопасности процесса клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="5526c-164">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="5526c-165">**вбемимперсонатионлевеленум**</span><span class="sxs-lookup"><span data-stu-id="5526c-165">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

