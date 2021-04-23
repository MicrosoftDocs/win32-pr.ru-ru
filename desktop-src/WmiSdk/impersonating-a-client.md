---
description: Когда пользовательское приложение запрашивает данные из объектов в системе через поставщик WMI, олицетворение означает, что поставщик представляет учетные данные, представляющие уровень безопасности клиентов, а не поставщики.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Олицетворение клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911507"
---
# <a name="impersonating-a-client"></a><span data-ttu-id="ace0b-103">Олицетворение клиента</span><span class="sxs-lookup"><span data-stu-id="ace0b-103">Impersonating a Client</span></span>

<span data-ttu-id="ace0b-104">Когда пользовательское приложение запрашивает данные из объектов в системе через поставщик WMI, олицетворение означает, что поставщик представляет учетные данные, представляющие уровень безопасности клиента, а не поставщика.</span><span class="sxs-lookup"><span data-stu-id="ace0b-104">When a user application requests data from objects on the system through a WMI provider, impersonation means the provider presents credentials that represent the client's security level rather than the provider's.</span></span> <span data-ttu-id="ace0b-105">Олицетворение не позволяет клиенту получить несанкционированный доступ к информации в системе.</span><span class="sxs-lookup"><span data-stu-id="ace0b-105">Impersonation prevents a client from obtaining unauthorized access to information on the system.</span></span>

<span data-ttu-id="ace0b-106">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="ace0b-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="ace0b-107">Регистрация поставщика для олицетворения</span><span class="sxs-lookup"><span data-stu-id="ace0b-107">Registering a Provider for Impersonation</span></span>](#registering-a-provider-for-impersonation)
-   [<span data-ttu-id="ace0b-108">Настройка уровней олицетворения в поставщике</span><span class="sxs-lookup"><span data-stu-id="ace0b-108">Setting Impersonation Levels Within a Provider</span></span>](#setting-impersonation-levels-within-a-provider)
-   [<span data-ttu-id="ace0b-109">Обслуживание уровней безопасности в поставщике</span><span class="sxs-lookup"><span data-stu-id="ace0b-109">Maintaining Security Levels in a Provider</span></span>](#maintaining-security-levels-in-a-provider)
-   [<span data-ttu-id="ace0b-110">Обработка сообщений об отказе в доступе в поставщике</span><span class="sxs-lookup"><span data-stu-id="ace0b-110">Handling Access Denied Messages in a Provider</span></span>](#handling-access-denied-messages-in-a-provider)
-   [<span data-ttu-id="ace0b-111">Создание отчетов с частичными экземплярами</span><span class="sxs-lookup"><span data-stu-id="ace0b-111">Reporting Partial Instances</span></span>](#reporting-partial-instances)
-   [<span data-ttu-id="ace0b-112">Создание отчетов о частичном перечислении</span><span class="sxs-lookup"><span data-stu-id="ace0b-112">Reporting Partial Enumerations</span></span>](#reporting-partial-enumerations)
-   [<span data-ttu-id="ace0b-113">Отладка кода, которым запрещен доступ</span><span class="sxs-lookup"><span data-stu-id="ace0b-113">Debugging Your Access Denied Code</span></span>](#debugging-your-access-denied-code)
-   [<span data-ttu-id="ace0b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="ace0b-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="ace0b-115">Как правило, WMI работает как административная служба на высоком уровне безопасности с помощью контекста безопасности Локалсервер.</span><span class="sxs-lookup"><span data-stu-id="ace0b-115">WMI typically runs as an administrative service at a high security level, using the LocalServer security context.</span></span> <span data-ttu-id="ace0b-116">Использование административной службы предоставляет инструментарию WMI средства для доступа к привилегированным сведениям.</span><span class="sxs-lookup"><span data-stu-id="ace0b-116">Using an administrative service gives WMI the means to access privileged information.</span></span> <span data-ttu-id="ace0b-117">При вызове поставщика для получения сведений Инструментарий WMI передает ему идентификатор безопасности (SID), позволяя поставщику получить доступ к информации на том же высоком уровне безопасности.</span><span class="sxs-lookup"><span data-stu-id="ace0b-117">When calling a provider for information, WMI passes its security identifier (SID) to the provider, enabling the provider to access information at the same high security level.</span></span>

<span data-ttu-id="ace0b-118">В процессе запуска приложения WMI операционная система Windows предоставляет приложению WMI контекст безопасности пользователя, запустившего процесс.</span><span class="sxs-lookup"><span data-stu-id="ace0b-118">During the WMI application launch process, the Windows operating system gives the WMI application the security context of the user who began the process.</span></span> <span data-ttu-id="ace0b-119">Контекст безопасности пользователя обычно является более низким уровнем безопасности, чем Локалсервер, поэтому пользователь может не иметь разрешения на доступ ко всей информации, доступной инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="ace0b-119">The security context of the user is typically a lower security level than LocalServer, so the user may not have permission to access all of the information available to WMI.</span></span> <span data-ttu-id="ace0b-120">Когда пользовательское приложение запрашивает динамическую информацию, Инструментарий WMI передает идентификатор безопасности пользователя соответствующему поставщику.</span><span class="sxs-lookup"><span data-stu-id="ace0b-120">When the user application asks for dynamic information, WMI passes the SID of the user to the corresponding provider.</span></span> <span data-ttu-id="ace0b-121">При соответствующей записи поставщик пытается получить доступ к информации с помощью идентификатора безопасности пользователя, а не идентификатора безопасности поставщика.</span><span class="sxs-lookup"><span data-stu-id="ace0b-121">If written appropriately, the provider attempts to access information with the user SID, rather than the provider SID.</span></span>

<span data-ttu-id="ace0b-122">Чтобы поставщик был успешно олицетворять клиентское приложение, клиентское приложение и поставщик должны удовлетворять следующим критериям.</span><span class="sxs-lookup"><span data-stu-id="ace0b-122">For the provider to successfully impersonate the client application, the client application and provider must meet the following criteria:</span></span>

-   <span data-ttu-id="ace0b-123">Клиентское приложение должно вызывать WMI с уровнем безопасности "COM-подключение" на уровне "RPC c", " **\_ \_ \_ \_ impersonate** " или " **RPC c" на \_ \_ \_ уровне \_ Imp**.</span><span class="sxs-lookup"><span data-stu-id="ace0b-123">The client application must call WMI with a COM connection security level of **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** or **RPC\_C\_IMP\_LEVEL\_DELEGATE**.</span></span> <span data-ttu-id="ace0b-124">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="ace0b-124">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>
-   <span data-ttu-id="ace0b-125">Поставщик должен зарегистрироваться в WMI как поставщик олицетворения.</span><span class="sxs-lookup"><span data-stu-id="ace0b-125">The provider must register with WMI as an impersonation provider.</span></span> <span data-ttu-id="ace0b-126">Дополнительные сведения см. [в разделе Регистрация поставщика для олицетворения](#registering-a-provider-for-impersonation).</span><span class="sxs-lookup"><span data-stu-id="ace0b-126">For more information, see [Registering a Provider for Impersonation](#registering-a-provider-for-impersonation).</span></span>
-   <span data-ttu-id="ace0b-127">Перед доступом к привилегированным сведениям поставщик должен переключиться на уровень безопасности клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ace0b-127">The provider must switch to the security level of the client application before accessing privileged information.</span></span> <span data-ttu-id="ace0b-128">Дополнительные сведения см. [в разделе Настройка уровней олицетворения в поставщике](#setting-impersonation-levels-within-a-provider).</span><span class="sxs-lookup"><span data-stu-id="ace0b-128">For more information, see [Setting Impersonation Levels Within a Provider](#setting-impersonation-levels-within-a-provider).</span></span>
-   <span data-ttu-id="ace0b-129">Поставщик должен правильно обрабатывал ошибки, если доступ к этим данным запрещен.</span><span class="sxs-lookup"><span data-stu-id="ace0b-129">The provider must correctly handle error conditions if access to this information is denied.</span></span> <span data-ttu-id="ace0b-130">Дополнительные сведения см. [в разделе Обработка сообщений с запретом доступа в поставщике](#handling-access-denied-messages-in-a-provider).</span><span class="sxs-lookup"><span data-stu-id="ace0b-130">For more information, see [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).</span></span>

## <a name="registering-a-provider-for-impersonation"></a><span data-ttu-id="ace0b-131">Регистрация поставщика для олицетворения</span><span class="sxs-lookup"><span data-stu-id="ace0b-131">Registering a Provider for Impersonation</span></span>

<span data-ttu-id="ace0b-132">Инструментарий WMI передает только идентификатор безопасности клиентского приложения поставщикам, зарегистрированным в качестве поставщиков олицетворения.</span><span class="sxs-lookup"><span data-stu-id="ace0b-132">WMI only passes the SID of a client application to providers who have registered as impersonation providers.</span></span> <span data-ttu-id="ace0b-133">Чтобы разрешить поставщику выполнять олицетворение, необходимо изменить процесс регистрации поставщика.</span><span class="sxs-lookup"><span data-stu-id="ace0b-133">Enabling a provider to perform impersonation requires that you modify the provider registration process.</span></span>

<span data-ttu-id="ace0b-134">В следующей процедуре описывается регистрация поставщика для олицетворения.</span><span class="sxs-lookup"><span data-stu-id="ace0b-134">The following procedure describes how to register a provider for impersonation.</span></span> <span data-ttu-id="ace0b-135">Процедура предполагает, что вы уже понимаете процесс регистрации.</span><span class="sxs-lookup"><span data-stu-id="ace0b-135">The procedure assumes that you already understand the registration process.</span></span> <span data-ttu-id="ace0b-136">Дополнительные сведения о процессе регистрации см. в разделе [Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ace0b-136">For more information about the registration process, see [Registering a Provider](registering-a-provider.md).</span></span>

<span data-ttu-id="ace0b-137">**Регистрация поставщика для олицетворения**</span><span class="sxs-lookup"><span data-stu-id="ace0b-137">**To register a provider for impersonation**</span></span>

1.  <span data-ttu-id="ace0b-138">Установите свойство [**имперсонатионлевел**](swbemsecurity-impersonationlevel.md) класса [**\_ \_ Win32Provider**](--win32provider.md) , который представляет поставщика, в значение 1.</span><span class="sxs-lookup"><span data-stu-id="ace0b-138">Set the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property of the [**\_\_Win32Provider**](--win32provider.md) class that represents your provider to 1.</span></span>

    <span data-ttu-id="ace0b-139">Свойство [**имперсонатионлевел**](swbemsecurity-impersonationlevel.md) документирует, поддерживает ли поставщик олицетворение.</span><span class="sxs-lookup"><span data-stu-id="ace0b-139">The [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property documents whether the provider supports impersonation or not.</span></span> <span data-ttu-id="ace0b-140">Установка значения 0 для **имперсонатионлевел** указывает, что поставщик не олицетворяет клиента и выполняет все запрошенные операции в том же контексте пользователя, что и WMI.</span><span class="sxs-lookup"><span data-stu-id="ace0b-140">Setting **ImpersonationLevel** to 0 indicates that the provider does not impersonate the client and performs all requested operations in the same user context as WMI.</span></span> <span data-ttu-id="ace0b-141">Установка значения 1 для **имперсонатионлевел** указывает, что поставщик использует вызовы олицетворения для проверки операций, выполняемых от имени клиента.</span><span class="sxs-lookup"><span data-stu-id="ace0b-141">Setting **ImpersonationLevel** to 1 indicates that the provider uses impersonation calls to check operations performed on behalf of the client.</span></span>

2.  <span data-ttu-id="ace0b-142">Задайте для свойства **перусеринитиализатион** одного и того же класса [**\_ \_ Win32Provider**](--win32provider.md) значение **true**.</span><span class="sxs-lookup"><span data-stu-id="ace0b-142">Set the **PerUserInitialization** property of the same [**\_\_Win32Provider**](--win32provider.md) class to **TRUE**.</span></span>

> [!Note]  
> <span data-ttu-id="ace0b-143">При регистрации поставщика со свойством [**\_ \_ Win32Provider**](--win32provider.md) **инитиализеасадминфирст** , установленным в **значение true**, поставщик использует токен безопасности потока уровня администрирования только на этапе инициализации.</span><span class="sxs-lookup"><span data-stu-id="ace0b-143">If you register a provider with the [**\_\_Win32Provider**](--win32provider.md) property **InitializeAsAdminFirst** set to **TRUE**, then the provider uses the administration-level thread security token only during the initialization phase.</span></span> <span data-ttu-id="ace0b-144">Хотя вызов [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) не завершается ошибкой, поставщик использует контекст безопасности WMI, а не клиент.</span><span class="sxs-lookup"><span data-stu-id="ace0b-144">While a call to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) does not fail, the provider uses the security context of WMI and not of the client.</span></span>

 

<span data-ttu-id="ace0b-145">В следующем примере кода показано, как зарегистрировать поставщик для олицетворения.</span><span class="sxs-lookup"><span data-stu-id="ace0b-145">The following code example shows how to register a provider for impersonation.</span></span>

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a><span data-ttu-id="ace0b-146">Настройка уровней олицетворения в поставщике</span><span class="sxs-lookup"><span data-stu-id="ace0b-146">Setting Impersonation Levels Within a Provider</span></span>

<span data-ttu-id="ace0b-147">При регистрации поставщика с помощью свойства класса [**\_ \_ Win32Provider**](--win32provider.md) [**имперсонатионлевел**](swbemsecurity-impersonationlevel.md) , установленного в значение 1, WMI вызывает поставщик для олицетворения различных клиентов.</span><span class="sxs-lookup"><span data-stu-id="ace0b-147">If you register a provider with the [**\_\_Win32Provider**](--win32provider.md) class property [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) set to 1, then WMI calls your provider to impersonate various clients.</span></span> <span data-ttu-id="ace0b-148">Чтобы обрабатывал эти вызовы, используйте функции COM [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) и [**кореверттоселф**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) в реализации интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="ace0b-148">To handle these calls, use the [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) COM functions in your implementation of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="ace0b-149">Функция [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) позволяет серверу олицетворять клиента, который сделал вызов.</span><span class="sxs-lookup"><span data-stu-id="ace0b-149">The [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) function allows a server to impersonate the client that made the call.</span></span> <span data-ttu-id="ace0b-150">Поместив вызов **коимперсонатеклиент** в свою реализацию [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), вы разрешаете поставщику установить маркер потока поставщика в соответствии с маркером потока клиента, а значит, олицетворять клиента.</span><span class="sxs-lookup"><span data-stu-id="ace0b-150">By placing a call to **CoImpersonateClient** into your implementation of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), you allow your provider to set the thread token of the provider to match the thread token of the client, and thus impersonate the client.</span></span> <span data-ttu-id="ace0b-151">Если не вызвать **коимперсонатеклиент**, поставщик выполняет код на уровне администратора безопасности, тем самым создавая потенциальную уязвимость безопасности.</span><span class="sxs-lookup"><span data-stu-id="ace0b-151">If you do not call **CoImpersonateClient**, your provider executes code at an administrator level of security, thereby creating a potential security vulnerability.</span></span> <span data-ttu-id="ace0b-152">Если поставщик временно должен работать от имени администратора или выполнить проверку доступа вручную, вызовите [**кореверттоселф**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="ace0b-152">If your provider temporarily needs to act as an administrator or perform the access check manually, then call [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span></span>

<span data-ttu-id="ace0b-153">В отличие от [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), [**кореверттоселф**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) является com-функцией, которая обрабатывает уровни олицетворения потоков.</span><span class="sxs-lookup"><span data-stu-id="ace0b-153">In contrast to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) is a COM function that handles thread impersonation levels.</span></span> <span data-ttu-id="ace0b-154">В этом случае **кореверттоселф** изменяет уровень олицетворения обратно на исходный параметр олицетворения.</span><span class="sxs-lookup"><span data-stu-id="ace0b-154">In this case, **CoRevertToSelf** changes the impersonation level back to the original impersonation setting.</span></span> <span data-ttu-id="ace0b-155">Как правило, поставщик изначально является администратором и перемещается между **коимперсонатеклиент** и **кореверттоселф** в зависимости от того, выполняется ли вызов, представляющий вызывающий объект, или его собственные вызовы.</span><span class="sxs-lookup"><span data-stu-id="ace0b-155">In general, the provider is initially an administrator and alternates between **CoImpersonateClient** and **CoRevertToSelf** depending on whether it is making a call that represents the caller or its own calls.</span></span> <span data-ttu-id="ace0b-156">Поставщик должен правильно размещать эти вызовы, чтобы не предоставлять конечному пользователю брешь в системе безопасности.</span><span class="sxs-lookup"><span data-stu-id="ace0b-156">It is the responsibility of the provider to place these calls correctly so as not to expose a security hole to the end user.</span></span> <span data-ttu-id="ace0b-157">Например, поставщик должен вызывать только собственные функции Windows в рамках последовательности кода с олицетворением.</span><span class="sxs-lookup"><span data-stu-id="ace0b-157">For example, the provider should only call native Windows functions within the impersonated code sequence.</span></span>

> [!Note]  
> <span data-ttu-id="ace0b-158">Назначение [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) и [**кореверттоселф**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) заключается в настройке безопасности для поставщика.</span><span class="sxs-lookup"><span data-stu-id="ace0b-158">The purpose of [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) is to set security for a provider.</span></span> <span data-ttu-id="ace0b-159">Если вы определили, что произошел сбой олицетворения, следует вернуть соответствующий код завершения в WMI через [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="ace0b-159">If you determine that your impersonation has failed, you should return an appropriate completion code to WMI through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="ace0b-160">Дополнительные сведения см. [в разделе Обработка сообщений с запретом доступа в поставщике](#handling-access-denied-messages-in-a-provider).</span><span class="sxs-lookup"><span data-stu-id="ace0b-160">For more information, see [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).</span></span>

 

## <a name="maintaining-security-levels-in-a-provider"></a><span data-ttu-id="ace0b-161">Обслуживание уровней безопасности в поставщике</span><span class="sxs-lookup"><span data-stu-id="ace0b-161">Maintaining Security Levels in a Provider</span></span>

<span data-ttu-id="ace0b-162">Поставщики не могут вызывать [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) один раз в реализации [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) и предполагают, что учетные данные олицетворения остаются на месте в течение срока действия поставщика.</span><span class="sxs-lookup"><span data-stu-id="ace0b-162">Providers cannot call [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) one time in an implementation of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) and assume that the impersonation credentials remain in place for the duration of the provider.</span></span> <span data-ttu-id="ace0b-163">Вместо этого вызывайте **коимперсонатеклиент** несколько раз во время реализации, чтобы предотвратить изменение учетных данных WMI.</span><span class="sxs-lookup"><span data-stu-id="ace0b-163">Instead, call **CoImpersonateClient** multiple times during the course of an implementation to keep WMI from changing the credentials.</span></span>

<span data-ttu-id="ace0b-164">Основная проблема при настройке олицетворения для поставщика — повторный вход.</span><span class="sxs-lookup"><span data-stu-id="ace0b-164">The main concern for setting impersonation for a provider is reentrancy.</span></span> <span data-ttu-id="ace0b-165">В этом контексте повторный вход происходит, когда поставщик вызывает WMI для получения сведений и ожидает, пока Инструментарий WMI не вернется к поставщику.</span><span class="sxs-lookup"><span data-stu-id="ace0b-165">In this context, reentrancy is when a provider makes a call to WMI for information and waits until WMI calls back into the provider.</span></span> <span data-ttu-id="ace0b-166">По сути, поток выполнения покидает код поставщика, только для повторного ввода кода в следующий день.</span><span class="sxs-lookup"><span data-stu-id="ace0b-166">In essence, the thread of execution leaves the provider code, only to reenter the code at a later date.</span></span> <span data-ttu-id="ace0b-167">Повторная запись является частью структуры модели COM и, как правило, не является проблемой.</span><span class="sxs-lookup"><span data-stu-id="ace0b-167">Reentry is a part of the design of COM, and is generally not a concern.</span></span> <span data-ttu-id="ace0b-168">Однако когда поток выполнения переходит в инструментарий WMI, поток принимает на себя уровни олицетворения WMI.</span><span class="sxs-lookup"><span data-stu-id="ace0b-168">However, when the thread of execution enters WMI, the thread takes on the impersonation levels of WMI.</span></span> <span data-ttu-id="ace0b-169">Когда поток возвращается поставщику, необходимо сбросить уровни олицетворения с помощью другого вызова [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).</span><span class="sxs-lookup"><span data-stu-id="ace0b-169">When the thread returns to the provider, you must reset the impersonation levels with another call to [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).</span></span>

<span data-ttu-id="ace0b-170">Чтобы защитить себя от брешей в системе безопасности поставщика, следует выполнять повторные вызовы в WMI только при олицетворении клиента.</span><span class="sxs-lookup"><span data-stu-id="ace0b-170">To protect yourself from security holes in your provider, you should make reentrant calls into WMI only while impersonating the client.</span></span> <span data-ttu-id="ace0b-171">То есть вызовы WMI должны быть сделаны после вызова [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) и перед вызовом [**кореверттоселф**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span><span class="sxs-lookup"><span data-stu-id="ace0b-171">That is, calls to WMI should be made after you call [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) and before you call [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).</span></span> <span data-ttu-id="ace0b-172">Так как **кореверттоселф** приводит к тому, что олицетворение устанавливается на уровне пользователя, то, как правило, используется учетная запись LocalSystem, повторное выполнение вызовов к инструментарию WMI после вызова **кореверттоселф** , может предоставить пользователю, а также все поставщики, вызываемые, гораздо больше возможностей, чем они должны быть.</span><span class="sxs-lookup"><span data-stu-id="ace0b-172">Because **CoRevertToSelf** causes the impersonation to be set to the user level WMI is running, generally LocalSystem, reentrant calls to WMI after calling **CoRevertToSelf** could give the user, and any providers called, a lot more capabilities than they should have.</span></span>

> [!Note]  
> <span data-ttu-id="ace0b-173">При вызове системной функции или другого метода интерфейса не гарантируется, что контекст вызова будет поддерживаться.</span><span class="sxs-lookup"><span data-stu-id="ace0b-173">If you call a system function or another interface method, the call context is not guaranteed to be maintained.</span></span>

 

## <a name="handling-access-denied-messages-in-a-provider"></a><span data-ttu-id="ace0b-174">Обработка сообщений об отказе в доступе в поставщике</span><span class="sxs-lookup"><span data-stu-id="ace0b-174">Handling Access Denied Messages in a Provider</span></span>

<span data-ttu-id="ace0b-175">Большинство сообщений об ошибках отказа в доступе появляются, когда клиент запрашивает класс или сведения, к которым у них нет доступа.</span><span class="sxs-lookup"><span data-stu-id="ace0b-175">Most Access Denied error messages appear when a client requests a class or information to which they do not have access.</span></span> <span data-ttu-id="ace0b-176">Если поставщик возвращает сообщение об ошибке отказа в доступе к инструментарию WMI и WMI передает его клиенту, клиент может определить, существует ли информация.</span><span class="sxs-lookup"><span data-stu-id="ace0b-176">If the provider returns an Access Denied error message to WMI and WMI passes this on to the client, the client can infer that the information exists.</span></span> <span data-ttu-id="ace0b-177">В некоторых случаях это может привести к нарушению безопасности.</span><span class="sxs-lookup"><span data-stu-id="ace0b-177">In some situations, this can be a breach of security.</span></span> <span data-ttu-id="ace0b-178">Поэтому поставщик не должен распространять сообщение клиенту.</span><span class="sxs-lookup"><span data-stu-id="ace0b-178">Therefore, your provider should not propagate the message to the client.</span></span> <span data-ttu-id="ace0b-179">Вместо этого набор классов, предоставленных поставщиком, не должен быть предоставлен.</span><span class="sxs-lookup"><span data-stu-id="ace0b-179">Instead, the set of classes that the provider would have supplied should not be exposed.</span></span> <span data-ttu-id="ace0b-180">Аналогичным образом, поставщик динамического экземпляра должен вызвать базовый источник данных, чтобы определить, как обрабатывать сообщения с запретом доступа.</span><span class="sxs-lookup"><span data-stu-id="ace0b-180">Similarly, a dynamic instance provider should call to the underlying data source to determine how to deal with Access Denied messages.</span></span> <span data-ttu-id="ace0b-181">Ответственность за репликацию этой философии в среду WMI несет поставщик.</span><span class="sxs-lookup"><span data-stu-id="ace0b-181">It is the responsibility of the provider to replicate that philosophy into the WMI environment.</span></span> <span data-ttu-id="ace0b-182">Дополнительные сведения см. в разделе [Создание отчетов с частичными экземплярами](#reporting-partial-instances) и [Создание отчетов о частичном перечислении](#reporting-partial-enumerations).</span><span class="sxs-lookup"><span data-stu-id="ace0b-182">For more information, see [Reporting Partial Instances](#reporting-partial-instances) and [Reporting Partial Enumerations](#reporting-partial-enumerations).</span></span>

<span data-ttu-id="ace0b-183">При определении того, как поставщик должен выполнять обработку сообщений об отказе в доступе, необходимо написать и отладить код.</span><span class="sxs-lookup"><span data-stu-id="ace0b-183">When you determine how your provider should handle Access Denied messages, you must write and debug your code.</span></span> <span data-ttu-id="ace0b-184">Во время отладки часто бывает удобно различать отработку отказа из-за недостаточного олицетворения и отказа из-за ошибки в коде.</span><span class="sxs-lookup"><span data-stu-id="ace0b-184">While debugging, it is often convenient to distinguish between a denial due to low impersonation, and a denial due to an error in your code.</span></span> <span data-ttu-id="ace0b-185">Для определения разницы можно использовать простой тест в коде.</span><span class="sxs-lookup"><span data-stu-id="ace0b-185">You can use a simple test in your code to determine the difference.</span></span> <span data-ttu-id="ace0b-186">Дополнительные сведения см. [в разделе Отладка кода, которым запрещен доступ](#debugging-your-access-denied-code).</span><span class="sxs-lookup"><span data-stu-id="ace0b-186">For more information, see [Debugging your Access Denied Code](#debugging-your-access-denied-code).</span></span>

## <a name="reporting-partial-instances"></a><span data-ttu-id="ace0b-187">Создание отчетов с частичными экземплярами</span><span class="sxs-lookup"><span data-stu-id="ace0b-187">Reporting Partial Instances</span></span>

<span data-ttu-id="ace0b-188">Одно из распространенных событий отказа в доступе заключается в том, что инструментарий WMI не может предоставить всю информацию для заполнения экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ace0b-188">One common occurrence of an Access Denied message is when WMI cannot provide all the information to fill an instance.</span></span> <span data-ttu-id="ace0b-189">Например, клиент может иметь полномочия на просмотр объекта жесткого диска, но может не иметь права видеть, сколько места доступно на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="ace0b-189">For example, a client may have the authority to view a hard disk drive object, but may not have authority to see how much space is available on the hard disk drive itself.</span></span> <span data-ttu-id="ace0b-190">Поставщик должен определить способ решения любой ситуации, когда поставщик не может полностью заполнить экземпляр свойствами из-за нарушения прав доступа.</span><span class="sxs-lookup"><span data-stu-id="ace0b-190">Your provider must determine how to handle any situation when the provider cannot completely fill an instance with properties due to an access violation.</span></span>

<span data-ttu-id="ace0b-191">Инструментарию WMI не требуется одиночный ответ клиентам с частичным доступом к экземпляру.</span><span class="sxs-lookup"><span data-stu-id="ace0b-191">WMI does not require a single response to clients that have partial access to an instance.</span></span> <span data-ttu-id="ace0b-192">Вместо этого WMI версии 1. x разрешает поставщику один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="ace0b-192">Instead, WMI version 1.x allows the provider one of the following options:</span></span>

-   <span data-ttu-id="ace0b-193">Завершить всю операцию с **\_ \_ \_ отказом в доступе к WBEM E** и не возвращать экземпляры.</span><span class="sxs-lookup"><span data-stu-id="ace0b-193">Fail the entire operation with **WBEM\_E\_ACCESS\_DENIED** and return no instances.</span></span>

    <span data-ttu-id="ace0b-194">Чтобы описать причину отказа, возвратите объект ошибки вместе с **\_ \_ \_ отказом в доступе к WBEM E**.</span><span class="sxs-lookup"><span data-stu-id="ace0b-194">Return an error object along with **WBEM\_E\_ACCESS\_DENIED**, to describe the reason for the denial.</span></span>

-   <span data-ttu-id="ace0b-195">Возвращают все доступные свойства и заполняют недоступные свойства **значением NULL**.</span><span class="sxs-lookup"><span data-stu-id="ace0b-195">Return all available properties, and fill unavailable properties with **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="ace0b-196">Убедитесь, что при возврате **\_ \_ доступа \_ WBEM E** не создается брешь в системе безопасности предприятия.</span><span class="sxs-lookup"><span data-stu-id="ace0b-196">Make sure that returning **WBEM\_E\_ACCESS\_DENIED** does not create a security hole in your enterprise.</span></span>

 

## <a name="reporting-partial-enumerations"></a><span data-ttu-id="ace0b-197">Создание отчетов о частичном перечислении</span><span class="sxs-lookup"><span data-stu-id="ace0b-197">Reporting Partial Enumerations</span></span>

<span data-ttu-id="ace0b-198">Другое распространенное возникновение нарушения прав доступа заключается в том, что WMI не может вернуть все перечисление.</span><span class="sxs-lookup"><span data-stu-id="ace0b-198">Another common occurrence of an access violation is when WMI cannot return all of an enumeration.</span></span> <span data-ttu-id="ace0b-199">Например, клиент может иметь доступ для просмотра всех объектов локального сетевого компьютера, но может не иметь доступа для просмотра объектов компьютера за пределами своего домена.</span><span class="sxs-lookup"><span data-stu-id="ace0b-199">For example, a client may have access to view all of the local network computer objects, but may not have access to view computer objects outside of his domain.</span></span> <span data-ttu-id="ace0b-200">Поставщик должен определить, как обрабатывать ситуацию, когда перечисление не может быть завершено из-за нарушения прав доступа.</span><span class="sxs-lookup"><span data-stu-id="ace0b-200">Your provider must determine how to handle any situation when an enumeration cannot be completed due to an access violation.</span></span>

<span data-ttu-id="ace0b-201">Как и у поставщика экземпляров, WMI не требует одного ответа на частичное перечисление.</span><span class="sxs-lookup"><span data-stu-id="ace0b-201">As with an instance provider, WMI does not require a single response to a partial enumeration.</span></span> <span data-ttu-id="ace0b-202">Вместо этого WMI версии 1. x предоставляет поставщику один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="ace0b-202">Instead, WMI version 1.x allows a provider one of the following options:</span></span>

-   <span data-ttu-id="ace0b-203">Возвратите **WBEM \_ \_ без \_ ошибок** для всех экземпляров, к которым поставщик может получить доступ.</span><span class="sxs-lookup"><span data-stu-id="ace0b-203">Return **WBEM\_S\_NO\_ERROR** for all instances that the provider can access.</span></span>

    <span data-ttu-id="ace0b-204">При использовании этого параметра пользователь не знает, что некоторые экземпляры были недоступны.</span><span class="sxs-lookup"><span data-stu-id="ace0b-204">If you use this option, the user is not aware that some instances were not available.</span></span> <span data-ttu-id="ace0b-205">Ряд поставщиков, например, с использованием язык SQL (SQL) с безопасностью на уровне строк, возвращают успешные частичные результаты, используя уровень безопасности вызывающего объекта для определения результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="ace0b-205">A number of providers, such as those using Structured Query Language (SQL) with row-level security, return successful partial results using the security level of the caller to define the result set.</span></span>

-   <span data-ttu-id="ace0b-206">Завершить всю операцию с **\_ \_ \_ отказом в доступе к WBEM E** и не возвращать экземпляры.</span><span class="sxs-lookup"><span data-stu-id="ace0b-206">Fail the entire operation with **WBEM\_E\_ACCESS\_DENIED** and return no instances.</span></span>

    <span data-ttu-id="ace0b-207">Поставщик может дополнительно включить объект Error, который описывает ситуацию для клиента.</span><span class="sxs-lookup"><span data-stu-id="ace0b-207">The provider may optionally include an error object that describes the situation to the client.</span></span> <span data-ttu-id="ace0b-208">Обратите внимание, что некоторые поставщики могут обращаться к источникам данных последовательно и могут не столкнуться с отказами, пока не попадете через перечисление.</span><span class="sxs-lookup"><span data-stu-id="ace0b-208">Note that some providers may access data sources serially and may not encounter denials until partway through the enumeration.</span></span>

-   <span data-ttu-id="ace0b-209">Возвращают все экземпляры, к которым возможен доступ, но также возвращают код состояния неошибки с кодом **WBEM \_ S \_ \_ отказано в доступе**.</span><span class="sxs-lookup"><span data-stu-id="ace0b-209">Return all of the instances that can be accessed but also return the nonerror status code **WBEM\_S\_ACCESS\_DENIED**.</span></span>

    <span data-ttu-id="ace0b-210">Поставщик должен отметить нарушение во время перечисления и может продолжать предоставлять экземпляры, завершая код состояния неошибки.</span><span class="sxs-lookup"><span data-stu-id="ace0b-210">The provider should note the denial during enumeration and may continue providing instances, finishing up with the nonerror status code.</span></span> <span data-ttu-id="ace0b-211">Поставщик может также выбрать завершение перечисления при первом отказе.</span><span class="sxs-lookup"><span data-stu-id="ace0b-211">The provider may also elect to terminate the enumeration at the first denial.</span></span> <span data-ttu-id="ace0b-212">Обоснование этого параметра заключается в том, что разные поставщики имеют разные парадигмы извлечения.</span><span class="sxs-lookup"><span data-stu-id="ace0b-212">The justification for this option is that different providers have different retrieval paradigms.</span></span> <span data-ttu-id="ace0b-213">Поставщик может уже доставить экземпляры, прежде чем обнаруживать нарушение прав доступа.</span><span class="sxs-lookup"><span data-stu-id="ace0b-213">A provider may have already delivered instances before discovering an access violation.</span></span> <span data-ttu-id="ace0b-214">Некоторые поставщики могут продолжать предоставлять другие экземпляры, и другие могут быть готовы к завершению.</span><span class="sxs-lookup"><span data-stu-id="ace0b-214">Some providers may elect to continue providing other instances and others may wish to terminate.</span></span>

<span data-ttu-id="ace0b-215">Из-за структуры COM невозможно выполнить упаковку обратной передачи информации во время ошибки, за исключением объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="ace0b-215">Due to the structure of COM, you cannot marshal back any information during an error except for an error object.</span></span> <span data-ttu-id="ace0b-216">Поэтому нельзя вернуть обе сведения и код ошибки.</span><span class="sxs-lookup"><span data-stu-id="ace0b-216">Therefore, you cannot return both information and an error code.</span></span> <span data-ttu-id="ace0b-217">Если вы решили вернуть сведения, необходимо использовать код состояния без ошибок.</span><span class="sxs-lookup"><span data-stu-id="ace0b-217">If you choose to return information, you must use a nonerror status code instead.</span></span>

## <a name="debugging-your-access-denied-code"></a><span data-ttu-id="ace0b-218">Отладка кода, которым запрещен доступ</span><span class="sxs-lookup"><span data-stu-id="ace0b-218">Debugging Your Access Denied Code</span></span>

<span data-ttu-id="ace0b-219">Некоторые приложения могут использовать уровни олицетворения ниже, чем **RPC \_ C \_ на \_ уровне \_ Imp**.</span><span class="sxs-lookup"><span data-stu-id="ace0b-219">Some applications may use impersonation levels lower than **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span> <span data-ttu-id="ace0b-220">В этом случае большинство вызовов олицетворения, выполненных поставщиком для клиентского приложения, завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ace0b-220">In this case, most impersonation calls made by the provider for the client application will fail.</span></span> <span data-ttu-id="ace0b-221">Для успешного проектирования и реализации поставщика необходимо учитывать эту идею.</span><span class="sxs-lookup"><span data-stu-id="ace0b-221">To successfully design and implement a provider, you must keep this idea in mind.</span></span>

<span data-ttu-id="ace0b-222">По умолчанию единственным другим уровнем олицетворения, который может получить доступ к поставщику, **является \_ \_ Указание на \_ уровне \_ "RPC C**".</span><span class="sxs-lookup"><span data-stu-id="ace0b-222">By default, the only other level of impersonation that can access a provider is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**.</span></span> <span data-ttu-id="ace0b-223">В случаях, когда клиентское приложение использует **RPC \_ C на \_ \_ уровне Imp \_**, [**коимперсонатеклиент**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) не возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="ace0b-223">In cases where a client application uses **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) does not return an error code.</span></span> <span data-ttu-id="ace0b-224">Вместо этого поставщик олицетворяет клиента только в целях идентификации.</span><span class="sxs-lookup"><span data-stu-id="ace0b-224">Instead, the provider impersonates the client for identification purposes only.</span></span> <span data-ttu-id="ace0b-225">Поэтому большинство методов Windows, вызываемых поставщиком, будут возвращать сообщение об отказе в доступе.</span><span class="sxs-lookup"><span data-stu-id="ace0b-225">Therefore, most Windows methods called by the provider will return an access denied message.</span></span> <span data-ttu-id="ace0b-226">Это не является безопасным на практике, поскольку пользователям не будет разрешено делать что-либо неприемлемое.</span><span class="sxs-lookup"><span data-stu-id="ace0b-226">This is harmless in practice, as users will not be permitted to do anything inappropriate.</span></span> <span data-ttu-id="ace0b-227">Однако это может быть полезно при разработке поставщика, чтобы определить, является ли клиент действительно олицетворенным.</span><span class="sxs-lookup"><span data-stu-id="ace0b-227">However, it may be useful during provider development to know whether the client was truly impersonated or not.</span></span>

<span data-ttu-id="ace0b-228">Для правильной компиляции кода требуются следующие ссылки и \# операторы include.</span><span class="sxs-lookup"><span data-stu-id="ace0b-228">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="ace0b-229">В следующем примере кода показано, как определить, был ли поставщик успешно олицетворять клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="ace0b-229">The following code example shows how to determine whether a provider has successfully impersonated a client application.</span></span>


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a><span data-ttu-id="ace0b-230">См. также</span><span class="sxs-lookup"><span data-stu-id="ace0b-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ace0b-231">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="ace0b-231">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="ace0b-232">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="ace0b-232">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="ace0b-233">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="ace0b-233">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
