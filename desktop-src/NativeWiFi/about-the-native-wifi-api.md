---
description: Собственный API Wi-Fi содержит функции, структуры и перечисления, поддерживающие беспроводное подключение и Управление профилем беспроводной сети.
ms.assetid: 686f9ccf-5040-44c5-8633-83f12dc46586
title: Сведения о встроенном API Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280d4f656145430e34d79e05b88bc2bdeb54fe5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272462"
---
# <a name="about-the-native-wifi-api"></a><span data-ttu-id="7bcc6-103">Сведения о встроенном API Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="7bcc6-103">About the Native Wifi API</span></span>

<span data-ttu-id="7bcc6-104">Собственный API Wi-Fi содержит функции, структуры и перечисления, поддерживающие беспроводное подключение и Управление профилем беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-104">The Native Wifi API contains functions, structures, and enumerations that support wireless network connectivity and wireless profile management.</span></span> <span data-ttu-id="7bcc6-105">API можно использовать как для инфраструктуры, так и для нерегламентированных сетей.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-105">The API can be used for both infrastructure and ad hoc networks.</span></span> <span data-ttu-id="7bcc6-106">Нерегламентированный интерфейс API — это упрощенный объектно-ориентированный интерфейс для создания, управления и использования нерегламентированных сетей.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-106">The Wireless Ad Hoc API is a simplified object-oriented interface for creating, managing, and using ad hoc networks.</span></span>

> [!Note]  
> <span data-ttu-id="7bcc6-107">Нерегламентированный режим может быть недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-107">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="7bcc6-108">Начиная с Windows 8.1 и Windows Server 2012 R2, следует использовать [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="7bcc6-108">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

<span data-ttu-id="7bcc6-109">Реализация нерегламентированного API использует собственный API Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-109">The implementation of the Ad Hoc API uses the Native Wifi API.</span></span> <span data-ttu-id="7bcc6-110">Это означает, что нерегламентированные вызовы API могут активировать собственные уведомления WiFi и наоборот.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-110">This means that Ad Hoc API calls can trigger Native Wifi notifications, and vice versa.</span></span>

<span data-ttu-id="7bcc6-111">Не рекомендуется смешивать собственные вызовы API WiFi и нерегламентированные вызовы API.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-111">Mixing Native Wifi API calls and Wireless Ad Hoc API calls is not recommended.</span></span> <span data-ttu-id="7bcc6-112">Разработчики должны выбрать подход к программированию перед проектированием приложения.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-112">Developers should choose a programming approach before designing an application.</span></span> <span data-ttu-id="7bcc6-113">Если приложение использует сети инфраструктуры или управляет ими, следует использовать собственный API Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-113">If your application uses or manages infrastructure networks, you should use the Native Wifi API.</span></span> <span data-ttu-id="7bcc6-114">Если приложению требуются функции управления профилями, следует использовать собственный API Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-114">If your application requires profile management functionality, you should use the Native Wifi API.</span></span> <span data-ttu-id="7bcc6-115">В противном случае следует использовать нерегламентированный интерфейс API.</span><span class="sxs-lookup"><span data-stu-id="7bcc6-115">Otherwise, you should use the Wireless Ad Hoc API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bcc6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="7bcc6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bcc6-117">О встроенных WiFi</span><span class="sxs-lookup"><span data-stu-id="7bcc6-117">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="7bcc6-118">Встроенная поддержка интерфейса API WiFi в Windows XP</span><span class="sxs-lookup"><span data-stu-id="7bcc6-118">Native Wifi API Support on Windows XP</span></span>](about-wireless-lan-api-for-windows-xp-service-pack-2.md)
</dt> <dt>

[<span data-ttu-id="7bcc6-119">Собственные разрешения API WiFi</span><span class="sxs-lookup"><span data-stu-id="7bcc6-119">Native Wifi API Permissions</span></span>](native-wifi-api-permissions.md)
</dt> <dt>

[<span data-ttu-id="7bcc6-120">Сведения о беспроводном нерегламентированном API</span><span class="sxs-lookup"><span data-stu-id="7bcc6-120">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="7bcc6-121">Загрузка пакета SDK для Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bcc6-121">Download the Windows Vista SDK</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)
</dt> </dl>

 

 



