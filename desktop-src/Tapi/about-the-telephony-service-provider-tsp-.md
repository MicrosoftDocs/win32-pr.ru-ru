---
description: Поставщик услуг телефонии TAPI (TSP) — это библиотека динамической компоновки (DLL), которая поддерживает управление устройствами связи с помощью набора экспортированных функций службы.
ms.assetid: 6e4fb295-940e-4f76-ad43-fad7da90094a
title: О поставщике услуг телефонии (TSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5200a4291bdd91aba9f93a5552fecf4b52d24ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809244"
---
# <a name="about-the-telephony-service-provider-tsp"></a><span data-ttu-id="e8f25-103">О поставщике услуг телефонии (TSP)</span><span class="sxs-lookup"><span data-stu-id="e8f25-103">About the Telephony Service Provider (TSP)</span></span>

<span data-ttu-id="e8f25-104">\[ H323 и Ипконф специалистами недоступны для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e8f25-104">\[ The H323 and IPConf TSPs are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e8f25-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="e8f25-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e8f25-106">Поставщик услуг телефонии TAPI (TSP) — это библиотека динамической компоновки (DLL), которая поддерживает управление устройствами связи с помощью набора экспортированных функций службы.</span><span class="sxs-lookup"><span data-stu-id="e8f25-106">A TAPI telephony service provider (TSP) is a dynamic-link library (DLL) that supports communications device control through a set of exported service functions.</span></span> <span data-ttu-id="e8f25-107">Приложение TAPI использует стандартизованные команды, TAPI передается в состав поставщика услуг телефонии, а TSP обрабатывает конкретные команды, которые должны обмениваться данными с устройством.</span><span class="sxs-lookup"><span data-stu-id="e8f25-107">A TAPI application uses standardized commands, TAPI passes in formation to the telephony service provider, and the TSP handles the specific commands that must be exchanged with the device.</span></span>

<span data-ttu-id="e8f25-108">В следующих разделах кратко описаны специалистами, предоставляемые в Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e8f25-108">The following sections briefly describe the TSPs provided with Microsoft Windows:</span></span>

-   [<span data-ttu-id="e8f25-109">H323 TSP</span><span class="sxs-lookup"><span data-stu-id="e8f25-109">H323 TSP</span></span>](h323-tsp.md)
-   [<span data-ttu-id="e8f25-110">Ипконф TSP</span><span class="sxs-lookup"><span data-stu-id="e8f25-110">IPConf TSP</span></span>](ipconf-tsp.md)
-   [<span data-ttu-id="e8f25-111">TSP драйвера устройства в режиме ядра</span><span class="sxs-lookup"><span data-stu-id="e8f25-111">Kernel-Mode Device Driver TSP</span></span>](kernel-mode-device-driver-tsp.md)
-   [<span data-ttu-id="e8f25-112">TSP прокси-сервера NDIS</span><span class="sxs-lookup"><span data-stu-id="e8f25-112">NDIS Proxy TSP</span></span>](ndis-proxy-tsp.md)
-   [<span data-ttu-id="e8f25-113">Удаленный TSP</span><span class="sxs-lookup"><span data-stu-id="e8f25-113">Remote TSP</span></span>](remote-tsp.md)
-   [<span data-ttu-id="e8f25-114">Сторонний TSP</span><span class="sxs-lookup"><span data-stu-id="e8f25-114">Third-Party TSP</span></span>](third-party-tsp.md)
-   [<span data-ttu-id="e8f25-115">TSP Unimodem</span><span class="sxs-lookup"><span data-stu-id="e8f25-115">Unimodem TSP</span></span>](unimodem-tsp.md)

<span data-ttu-id="e8f25-116">Подробные сведения см. в наборе ресурсов для целевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e8f25-116">For detailed information, please see the Resource Kit for the target operating system.</span></span> <span data-ttu-id="e8f25-117">Сторонние специалистами для специализированных коммуникационных устройств, как правило, предоставляются производителем и устанавливаются вместе с устройством.</span><span class="sxs-lookup"><span data-stu-id="e8f25-117">Third-party TSPs for specialized communications devices will typically be provided by the manufacturer and will be installed with the device.</span></span>

<span data-ttu-id="e8f25-118">В следующих разделах описано, как создать TSP, который будет правильно функционировать в среде телефонии Майкрософт, и как создать пару TSP/MSP:</span><span class="sxs-lookup"><span data-stu-id="e8f25-118">The following topics describe how to create a TSP that will function properly within the Microsoft Telephony environment, and how to create a TSP/MSP pair:</span></span>

-   [<span data-ttu-id="e8f25-119">Интерфейс поставщика услуг телефонии (ТСПИ)</span><span class="sxs-lookup"><span data-stu-id="e8f25-119">Telephony Service Provider Interface (TSPI)</span></span>](telephony-service-provider-interface-tspi-.md)
-   [<span data-ttu-id="e8f25-120">Справочник по ТСПИ</span><span class="sxs-lookup"><span data-stu-id="e8f25-120">TSPI Reference</span></span>](tspi-reference.md)
-   [<span data-ttu-id="e8f25-121">Поставщики служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="e8f25-121">Media Service Providers</span></span>](./media-service-providers-start-page.md)

> [!Note]  
> <span data-ttu-id="e8f25-122">TSP — это созданная пользователем библиотека DLL.</span><span class="sxs-lookup"><span data-stu-id="e8f25-122">A TSP is a user-created DLL.</span></span> <span data-ttu-id="e8f25-123">При создании TSP для 64-разрядной платформы Windows ее необходимо компилировать как 64-разрядную библиотеку DLL или библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="e8f25-123">If you are creating a TSP for a 64-bit Windows platform, you must compile it as a 64-bit DLL or DLLs.</span></span>

 

 

 
