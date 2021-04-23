---
description: Временные и постоянные потребители имеют разные методы защиты доставки событий.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Безопасное получение событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663773"
---
# <a name="receiving-events-securely"></a><span data-ttu-id="3d9ac-103">Безопасное получение событий</span><span class="sxs-lookup"><span data-stu-id="3d9ac-103">Receiving Events Securely</span></span>

<span data-ttu-id="3d9ac-104">Временные и постоянные потребители имеют разные методы защиты доставки событий.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-104">Temporary and permanent consumers have different methods of securing event delivery.</span></span>

<span data-ttu-id="3d9ac-105">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="3d9ac-105">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="3d9ac-106">Защита временных потребителей</span><span class="sxs-lookup"><span data-stu-id="3d9ac-106">Securing Temporary Consumers</span></span>](#securing-temporary-consumers)
-   [<span data-ttu-id="3d9ac-107">Защита постоянных потребителей</span><span class="sxs-lookup"><span data-stu-id="3d9ac-107">Securing Permanent Consumers</span></span>](#securing-permanent-consumers)
-   [<span data-ttu-id="3d9ac-108">Защита постоянной подписки</span><span class="sxs-lookup"><span data-stu-id="3d9ac-108">Securing the Permanent Subscription</span></span>](#securing-the-permanent-subscription)
-   [<span data-ttu-id="3d9ac-109">Установка Administrator-Only SD</span><span class="sxs-lookup"><span data-stu-id="3d9ac-109">Setting an Administrator-Only SD</span></span>](#setting-an-administrator-only-sd)
-   [<span data-ttu-id="3d9ac-110">Олицетворение удостоверения поставщика событий</span><span class="sxs-lookup"><span data-stu-id="3d9ac-110">Impersonating the Event Provider Identity</span></span>](#impersonating-the-event-provider-identity)
-   [<span data-ttu-id="3d9ac-111">Идентификаторы безопасности и постоянные подписки</span><span class="sxs-lookup"><span data-stu-id="3d9ac-111">SIDs and Permanent Subscriptions</span></span>](#sids-and-permanent-subscriptions)
-   [<span data-ttu-id="3d9ac-112">Создание постоянных подписок с использованием учетных записей домена</span><span class="sxs-lookup"><span data-stu-id="3d9ac-112">Creating Permanent Subscriptions Using Domain Accounts</span></span>](#creating-permanent-subscriptions-using-domain-accounts)
-   [<span data-ttu-id="3d9ac-113">См. также</span><span class="sxs-lookup"><span data-stu-id="3d9ac-113">Related topics</span></span>](#related-topics)

## <a name="securing-temporary-consumers"></a><span data-ttu-id="3d9ac-114">Защита временных потребителей</span><span class="sxs-lookup"><span data-stu-id="3d9ac-114">Securing Temporary Consumers</span></span>

<span data-ttu-id="3d9ac-115">[*Временные потребители*](gloss-t.md) выполняются до перезагрузки системы или остановки инструментария WMI, но не могут быть запущены при возникновении определенного события.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-115">A [*temporary consumers*](gloss-t.md) runs until the system is rebooted or WMI is stopped but cannot be started if a specific event is raised.</span></span> <span data-ttu-id="3d9ac-116">Например, вызов [**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md) создает временный потребитель.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-116">For example, a call to [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) creates a temporary consumer.</span></span>

<span data-ttu-id="3d9ac-117">Вызовы [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) или [**IWbemServices:: ексекнотификатионкуери**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) создают временные потребители событий.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-117">The calls [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) or [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) create temporary event consumers.</span></span> <span data-ttu-id="3d9ac-118">Временные потребители не могут контролировать, кто предоставляет события создаваемому [*приемнику*](gloss-s.md) событий.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-118">Temporary consumers cannot control who provides events to the event [*sink*](gloss-s.md) they create.</span></span>

<span data-ttu-id="3d9ac-119">Вызовы методов [**ексекнотификатионкуери**](swbemservices-execnotificationquery.md) могут выполняться синхронно, [*полусинхронном*](gloss-s.md)или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-119">Calls to [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) methods can be made synchronously, [*semisynchronously*](gloss-s.md), or asynchronously.</span></span> <span data-ttu-id="3d9ac-120">Например, [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) является синхронным методом, который может вызываться полусинхронном в зависимости от того, как задан параметр *ифлагс* .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-120">For example, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) is a synchronous method that can be called semisynchronously, depending on how the *iflags* parameter is set.</span></span> <span data-ttu-id="3d9ac-121">[**SWbemServices.Exeкнотификатионкуерясинк**](swbemservices-execnotificationqueryasync.md) является асинхронным вызовом.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-121">[**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) is an asynchronous call.</span></span>

<span data-ttu-id="3d9ac-122">Имейте в виду, что обратный вызов приемника для асинхронных версий этих вызовов может быть не возвращен на том же уровне проверки подлинности, что и вызов созданного скрипта.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-122">Be aware that the callback to the sink for the asynchronous versions of these calls might not be returned at the same authentication level as the call the script made.</span></span> <span data-ttu-id="3d9ac-123">Поэтому рекомендуется использовать семисинчронаус вместо асинхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-123">Therefore, it is recommended that you use semisynchronous instead of asynchronous calls.</span></span> <span data-ttu-id="3d9ac-124">Если требуется асинхронное взаимодействие, см. статью [вызов метода](calling-a-method.md) и [Настройка безопасности при асинхронном вызове](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-124">If you require asynchronous communication, see [Calling a Method](calling-a-method.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="3d9ac-125">Подписчики скриптов не могут проверить права доступа поставщика событий, чтобы предоставить события приемнику, созданному сценарием.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-125">Scripting subscribers cannot check the access rights of an event provider to provide events to the sink created by the script.</span></span> <span data-ttu-id="3d9ac-126">Поэтому рекомендуется, чтобы вызовы [**SWbemServices.Exeкнотификатионкуери**](swbemservices-execnotificationquery.md) использовали семисинчронаус форму вызова и использовали определенные параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-126">Therefore, it is recommended that calls to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) use the semisynchronous form of the call and use specific security settings.</span></span> <span data-ttu-id="3d9ac-127">Дополнительные сведения см. в разделе [осуществление вызова семисинчронаус с помощью VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-127">For more information, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="securing-permanent-consumers"></a><span data-ttu-id="3d9ac-128">Защита постоянных потребителей</span><span class="sxs-lookup"><span data-stu-id="3d9ac-128">Securing Permanent Consumers</span></span>

<span data-ttu-id="3d9ac-129">[*Постоянные потребители*](gloss-p.md) имеют постоянную подписку на события от поставщика событий, который будет сохранен после перезапуска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-129">A [*permanent consumers*](gloss-p.md) has a permanent subscription to events from an event provider that will persist after the operating system is restarted.</span></span> <span data-ttu-id="3d9ac-130">Поставщик событий, поддерживающий постоянные потребители, является [*поставщиком потребителей событий*](gloss-e.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-130">An event provider that supports permanent consumers is a [*event consumer provider*](gloss-e.md).</span></span> <span data-ttu-id="3d9ac-131">Если поставщик событий не выполняется при возникновении события, Инструментарий WMI запускает поставщик, когда ему требуется доставка событий.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-131">If the event provider is not running when an event occurs, then WMI starts the provider when it needs to deliver events.</span></span> <span data-ttu-id="3d9ac-132">WMI определяет, в какой поставщик потребителей должны доставляться события, на основе экземпляра [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md) , который связывает экземпляр [**\_ \_ Win32Provider**](--win32provider.md) поставщика с [*логическим классом-получателем*](gloss-l.md) , определенным поставщиком потребителя.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-132">WMI identifies which consumer provider the events should be delivered to, based on the [**\_\_EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) instance, which associates the consumer provider [**\_\_Win32Provider**](--win32provider.md) instance with a [*logical consumer class*](gloss-l.md) defined by the consumer provider.</span></span> <span data-ttu-id="3d9ac-133">Дополнительные сведения о роли поставщиков потребителей см. в разделе [написание поставщика событий](writing-an-event-consumer-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-133">For more information about the role of consumer providers, see [Writing an Event Consumer Provider](writing-an-event-consumer-provider.md).</span></span>

<span data-ttu-id="3d9ac-134">Постоянные потребители могут управлять отправкой событий и поставщиков событий для управления доступом к своим событиям.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-134">Permanent consumers can control who sends them events and event providers can control who accesses their events.</span></span>

<span data-ttu-id="3d9ac-135">Клиентские скрипты и приложения создают экземпляры класса логического потребителя в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-135">Client scripts and applications create instances of the logical consumer class as part of a subscription.</span></span> <span data-ttu-id="3d9ac-136">Класс логического потребителя определяет, какие сведения содержит событие, что может делать клиент с событием и как доставляется событие.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-136">The logical consumer class defines what information the event contains, what the client can do with the event, and how the event is delivered.</span></span>

<span data-ttu-id="3d9ac-137">[Классы стандартных потребителей](standard-consumer-classes.md) WMI предоставляют примеры роли для классов логических потребителей.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-137">The WMI [Standard Consumer Classes](standard-consumer-classes.md) provide examples of the role of logical consumer classes.</span></span> <span data-ttu-id="3d9ac-138">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-138">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

## <a name="securing-the-permanent-subscription"></a><span data-ttu-id="3d9ac-139">Защита постоянной подписки</span><span class="sxs-lookup"><span data-stu-id="3d9ac-139">Securing the Permanent Subscription</span></span>

<span data-ttu-id="3d9ac-140">Постоянные подписки имеют большую вероятность вызвать проблемы безопасности в WMI и, следовательно, предъявляют следующие требования к безопасности.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-140">Permanent subscriptions have greater potential to cause security problems in WMI and therefore have the following security requirements:</span></span>

-   <span data-ttu-id="3d9ac-141">Логический экземпляр потребителя, [**\_ \_ EventFilter**](--eventfilter.md)и экземпляры [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) должны иметь один и тот же идентификатор безопасности (SID) в свойстве **креаторсид** .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-141">The logical consumer instance, the [**\_\_EventFilter**](--eventfilter.md), and the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) instances must have the same individual security identifier (SID) in the **CreatorSID** property.</span></span> <span data-ttu-id="3d9ac-142">Дополнительные сведения см. [в разделе поддержание одного и того же идентификатора безопасности во всех экземплярах постоянной подписки](#sids-and-permanent-subscriptions).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-142">For more information, see [Keeping the same SID in all instances of a permanent subscription](#sids-and-permanent-subscriptions).</span></span>
-   <span data-ttu-id="3d9ac-143">Учетная запись, создающая подписку, должна быть либо учетной записью домена с правами локального администратора, либо локальной учетной записью группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-143">The account that creates the subscription must be either a domain account with local administrator privileges or the local Administrators group account.</span></span> <span data-ttu-id="3d9ac-144">Использование идентификатора безопасности группы администраторов позволяет подписке продолжать работу на локальном компьютере, даже если она отключена от сети.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-144">Using the Administrators group SID allows the subscription to continue to work on the local computer, even if it is disconnected from the network.</span></span> <span data-ttu-id="3d9ac-145">Использование учетной записи домена позволяет точно идентифицировать пользователя.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-145">Using a domain account allows exact identification of the user.</span></span>

    <span data-ttu-id="3d9ac-146">Однако если компьютер не подключен, а создание учетной записи является учетной записью домена, происходит сбой потребителя, так как WMI не может проверить удостоверение учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-146">However, if the computer is not connected and the creating account is a domain account, the consumer fails because WMI cannot verify the identity of the account.</span></span> <span data-ttu-id="3d9ac-147">Чтобы избежать сбоя подписки, если компьютер отключен от сети, используйте идентификатор безопасности группы администраторов для подписки.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-147">To avoid subscription failure if the computer is disconnected from the network, use the Administrators group SID for a subscription.</span></span> <span data-ttu-id="3d9ac-148">В этом случае следует убедиться, что учетная запись LocalSystem может получать доступ к данным членства в домене.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-148">In this case, you should ensure that the LocalSystem account can access group membership data on the domain.</span></span> <span data-ttu-id="3d9ac-149">Некоторые поставщики потребителей событий имеют особенно высокий уровень безопасности, так как незаконная подписка может привести к существенному повреждению.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-149">Some event consumer providers have particularly high security requirements, since a rogue subscription can cause great damage.</span></span> <span data-ttu-id="3d9ac-150">Примерами являются стандартные потребители, [**активескриптевентконсумер**](activescripteventconsumer.md) и [**коммандлинивентконсумер**](commandlineeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-150">Examples are the standard consumers, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) and [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>

-   <span data-ttu-id="3d9ac-151">Постоянную подписку можно настроить на прием событий только от конкретных удостоверений поставщиков событий.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-151">You can configure the permanent subscription to only accept events from specific event provider identities.</span></span> <span data-ttu-id="3d9ac-152">Установите дескриптор безопасности в свойстве **евентакцесс** экземпляра [**\_ \_ EventFilter**](--eventfilter.md) на удостоверения поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-152">Set the security descriptor in the **EventAccess** property of the [**\_\_EventFilter**](--eventfilter.md) instance to the event provider identities.</span></span> <span data-ttu-id="3d9ac-153">Инструментарий WMI сравнивает удостоверение поставщика событий с дескриптором безопасности, чтобы определить, имеет ли поставщик **WBEM доступ к \_ \_ публикации** .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-153">WMI compares the identity of the event provider to the security descriptor to determine if the provider has **WBEM\_RIGHT\_PUBLISH** access.</span></span> <span data-ttu-id="3d9ac-154">Дополнительные сведения см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-154">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

    <span data-ttu-id="3d9ac-155">Если фильтр разрешает доступ к удостоверению поставщика событий, он также доверяет этому событию.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-155">If the filter allows access to the event provider identity, then it also trusts the event.</span></span> <span data-ttu-id="3d9ac-156">Это позволяет потребителю, получившим событие, вызывать делегированное событие.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-156">This allows the consumer that received the event to raise a delegated event.</span></span>

    <span data-ttu-id="3d9ac-157">**Примечание**  .  Значение по умолчанию для дескриптора безопасности в **евентакцесс** — **null**, что позволяет получить доступ ко всем.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-157">**Note**  The default for the security descriptor in **EventAccess** is **NULL**, which allows access to everyone.</span></span> <span data-ttu-id="3d9ac-158">Для повышения безопасности событий рекомендуется ограничить доступ в экземпляре подписки [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-158">Limiting access in the subscription instance of [**\_\_EventFilter**](--eventfilter.md) is recommended for better event security.</span></span>

## <a name="setting-an-administrator-only-sd"></a><span data-ttu-id="3d9ac-159">Установка Administrator-Only SD</span><span class="sxs-lookup"><span data-stu-id="3d9ac-159">Setting an Administrator-Only SD</span></span>

<span data-ttu-id="3d9ac-160">В следующем примере кода C++ создается дескриптор безопасности только для администраторов на экземпляре [**\_ \_ EventFilter**](--eventfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-160">The following C++ code example creates an administrator-only security descriptor on the [**\_\_EventFilter**](--eventfilter.md) instance.</span></span> <span data-ttu-id="3d9ac-161">В этом примере создается дескриптор безопасности с использованием [языка определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-161">This example creates the security descriptor using [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL).</span></span> <span data-ttu-id="3d9ac-162">Дополнительные сведения о подсистеме **WBEM \_ right \_** см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-162">For more information about **WBEM\_RIGHT\_SUBSCRIBE**, see [WMI Security Constants](wmi-security-constants.md).</span></span>


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



<span data-ttu-id="3d9ac-163">Для предыдущего примера кода требуются следующие инструкции Reference и \# include.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-163">The previous code example requires the following reference and \#include statements.</span></span>


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a><span data-ttu-id="3d9ac-164">Олицетворение удостоверения поставщика событий</span><span class="sxs-lookup"><span data-stu-id="3d9ac-164">Impersonating the Event Provider Identity</span></span>

<span data-ttu-id="3d9ac-165">Постоянному потребителю может потребоваться олицетворение поставщика событий для обработки события.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-165">A permanent consumer may need to impersonate the event provider to process the event.</span></span> <span data-ttu-id="3d9ac-166">Постоянные потребители могут олицетворять только поставщика событий, только если выполняются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-166">Permanent consumers can only impersonate the event provider when the following conditions exist:</span></span>

-   <span data-ttu-id="3d9ac-167">Экземпляр [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) имеет свойство **маинтаинсекуритиконтекст** со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-167">The instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) has the **MaintainSecurityContext** property set to **True**.</span></span>
-   <span data-ttu-id="3d9ac-168">Событие доставляется в том же контексте безопасности, в котором находился поставщик при создании события.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-168">An event is delivered in the same security context that the provider was in when it generated the event.</span></span> <span data-ttu-id="3d9ac-169">Только потребитель, реализованный как библиотека DLL, внутрипроцессный потребитель, может принимать события в контексте безопасности поставщика.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-169">Only a consumer implemented as a DLL, an in-process consumer, can receive events in the security context of the provider.</span></span> <span data-ttu-id="3d9ac-170">Дополнительные сведения о безопасности внутрипроцессного поставщика и потребителей см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-170">For more information about security of in-process providers and consumers, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="3d9ac-171">Поставщик событий выполняется в процессе, допускающем олицетворение.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-171">The event provider is running in a process that allows impersonation.</span></span>

<span data-ttu-id="3d9ac-172">Учетная запись, выполняющая процесс потребителя, должна иметь полный доступ на **\_ запись** к репозиторию WMI (также известному как репозиторий CIM).</span><span class="sxs-lookup"><span data-stu-id="3d9ac-172">The account running the consumer process must have **FULL\_WRITE** access to the WMI repository (also known as the CIM repository).</span></span> <span data-ttu-id="3d9ac-173">В подписке экземпляры [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md), [**\_ \_ евентконсумер**](--eventconsumer.md)и [**\_ \_ EventFilter**](--eventfilter.md) должны иметь одинаковое значение индивидуального идентификатора безопасности (SID) в свойстве **креаторсид** .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-173">In the subscription, the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_\_EventConsumer**](--eventconsumer.md), and [**\_\_EventFilter**](--eventfilter.md) instances must have the same individual security identifier (SID) value in the **CreatorSID** property.</span></span> <span data-ttu-id="3d9ac-174">WMI сохраняет идентификатор безопасности в **креаторсид** для каждого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-174">WMI stores the SID in the **CreatorSID** for each instance.</span></span>

## <a name="sids-and-permanent-subscriptions"></a><span data-ttu-id="3d9ac-175">Идентификаторы безопасности и постоянные подписки</span><span class="sxs-lookup"><span data-stu-id="3d9ac-175">SIDs and Permanent Subscriptions</span></span>

<span data-ttu-id="3d9ac-176">Постоянная подписка не работает, если привязка, потребитель и фильтр созданы не одним пользователем. Это означает, что [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md), [**\_ \_ евентконсумер**](--eventconsumer.md)и [**\_ \_ EventFilter**](--eventfilter.md) должны иметь одинаковое значение индивидуального идентификатора безопасности (SID) в свойстве **креаторсид** .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-176">A permanent subscription does not work when the binding, the consumer, and the filter are not created by the same user, which means that the [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_\_EventConsumer**](--eventconsumer.md), and [**\_\_EventFilter**](--eventfilter.md) must have the same individual security identifier (SID) value in the **CreatorSID** property.</span></span> <span data-ttu-id="3d9ac-177">Инструментарий управления Windows (WMI) (WMI) сохраняет это значение.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-177">Windows Management Instrumentation (WMI) stores this value.</span></span>

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a><span data-ttu-id="3d9ac-178">Создание постоянных подписок с использованием учетных записей домена</span><span class="sxs-lookup"><span data-stu-id="3d9ac-178">Creating Permanent Subscriptions Using Domain Accounts</span></span>

<span data-ttu-id="3d9ac-179">При использовании учетных записей домена для создания постоянных подписок следует учитывать несколько проблем.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-179">Several issues must be considered when using domain accounts to create permanent subscriptions.</span></span> <span data-ttu-id="3d9ac-180">Каждая постоянная подписка по-прежнему будет работать, когда никто из пользователей не вошел в систему. Это означает, что они работают под встроенной учетной записью LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-180">Every permanent subscription should still work when no user is logged on, which means they function under the built-in LocalSystem account.</span></span>

<span data-ttu-id="3d9ac-181">Если пользователь домена является создателем постоянной подписки для потребителей с защитой безопасности ([**активескриптевентконсумер**](activescripteventconsumer.md), [**коммандлинивентконсумер**](commandlineeventconsumer.md)), Инструментарий WMI проверяет, принадлежат ли свойства **креаторсид** класса [**\_ \_ EventFilter**](--eventfilter.md) , класса [**\_ \_ филтертоконсумербиндинг**](--filtertoconsumerbinding.md) и экземпляров потребителей пользователю, который является членом локальной группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-181">If a domain user is the creator of a permanent subscription for security sensitive consumers ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), then WMI verifies whether the **CreatorSID** property of the [**\_\_EventFilter**](--eventfilter.md) class, [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) class, and the consumer instances belong to a user who is member of local Administrators group.</span></span>

<span data-ttu-id="3d9ac-182">В следующем примере кода показано, как можно указать свойство **креаторсид** .</span><span class="sxs-lookup"><span data-stu-id="3d9ac-182">The following code example shows how you can specify the **CreatorSID** property.</span></span>

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

<span data-ttu-id="3d9ac-183">В случае междоменных ситуаций добавьте пользователей, прошедших проверку подлинности, в группу доступа Windows Authorization.</span><span class="sxs-lookup"><span data-stu-id="3d9ac-183">For cross domain situations, add Authenticated Users to the "Windows Authorization Access Group".</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d9ac-184">См. также</span><span class="sxs-lookup"><span data-stu-id="3d9ac-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d9ac-185">Защита событий WMI</span><span class="sxs-lookup"><span data-stu-id="3d9ac-185">Securing WMI Events</span></span>](securing-wmi-events.md)
</dt> <dt>

[<span data-ttu-id="3d9ac-186">Получение события WMI</span><span class="sxs-lookup"><span data-stu-id="3d9ac-186">Receiving a WMI Event</span></span>](receiving-a-wmi-event.md)
</dt> </dl>

 

 
