---
title: Теперь операционная система управляет питанием оптических дисков.
description: Теперь операционная система управляет питанием оптических дисков.
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "103794202"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a><span data-ttu-id="8ef7a-103">Теперь операционная система управляет питанием оптических дисков.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-103">Operating system now controls power to optical disk drives</span></span>

## <a name="platforms"></a><span data-ttu-id="8ef7a-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="8ef7a-104">Platforms</span></span>

<span data-ttu-id="8ef7a-105">**Клиенты** — Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ef7a-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="8ef7a-106">**Серверы** — Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ef7a-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="8ef7a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8ef7a-107">Description</span></span>

<span data-ttu-id="8ef7a-108">В предыдущих версиях Windows питание оптического дисковода не было управляемым, если оптический дисковод не использовался.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-108">In previous versions of Windows, power to the optical drive was not managed when the optical drive was not in use.</span></span> <span data-ttu-id="8ef7a-109">Теперь, если на оптическом диске нет носителя (НЕЧЕТного), операционная система выключает питание на оптический диск.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-109">Now, if there is no media present in the optical disk drive (ODD), the operating system turns off the power to the optical drive.</span></span> <span data-ttu-id="8ef7a-110">Эта функция называется 0 Power НЕЧЕТная (ЗПОДД).</span><span class="sxs-lookup"><span data-stu-id="8ef7a-110">This feature is called zero power ODD (ZPODD).</span></span> <span data-ttu-id="8ef7a-111">Эта функция применима только к дисководам оптических дисков, использующим соединитель SATA форм-фактора slimline (с последовательным подключением).</span><span class="sxs-lookup"><span data-stu-id="8ef7a-111">The feature is applicable only to optical drives that use a Slimline SATA (Serial Advanced Technology Attachment) connector.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8ef7a-112">Проявление</span><span class="sxs-lookup"><span data-stu-id="8ef7a-112">Manifestation</span></span>

<span data-ttu-id="8ef7a-113">В этом новом поведении не обнаружено негативных последствий. Однако следует иметь в виду, что это может привести к непредвиденному поведению мультимедийного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-113">We have not found any negative impacts from this new behavior; however, you should be aware of it as it may result in unexpected behavior of media-writing software.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8ef7a-114">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="8ef7a-114">Mitigation</span></span>

<span data-ttu-id="8ef7a-115">Чтобы вернуться к состоянию Always on, отключите эту функцию в реестре.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-115">To revert to always-on status, turn off this functionality in the Registry.</span></span> <span data-ttu-id="8ef7a-116">Абсолютный путь к значению реестра:</span><span class="sxs-lookup"><span data-stu-id="8ef7a-116">The absolute path to the registry value is:</span></span>

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

<span data-ttu-id="8ef7a-117">Его тип — DWORD (32 бит), и если его значение равно 0, то ЗПОДД отключена; Если это любое другое значение, то ЗПОДД включен.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-117">Its type is DWORD (32 bit), and if its value is 0, then ZPODD is disabled; if it’s any other value, then ZPODD is enabled.</span></span>

## <a name="tests"></a><span data-ttu-id="8ef7a-118">Тесты</span><span class="sxs-lookup"><span data-stu-id="8ef7a-118">Tests</span></span>

<span data-ttu-id="8ef7a-119">Протестируйте программное обеспечение на основе мультимедиа для всех аномалий, возникающих из-за этой новой функции.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-119">Test your media-writing software for any anomalies that occur due to this new feature.</span></span> <span data-ttu-id="8ef7a-120">[Сообщите корпорации Майкрософт](mailto:OptIssue@microsoft.com) о любых проблемах, обнаруженных с помощью этой новой функции.</span><span class="sxs-lookup"><span data-stu-id="8ef7a-120">Please [inform Microsoft](mailto:OptIssue@microsoft.com) of any issues you find with this new feature.</span></span>

 

 




