---
description: Одна из первых задач, которую необходимо запрограммировать для поставщика, — это процесс инициализации, который охватывает все задачи, которые должен выполнить поставщик, что позволяет ему отправлять и получать данные из WMI, управлять управляемым объектом и выполнять другие задачи.
ms.assetid: 3dc145b8-1ce4-4caa-b2ac-31a3681e76f1
ms.tgt_platform: multiple
title: Инициализация поставщика
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14a724d72d5e5c58eff30f2fa61da64d77a493f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913368"
---
# <a name="initializing-a-provider"></a><span data-ttu-id="965c1-103">Инициализация поставщика</span><span class="sxs-lookup"><span data-stu-id="965c1-103">Initializing a Provider</span></span>

<span data-ttu-id="965c1-104">Одна из первых задач, которую необходимо запрограммировать для поставщика, — это процесс инициализации, который охватывает все задачи, которые должен выполнить поставщик, что позволяет ему отправлять и получать данные из WMI, управлять управляемым объектом и выполнять другие задачи.</span><span class="sxs-lookup"><span data-stu-id="965c1-104">One of the first tasks you must code for a provider is the initialization process, which covers any tasks your provider must perform that allows it to send and receive information from WMI, control a managed object, and perform other tasks.</span></span> <span data-ttu-id="965c1-105">Каждый тип поставщика имеет свой набор задач, который должен выполняться и имеет сопутствующий набор уникальных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="965c1-105">Each type of provider has a different set of tasks that it must perform and has an accompanying set of unique interfaces.</span></span>

<span data-ttu-id="965c1-106">Однако все поставщики инициализируются через интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и СООБЩАют инструментарию WMI о своем состоянии инициализации через интерфейс [**ивбемпровидеринитсинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .</span><span class="sxs-lookup"><span data-stu-id="965c1-106">However, all providers initialize through the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface, and inform WMI of their initialization status through the [**IWbemProviderInitSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) interface.</span></span>

<span data-ttu-id="965c1-107">В следующей процедуре описывается инициализация поставщика.</span><span class="sxs-lookup"><span data-stu-id="965c1-107">The following procedure describes how to initialize a provider.</span></span>

<span data-ttu-id="965c1-108">**Инициализация поставщика**</span><span class="sxs-lookup"><span data-stu-id="965c1-108">**To initialize a provider**</span></span>

1.  <span data-ttu-id="965c1-109">Реализуйте [**ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="965c1-109">Implement [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) for your provider.</span></span>

    <span data-ttu-id="965c1-110">Когда WMI определяет, что клиенту требуются службы поставщика, WMI загружает поставщик, вызывая метод [**ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="965c1-110">When WMI determines that a client requires the services of a provider, WMI loads the provider by calling the [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) method.</span></span>

2.  <span data-ttu-id="965c1-111">Реализуйте любые интерфейсы, уникальные для вашего типа поставщика.</span><span class="sxs-lookup"><span data-stu-id="965c1-111">Implement any interfaces unique to your type of provider.</span></span>
3.  <span data-ttu-id="965c1-112">Сообщите инструментарию WMI о том, что поставщик завершен с инициализацией, вызвав [**ивбемпровидеринитсинк:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="965c1-112">Inform WMI that your provider is finished with initialization by calling [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus).</span></span>

    <span data-ttu-id="965c1-113">Все реализации [**ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) должны вызывать [**Ивбемпровидеринитсинк:: SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) для передачи состояния инициализации в WMI.</span><span class="sxs-lookup"><span data-stu-id="965c1-113">All implementations of [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) must call [**IWbemProviderInitSink::SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to report initialization status to WMI.</span></span> <span data-ttu-id="965c1-114">Метод **SetStatus** позволяет инструментарию WMI определить, готов ли поставщик к получению запросов, и тип запросов, которые поставщик готов к получению.</span><span class="sxs-lookup"><span data-stu-id="965c1-114">The **SetStatus** method allows WMI to determine if a provider is ready to receive requests and the type of requests that the provider is ready to receive.</span></span>

<span data-ttu-id="965c1-115">Следующая процедура описывает, как сообщить об успешной инициализации.</span><span class="sxs-lookup"><span data-stu-id="965c1-115">The following procedure describes how to report a successful initialization.</span></span>

<span data-ttu-id="965c1-116">**Чтобы сообщить об успешной инициализации**</span><span class="sxs-lookup"><span data-stu-id="965c1-116">**To report a successful initialization**</span></span>

-   <span data-ttu-id="965c1-117">Установите для параметра *Истатус* [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) значение **WBEM, \_ \_ инициализированное**.</span><span class="sxs-lookup"><span data-stu-id="965c1-117">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_S\_INITIALIZED**.</span></span>

    <span data-ttu-id="965c1-118">После того как вы вернете значение **WBEM \_ \_**, поставщик указывает на готовность к обработке запросов от приложений, WMI и других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="965c1-118">By returning **WBEM\_S\_INITIALIZED**, a provider indicates a readiness to handle requests from applications, WMI, and other providers.</span></span> <span data-ttu-id="965c1-119">После инициализации WBEM \_ \_ , Инструментарий WMI выполняет вызов метода [**Ивбемпровидеринит:: QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) поставщика.</span><span class="sxs-lookup"><span data-stu-id="965c1-119">After receiving WBEM\_S\_INITIALIZED, WMI makes a call to the [**IWbemProviderInit::QueryInterface**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) method on the provider.</span></span> <span data-ttu-id="965c1-120">Этот запрос получает указатель на основной интерфейс поставщика.</span><span class="sxs-lookup"><span data-stu-id="965c1-120">This query retrieves a pointer to the primary interface of the provider.</span></span>

<span data-ttu-id="965c1-121">Следующая процедура описывает, как сообщить об ошибке во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="965c1-121">The following procedure describes how to report an error during initialization.</span></span>

<span data-ttu-id="965c1-122">**Сообщение об ошибке во время инициализации**</span><span class="sxs-lookup"><span data-stu-id="965c1-122">**To report an error during initialization**</span></span>

-   <span data-ttu-id="965c1-123">Установите для параметра *Истатус* [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) значение **WBEM \_ E \_ не удалось**.</span><span class="sxs-lookup"><span data-stu-id="965c1-123">Set the *IStatus* parameter of [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) to **WBEM\_E\_FAILED**.</span></span> <span data-ttu-id="965c1-124">Поставщики представлений WMI, которые возвращают **WBEM \_ E \_** , не работают.</span><span class="sxs-lookup"><span data-stu-id="965c1-124">WMI views providers that return **WBEM\_E\_FAILED** as not functional.</span></span>

    <span data-ttu-id="965c1-125">Инструментарий WMI освобождает указатель [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) либо после того, как WMI получил указатель на основной интерфейс поставщика или после сбоя инициализации.</span><span class="sxs-lookup"><span data-stu-id="965c1-125">WMI releases the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pointer either after WMI has obtained a pointer to the primary interface of the provider or after initialization has failed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="965c1-126">См. также</span><span class="sxs-lookup"><span data-stu-id="965c1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="965c1-127">Разработка поставщика WMI</span><span class="sxs-lookup"><span data-stu-id="965c1-127">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="965c1-128">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="965c1-128">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="965c1-129">Защита поставщика</span><span class="sxs-lookup"><span data-stu-id="965c1-129">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



