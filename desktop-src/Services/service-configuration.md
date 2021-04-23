---
description: Система использует сведения о конфигурации для определения способа запуска службы.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Конфигурация службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541122"
---
# <a name="service-configuration"></a><span data-ttu-id="83965-103">Конфигурация службы</span><span class="sxs-lookup"><span data-stu-id="83965-103">Service Configuration</span></span>

<span data-ttu-id="83965-104">Система использует сведения о конфигурации для определения способа запуска службы.</span><span class="sxs-lookup"><span data-stu-id="83965-104">The system uses the configuration information to determine how to start the service.</span></span> <span data-ttu-id="83965-105">Сведения о конфигурации также включают отображаемое имя службы и ее описание.</span><span class="sxs-lookup"><span data-stu-id="83965-105">The configuration information also includes the service display name and its description.</span></span> <span data-ttu-id="83965-106">Например, для службы DHCP можно использовать отображаемое имя "Служба протокола настройки динамического узла" и описание "предоставляет адреса Интернета для компьютера в сети".</span><span class="sxs-lookup"><span data-stu-id="83965-106">For example, for the DHCP service, you could use the display name "Dynamic Host Configuration Protocol Service" and the description "Provides internet addresses for computer on your network."</span></span>

<span data-ttu-id="83965-107">Чтобы изменить сведения о конфигурации для объекта службы, программа настройки использует функцию [**чанжесервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) или [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="83965-107">To modify the configuration information for a service object, a configuration program uses the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function.</span></span> <span data-ttu-id="83965-108">Пример см. в разделе [изменение конфигурации службы](changing-a-service-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="83965-108">For an example, see [Changing a Service Configuration](changing-a-service-configuration.md).</span></span>

<span data-ttu-id="83965-109">Чтобы получить сведения о конфигурации для объекта службы, программа настройки использует функцию [**куерисервицеконфиг**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) или [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) .</span><span class="sxs-lookup"><span data-stu-id="83965-109">To retrieve the configuration information for a service object, the configuration program uses the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) or [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) function.</span></span> <span data-ttu-id="83965-110">Пример см. в разделе [запросы к конфигурации службы](querying-a-service-s-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="83965-110">For an example, see [Querying a Service's Configuration](querying-a-service-s-configuration.md).</span></span>

<span data-ttu-id="83965-111">Функции конфигурации службы [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) и [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) поддерживают использование триггеров для управления запуском службы.</span><span class="sxs-lookup"><span data-stu-id="83965-111">The [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) service configuration functions support the use of triggers to control service start.</span></span>

<span data-ttu-id="83965-112">Чтобы изменить дескриптор безопасности для объекта SCManager или объекта службы, программа настройки использует функцию [**сетсервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="83965-112">To modify the security descriptor for either an SCManager object or a service object, a configuration program uses the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function.</span></span> <span data-ttu-id="83965-113">Чтобы получить копию дескриптора безопасности, программа настройки использует функцию [**куерисервицеобжектсекурити**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="83965-113">To retrieve a copy of the security descriptor, the configuration program uses the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83965-114">См. также</span><span class="sxs-lookup"><span data-stu-id="83965-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83965-115">Настройка службы с помощью SC</span><span class="sxs-lookup"><span data-stu-id="83965-115">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
