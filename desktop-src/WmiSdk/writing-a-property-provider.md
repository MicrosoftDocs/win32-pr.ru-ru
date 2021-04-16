---
description: Поставщик свойств извлекает и изменяет отдельные значения свойств для экземпляров заданного класса, хранящегося в репозитории WMI.
ms.assetid: fe150157-cf9d-47da-8f94-b18eb0502bd8
ms.tgt_platform: multiple
title: Создание поставщика свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bf22d927435b5c46f0ec8d8d2cf42ab872a0c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712093"
---
# <a name="writing-a-property-provider"></a><span data-ttu-id="f3f8b-103">Создание поставщика свойств</span><span class="sxs-lookup"><span data-stu-id="f3f8b-103">Writing a Property Provider</span></span>

<span data-ttu-id="f3f8b-104">Поставщик свойств извлекает и изменяет отдельные значения свойств для экземпляров заданного класса, хранящегося в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-104">A property provider retrieves and modifies individual property values for instances of a given class that is stored in the WMI repository.</span></span>

<span data-ttu-id="f3f8b-105">В следующей процедуре описывается создание поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-105">The following procedure describes how to create a property provider.</span></span>

<span data-ttu-id="f3f8b-106">**Создание поставщика свойств**</span><span class="sxs-lookup"><span data-stu-id="f3f8b-106">**To create a property provider**</span></span>

1.  <span data-ttu-id="f3f8b-107">Разработка и регистрация поставщика с помощью WMI.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-107">Design and register your provider with WMI.</span></span>

    <span data-ttu-id="f3f8b-108">Поставщики экземпляров регистрируются в WMI путем создания экземпляра [**\_ \_ Win32Provider**](--win32provider.md) и класса [**\_ \_ пропертипровидеррегистратион**](--propertyproviderregistration.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f8b-108">Instance providers register with WMI by creating a [**\_\_Win32Provider**](--win32provider.md) instance and a [**\_\_PropertyProviderRegistration**](--propertyproviderregistration.md) class.</span></span> <span data-ttu-id="f3f8b-109">Дополнительные сведения см. [в разделе Регистрация поставщика свойств](registering-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3f8b-109">For more information, see [Registering a Property Provider](registering-a-property-provider.md).</span></span>

2.  <span data-ttu-id="f3f8b-110">Реализуйте интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-110">Implement the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface for your provider.</span></span>

    <span data-ttu-id="f3f8b-111">Инструментарий WMI использует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для загрузки и инициализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-111">WMI uses [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) to load and initialize a provider.</span></span> <span data-ttu-id="f3f8b-112">Это задача, общая для всех поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-112">This is a task common to all providers.</span></span> <span data-ttu-id="f3f8b-113">Дополнительные сведения см. [в разделе Инициализация поставщика](initializing-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3f8b-113">For more information, see [Initializing a Provider](initializing-a-provider.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="f3f8b-114">Поставщики свойств настоятельно рекомендуется использовать модель многопоточности "both".</span><span class="sxs-lookup"><span data-stu-id="f3f8b-114">Property providers are strongly encouraged to use the multithreading model "Both".</span></span>

     

3.  <span data-ttu-id="f3f8b-115">Реализуйте интерфейс [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) для поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-115">Implement the [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface for your provider.</span></span>

    <span data-ttu-id="f3f8b-116">Интерфейс [**ивбемпропертипровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) является основным интерфейсом для поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-116">The [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) interface is the primary interface for a property provider.</span></span> <span data-ttu-id="f3f8b-117">Двумя основными методами являются [**Свойства**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) [**putproperty изменил**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty)и.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-117">The two main methods are [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) and [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty).</span></span> <span data-ttu-id="f3f8b-118">Дополнительные сведения см. [в разделе Реализация основного интерфейса для поставщика свойств](implementing-the-primary-interface-for-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3f8b-118">For more information, see [Implementing the Primary Interface for a Property Provider](implementing-the-primary-interface-for-a-property-provider.md).</span></span>

4.  <span data-ttu-id="f3f8b-119">Добавьте дополнительный код, необходимый для поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-119">Add any additional code necessary for your provider.</span></span>

    <span data-ttu-id="f3f8b-120">При проектировании поставщика вам, скорее всего, придется вызывать интерфейсы WMI.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-120">When designing your provider, you will most likely need to call WMI interfaces.</span></span> <span data-ttu-id="f3f8b-121">Дополнительные сведения см. в разделе [вызов метода](calling-a-method.md) и [обслуживание уровней безопасности в поставщике](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="f3f8b-121">For more information, see [Calling a Method](calling-a-method.md) and [Maintaining Security Levels in a Provider](impersonating-a-client.md).</span></span>

    <span data-ttu-id="f3f8b-122">При получении сведений для клиента может потребоваться доступ к уровням безопасности для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-122">When retrieving information for a client, you may need to access the security levels for that client.</span></span> <span data-ttu-id="f3f8b-123">Дополнительные сведения см. в разделе [олицетворение клиента](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="f3f8b-123">For more information, see [Impersonating a Client](impersonating-a-client.md).</span></span>

5.  <span data-ttu-id="f3f8b-124">Замените имеющийся поставщик новым кодом.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-124">Replace the preexisting provider with your new code.</span></span>

    <span data-ttu-id="f3f8b-125">Вам не нужно выполнять этот шаг, если у вас нет уже существующего поставщика для копирования.</span><span class="sxs-lookup"><span data-stu-id="f3f8b-125">You do not need to perform this step if you do not have a preexisting provider to copy over.</span></span> <span data-ttu-id="f3f8b-126">Дополнительные сведения см. [в разделе Обновление поставщика](updating-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3f8b-126">For more information, see [Updating a Provider](updating-a-provider.md).</span></span>

 

 



