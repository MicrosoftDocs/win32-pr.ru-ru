---
title: D (API-интерфейсы UPnP)
description: Содержит термины, связанные с UPnP, которые начинаются с буквы D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9acec267-3f8b-4906-bb0e-a1411d218043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d92678413f407434c50106ae79ff4836efa58b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105691724"
---
# <a name="d-upnp-apis"></a><span data-ttu-id="694ee-103">D (API-интерфейсы UPnP)</span><span class="sxs-lookup"><span data-stu-id="694ee-103">D (UPnP APIs)</span></span>

<span data-ttu-id="694ee-104">Содержит термины, связанные с UPnP, которые начинаются с буквы D.</span><span class="sxs-lookup"><span data-stu-id="694ee-104">Contains UPnP-related terms that begin with the letter D.</span></span>

<span data-ttu-id="694ee-105">[A](a-gly.md) B [C](c-gly.md) D [E](e-gly.md) F G [р](h-gly.md) . J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="694ee-105">[A](a-gly.md) B [C](c-gly.md) D [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="694ee-106"><span id="upnp.d_1_gly"></span><span id="UPNP.D_1_GLY"></span>**модем**</span><span class="sxs-lookup"><span data-stu-id="694ee-106"><span id="upnp.d_1_gly"></span><span id="UPNP.D_1_GLY"></span>**device**</span></span>
</dt> <dd>

<span data-ttu-id="694ee-107">Устройство — это контейнер других служб или устройств.</span><span class="sxs-lookup"><span data-stu-id="694ee-107">A device is a container of other services or devices.</span></span> <span data-ttu-id="694ee-108">Устройство может содержать другие логические устройства.</span><span class="sxs-lookup"><span data-stu-id="694ee-108">A device can contain other logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="694ee-109"><span id="upnp.d_2_gly"></span><span id="UPNP.D_2_GLY"></span>**объект управления устройством**</span><span class="sxs-lookup"><span data-stu-id="694ee-109"><span id="upnp.d_2_gly"></span><span id="UPNP.D_2_GLY"></span>**device control object**</span></span>
</dt> <dd>

<span data-ttu-id="694ee-110">Объект управления устройством является центральной точкой управления для объектов службы устройства.</span><span class="sxs-lookup"><span data-stu-id="694ee-110">A device control object is the central point of management for a device's service objects.</span></span> <span data-ttu-id="694ee-111">При регистрации устройства его объект управления устройством передается на узел устройства.</span><span class="sxs-lookup"><span data-stu-id="694ee-111">When a device is registered, its device control object is passed to the device host.</span></span>

</dd> <dt>

<span data-ttu-id="694ee-112"><span id="upnp.d_3_gly"></span><span id="UPNP.D_3_GLY"></span>**Описание устройства**</span><span class="sxs-lookup"><span data-stu-id="694ee-112"><span id="upnp.d_3_gly"></span><span id="UPNP.D_3_GLY"></span>**device description**</span></span>
</dt> <dd>

<span data-ttu-id="694ee-113">Описание устройства — это список универсальных свойств всех устройств на физическом устройстве, включая службы, иерархию устройства и его свойства.</span><span class="sxs-lookup"><span data-stu-id="694ee-113">A device description is a list of the generic properties of all the devices in a physical device, including the services, the device's hierarchy, and its properties.</span></span>

</dd> <dt>

<span data-ttu-id="694ee-114"><span id="upnp.d_4_gly"></span><span id="UPNP.D_4_GLY"></span>**узел устройства**</span><span class="sxs-lookup"><span data-stu-id="694ee-114"><span id="upnp.d_4_gly"></span><span id="UPNP.D_4_GLY"></span>**device host**</span></span>
</dt> <dd>

<span data-ttu-id="694ee-115">Узел устройства обрабатывает части функций обнаружения, описания, управления и работы с событиями устройства.</span><span class="sxs-lookup"><span data-stu-id="694ee-115">The device host handles the discovery, description, control, and eventing portions of a device's functionality.</span></span> <span data-ttu-id="694ee-116">Устройства содержат код для обработки функций конкретного устройства, таких как Перемотка ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="694ee-116">Devices contain the code to handle the device-specific functionality, such as rewinding a VCR.</span></span>

</dd> <dt>

<span data-ttu-id="694ee-117"><span id="upnp.d_5_gly"></span><span id="UPNP.D_5_GLY"></span>**Поставщик устройства**</span><span class="sxs-lookup"><span data-stu-id="694ee-117"><span id="upnp.d_5_gly"></span><span id="UPNP.D_5_GLY"></span>**device provider**</span></span>
</dt> <dd>

<span data-ttu-id="694ee-118">Поставщик устройств — это сущность, зарегистрированная на узле устройства.</span><span class="sxs-lookup"><span data-stu-id="694ee-118">A device provider is an entity that is registered with the device host.</span></span> <span data-ttu-id="694ee-119">Этот поставщик устройств не опубликован в сети.</span><span class="sxs-lookup"><span data-stu-id="694ee-119">This device provider is not published on the network.</span></span> <span data-ttu-id="694ee-120">Однако поставщик устройства регистрирует другие устройства и публикует их в сети.</span><span class="sxs-lookup"><span data-stu-id="694ee-120">However, the device provider registers other devices and publishes them on the network.</span></span>

</dd> <dt>

<span data-ttu-id="694ee-121"><span id="upnp.d_6_gly"></span><span id="UPNP.D_6_GLY"></span>**Тип устройства**</span><span class="sxs-lookup"><span data-stu-id="694ee-121"><span id="upnp.d_6_gly"></span><span id="UPNP.D_6_GLY"></span>**device type**</span></span>
</dt> <dd>

<span data-ttu-id="694ee-122">Тип устройства "Стандартный" обозначается универсальным именем URN: schemas-UPnP-org: Device:, за которым следует уникальное имя, назначенное форумом UPnP.</span><span class="sxs-lookup"><span data-stu-id="694ee-122">A standard device type is denoted by urn:schemas-upnp-org:device: followed by a unique name assigned by the UPnP Forum.</span></span>

<span data-ttu-id="694ee-123">Между шаблонами устройств на основе UPnP и типами устройств существует связь «один к одному».</span><span class="sxs-lookup"><span data-stu-id="694ee-123">There is a one-to-one relationship between UPnP-based device templates and device types.</span></span> <span data-ttu-id="694ee-124">Поставщики UPnP могут указывать дополнительные типы устройств; они обозначаются urn: domain-name: Device:, за которым следует уникальное имя, назначенное поставщиком, где domain-name — это доменное имя, зарегистрированное для поставщика.</span><span class="sxs-lookup"><span data-stu-id="694ee-124">UPnP vendors might specify additional device types; these are denoted by urn:domain-name:device: followed by a unique name assigned by the vendor, where domain-name is a domain name registered to the vendor.</span></span>

</dd> </dl>

 

 




