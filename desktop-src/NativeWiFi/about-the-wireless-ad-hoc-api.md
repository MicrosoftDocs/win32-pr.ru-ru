---
description: Сведения о беспроводном нерегламентированном API
ms.assetid: 9e6e32c5-454b-41c8-b00e-70a2e82266f1
title: Сведения о беспроводном нерегламентированном API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3ac7d87159505a3d69f65ff2e8f5d59adc35b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664486"
---
# <a name="about-the-wireless-ad-hoc-api"></a><span data-ttu-id="bb5ff-103">Сведения о беспроводном нерегламентированном API</span><span class="sxs-lookup"><span data-stu-id="bb5ff-103">About the Wireless Ad Hoc API</span></span>

<span data-ttu-id="bb5ff-104">Нерегламентированный API предоставляет интерфейсы для перечисления и подключения к сетям 802,11 ad hoc.</span><span class="sxs-lookup"><span data-stu-id="bb5ff-104">The Wireless Ad Hoc API exposes interfaces for enumerating and connecting to 802.11 ad hoc networks.</span></span> <span data-ttu-id="bb5ff-105">Эти интерфейсы предоставляют упрощенный объектно-ориентированный подход к управлению сетью ad hoc.</span><span class="sxs-lookup"><span data-stu-id="bb5ff-105">These interfaces provide a simplified object-oriented approach to ad hoc network management.</span></span> <span data-ttu-id="bb5ff-106">Для сетей и интерфейсов предоставляются стандартные перечислители.</span><span class="sxs-lookup"><span data-stu-id="bb5ff-106">Standard enumerators are provided for networks and interfaces.</span></span> <span data-ttu-id="bb5ff-107">Эти Перечислители можно фильтровать для перечисления только нерегламентированных сетей, созданных вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="bb5ff-107">These enumerators can be filtered to enumerate only ad hoc networks created by your application.</span></span>

> [!Note]  
> <span data-ttu-id="bb5ff-108">Нерегламентированный режим может быть недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="bb5ff-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="bb5ff-109">Начиная с Windows 8.1 и Windows Server 2012 R2, следует использовать [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5ff-109">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="bb5ff-110">Разработчикам, использующим нерегламентированный API, следует учитывать, что для управления сетями и профилями, созданными с помощью нерегламентированного API, можно использовать собственный API WiFi, не уведомляя соответствующие нерегламентированные прослушиватели уведомлений API.</span><span class="sxs-lookup"><span data-stu-id="bb5ff-110">Developers using the Ad Hoc API should be aware that networks and profiles created using the Ad Hoc API can be manipulated using the Native Wifi API without notifying the relevant Ad Hoc API notification listeners.</span></span>

<span data-ttu-id="bb5ff-111">Нерегламентированный специальный API подробно описан в [нерегламентированной справочной документации](wireless-ad-hoc-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bb5ff-111">The Wireless Ad Hoc API is described in detail in the [Wireless Ad Hoc Reference](wireless-ad-hoc-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="bb5ff-112">Нерегламентированный API-интерфейс беспроводных сетей поддерживается только в Windows Vista и более поздних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bb5ff-112">The Wireless Ad Hoc API is only supported on Windows Vista and later versions of the operating system.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="bb5ff-113">См. также</span><span class="sxs-lookup"><span data-stu-id="bb5ff-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb5ff-114">О встроенных WiFi</span><span class="sxs-lookup"><span data-stu-id="bb5ff-114">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="bb5ff-115">Сведения о встроенном API Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="bb5ff-115">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> </dl>

 

 



