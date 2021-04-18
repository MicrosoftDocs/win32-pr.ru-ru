---
description: Поставщик метода позволяет инструментарию WMI обращаться к методам класса. Например, класс, представляющий приложение, может иметь метод, который прерывает работу приложения.
ms.assetid: bce87e65-5cba-4eef-91da-a3e13c80b8a6
ms.tgt_platform: multiple
title: Написание поставщика методов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8626e2e16fe5424a0b05df81e2444a72ecb8841f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711722"
---
# <a name="writing-a-method-provider"></a><span data-ttu-id="c5c4d-104">Написание поставщика методов</span><span class="sxs-lookup"><span data-stu-id="c5c4d-104">Writing a Method Provider</span></span>

<span data-ttu-id="c5c4d-105">Поставщик метода позволяет инструментарию WMI обращаться к методам класса.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-105">A method provider allows WMI access to the methods of a class.</span></span> <span data-ttu-id="c5c4d-106">Например, класс, представляющий приложение, может иметь метод, который прерывает работу приложения.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-106">For example, a class that represents an application may have a method that terminates the application.</span></span>

<span data-ttu-id="c5c4d-107">Изменение порядка входных и выходных параметров метода при обновлении существующего поставщика методов может привести к сбою в приложениях, которые вызывают метод.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-107">Changing the order of method input and output parameters when updating an existing method provider can cause failure for applications that call the method.</span></span> <span data-ttu-id="c5c4d-108">Порядок входных или выходных параметров устанавливается значением квалификатора [**ID**](standard-wmi-qualifiers.md) для каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-108">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="c5c4d-109">Первый параметр имеет нулевое значение **идентификатора** .</span><span class="sxs-lookup"><span data-stu-id="c5c4d-109">The first parameter has an **ID** value of zero.</span></span> <span data-ttu-id="c5c4d-110">Добавьте новые входные параметры в конец существующих параметров вместо того, чтобы вставлять их в уже установленную последовательность.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-110">Add new input parameters at the end of the existing parameters rather than inserting them in the already established sequence.</span></span>

<span data-ttu-id="c5c4d-111">В следующей процедуре описывается реализация поставщика методов.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-111">The following procedure describes how to implement a method provider.</span></span>

<span data-ttu-id="c5c4d-112">**Реализация поставщика методов**</span><span class="sxs-lookup"><span data-stu-id="c5c4d-112">**To implement a method provider**</span></span>

1.  <span data-ttu-id="c5c4d-113">Разработка и регистрация поставщика классов с помощью инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-113">Design and register your class provider with WMI.</span></span>

    <span data-ttu-id="c5c4d-114">Поставщики классов регистрируются в WMI путем создания экземпляра [**\_ \_ Win32Provider**](--win32provider.md) и класса [**\_ \_ месодпровидеррегистратион**](--methodproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="c5c4d-114">Class providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_MethodProviderRegistration**](--methodproviderregistration.md) class.</span></span> <span data-ttu-id="c5c4d-115">Дополнительные сведения см. [в разделе Регистрация поставщика методов](registering-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c5c4d-115">For more information, see [Registering a Method Provider](registering-a-method-provider.md).</span></span>

2.  <span data-ttu-id="c5c4d-116">Реализуйте интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-116">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    > [!Note]  
    > <span data-ttu-id="c5c4d-117">Поставщики методов настоятельно рекомендуется использовать модель многопоточности "both".</span><span class="sxs-lookup"><span data-stu-id="c5c4d-117">Method providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="c5c4d-118">Реализуйте метод [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) для вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-118">Implement the [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) method for your provider.</span></span>

    <span data-ttu-id="c5c4d-119">Интерфейс [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) является основным интерфейсом для поставщика метода.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-119">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface is the primary interface for a method provider.</span></span> <span data-ttu-id="c5c4d-120">Дополнительные сведения см. [в разделе Реализация основного интерфейса для поставщика метода](implementing-the-primary-interface-for-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c5c4d-120">For more information, see [Implementing the Primary Interface for a Method Provider](implementing-the-primary-interface-for-a-method-provider.md).</span></span>

4.  <span data-ttu-id="c5c4d-121">Добавьте дополнительный код, необходимый для поставщика.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-121">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="c5c4d-122">При проектировании поставщика вам, скорее всего, придется вызывать интерфейсы WMI.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-122">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="c5c4d-123">Дополнительные сведения см. в разделе [вызов метода](calling-a-method.md) и [обслуживание уровней безопасности в поставщике](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c5c4d-123">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="c5c4d-124">При получении сведений для клиента может потребоваться доступ к уровням безопасности для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-124">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="c5c4d-125">Дополнительные сведения см. в разделе [олицетворение клиента](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="c5c4d-125">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="c5c4d-126">Замените имеющийся поставщик новым кодом.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-126">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="c5c4d-127">Вам не нужно выполнять этот шаг, если у вас нет уже существующего поставщика для копирования.</span><span class="sxs-lookup"><span data-stu-id="c5c4d-127">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="c5c4d-128">Дополнительные сведения см. [в разделе Обновление поставщика](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c5c4d-128">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



