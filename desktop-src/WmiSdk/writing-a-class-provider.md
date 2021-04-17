---
description: Поставщик класса управляет классом или набором классов для WMI.
ms.assetid: 755f1fde-a0bf-43f6-a01d-2da7d4e6c10d
ms.tgt_platform: multiple
title: Написание поставщика класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1e20115c4f833ad828e8d181ca97782d233130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712094"
---
# <a name="writing-a-class-provider"></a><span data-ttu-id="9248c-103">Написание поставщика класса</span><span class="sxs-lookup"><span data-stu-id="9248c-103">Writing a Class Provider</span></span>

<span data-ttu-id="9248c-104">Поставщик класса управляет классом или набором классов для WMI.</span><span class="sxs-lookup"><span data-stu-id="9248c-104">A class provider manages a class or series of classes for WMI.</span></span> <span data-ttu-id="9248c-105">Поставщик класса может быть либо принудительным, либо опрашивающим; то есть он может хранить собственные данные или разрешать инструментарию WMI хранить данные для них в службе управления Windows.</span><span class="sxs-lookup"><span data-stu-id="9248c-105">A class provider can either be push or pull; that is, it can either store its own data or allow WMI to store data for it in the Windows Management Service.</span></span> <span data-ttu-id="9248c-106">Хотя поставщик класса установлен на определенном компьютере, он может изменять определения классов во всей Организации.</span><span class="sxs-lookup"><span data-stu-id="9248c-106">Although a class provider is installed on a specific machine, it can change the class definitions across an entire enterprise.</span></span> <span data-ttu-id="9248c-107">Поэтому большинство разработчиков часто не создают поставщики классов.</span><span class="sxs-lookup"><span data-stu-id="9248c-107">Therefore, most developers do not often create class providers.</span></span>

<span data-ttu-id="9248c-108">Перед созданием поставщика класса убедитесь, что поддерживаемые классы действительно должны создаваться динамически.</span><span class="sxs-lookup"><span data-stu-id="9248c-108">Before constructing a class provider, verify that the supported classes truly must be generated dynamically.</span></span> <span data-ttu-id="9248c-109">В большинстве случаев список классов является неизменным и конечным.</span><span class="sxs-lookup"><span data-stu-id="9248c-109">In most cases, the list of classes is slow-changing and finite.</span></span> <span data-ttu-id="9248c-110">В этом случае не нужно создавать поставщик класса.</span><span class="sxs-lookup"><span data-stu-id="9248c-110">If this is the case, you should not have to create a class provider.</span></span> <span data-ttu-id="9248c-111">Вместо этого можно разместить определения классов в репозитории WMI с помощью API инструментария WMI или MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="9248c-111">Instead, you can place your class definitions in the WMI repository using the WMI API or a MOF file.</span></span>

<span data-ttu-id="9248c-112">В следующей процедуре описывается реализация поставщика класса.</span><span class="sxs-lookup"><span data-stu-id="9248c-112">The following procedure describes how to implement a class provider.</span></span>

<span data-ttu-id="9248c-113">**Реализация поставщика класса**</span><span class="sxs-lookup"><span data-stu-id="9248c-113">**To implement a class provider**</span></span>

1.  <span data-ttu-id="9248c-114">Определите, является ли поставщик принудительным или поставщиком опрашивающей репликации.</span><span class="sxs-lookup"><span data-stu-id="9248c-114">Determine if your provider is a push or pull provider.</span></span>

    <span data-ttu-id="9248c-115">Поставщик опроса предоставляет данные динамически в ответ на запрос приложения, тогда как поставщики push-уведомлений хранят свои данные один раз в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="9248c-115">A pull provider supplies data dynamically in response to an application request, whereas push providers store their data once in the WMI repository.</span></span> <span data-ttu-id="9248c-116">Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="9248c-116">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

2.  <span data-ttu-id="9248c-117">Разработка и регистрация поставщика классов с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="9248c-117">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="9248c-118">Поставщики классов регистрируются в WMI путем создания экземпляра [**\_ \_ Win32Provider**](--win32provider.md) и экземпляра [**\_ \_ класспровидеррегистратион**](--classproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="9248c-118">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_ClassProviderRegistration**](--classproviderregistration.md) instance.</span></span> <span data-ttu-id="9248c-119">Дополнительные сведения см. [в разделе Регистрация поставщика класса](registering-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9248c-119">For more information, see [Registering a Class Provider](registering-a-class-provider.md).</span></span>

3.  <span data-ttu-id="9248c-120">Реализуйте интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="9248c-120">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="9248c-121">Инструментарий WMI использует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для загрузки и инициализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="9248c-121">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="9248c-122">При проектировании поставщика push-уведомлений **ивбемпровидеринит** является единственным интерфейсом, который вы будете реализовывать.</span><span class="sxs-lookup"><span data-stu-id="9248c-122">If you are designing a push provider, **IWbemProviderInit** is the only interface you will implement.</span></span> <span data-ttu-id="9248c-123">Дополнительные сведения см. [в разделе Инициализация поставщика](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9248c-123">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="9248c-124">Поставщики классов настоятельно рекомендуется использовать модель многопоточности "both".</span><span class="sxs-lookup"><span data-stu-id="9248c-124">Class providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

4.  <span data-ttu-id="9248c-125">Добавьте дополнительный код, необходимый для поставщика.</span><span class="sxs-lookup"><span data-stu-id="9248c-125">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="9248c-126">При проектировании поставщика вам, скорее всего, придется вызывать интерфейсы WMI.</span><span class="sxs-lookup"><span data-stu-id="9248c-126">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="9248c-127">Дополнительные сведения см. в разделе [вызов метода](calling-a-method.md) и [обслуживание уровней безопасности в поставщике](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="9248c-127">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="9248c-128">При получении сведений для клиента может потребоваться доступ к уровням безопасности для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="9248c-128">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="9248c-129">Дополнительные сведения см. в разделе [олицетворение клиента](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="9248c-129">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="9248c-130">Реализуйте интерфейс [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) для вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="9248c-130">Implement the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface for your provider.</span></span>

    <span data-ttu-id="9248c-131">Интерфейс [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) является основным интерфейсом для поставщика опрашивающего класса.</span><span class="sxs-lookup"><span data-stu-id="9248c-131">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a pull class provider.</span></span> <span data-ttu-id="9248c-132">Дополнительные сведения см. [в разделе Реализация основного интерфейса для поставщика класса](implementing-the-primary-interface-for-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9248c-132">For more information, see [Implementing the Primary Interface for a Class Provider](implementing-the-primary-interface-for-a-class-provider.md).</span></span>

6.  <span data-ttu-id="9248c-133">Замените имеющийся поставщик новым кодом.</span><span class="sxs-lookup"><span data-stu-id="9248c-133">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="9248c-134">Вам не нужно выполнять этот шаг, если у вас нет уже существующего поставщика для копирования.</span><span class="sxs-lookup"><span data-stu-id="9248c-134">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="9248c-135">Дополнительные сведения см. [в разделе Обновление поставщика](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9248c-135">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



