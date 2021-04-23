---
title: Проверки ядра для драйверов, не подписанных WHQL
description: Для устройств, на которых чистая установка Windows 10 и где включена безопасная загрузка (Обратите внимание, что это стандартный вариант для всех новых устройств, начиная с выпуска Windows 8,0), все новые драйверы должны быть подписаны WHQL/Сисдев, а не просто использоваться с перекрестной подписью сертификатов.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411233"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a><span data-ttu-id="06075-103">Проверки ядра для драйверов, не подписанных WHQL</span><span class="sxs-lookup"><span data-stu-id="06075-103">Kernel checks for non-WHQL signed drivers</span></span>

<span data-ttu-id="06075-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="06075-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="06075-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="06075-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="06075-106">Для устройств, на которых чистая установка Windows 10 и где включена безопасная загрузка (Обратите внимание, что это стандартный вариант для всех новых устройств, начиная с выпуска Windows 8,0), все новые драйверы должны быть подписаны WHQL/Сисдев, а не просто использоваться с перекрестной подписью сертификатов.</span><span class="sxs-lookup"><span data-stu-id="06075-106">For devices that clean install Windows 10, and where Secure Boot is on (note that this is standard for all new devices since the release of Windows 8.0), all new drivers must be signed by WHQL/Sysdev rather than just use cross-signed certificates.</span></span> <span data-ttu-id="06075-107">Обновленные устройства и случаи, когда драйверы были подписаны с помощью перекрестных сертификатов, прежде чем эта политика вступит в действие, исключается из этой политики, чтобы обеспечить обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="06075-107">Devices that are upgraded and cases where drivers have been signed with a cross-cert before this policy went into effect are excluded from this policy to ensure backwards compatibility.</span></span> <span data-ttu-id="06075-108">Эта политика была объявлена как апрель 2015, однако она будет применена к выпуску годовщины Windows, выпущенной 2016 августа.</span><span class="sxs-lookup"><span data-stu-id="06075-108">This policy was announced April 2015, however it will be enforced with the Windows Anniversary Edition, released August 2016.</span></span>

<span data-ttu-id="06075-109">В случаях, когда драйвер не подписан должным образом, он будет проявляться как уведомление PCA о том, что драйверы заблокированы, если они не прошли требования к подписи.</span><span class="sxs-lookup"><span data-stu-id="06075-109">In cases where a driver is not signed correctly, it will manifest as a PCA notification that the driver(s) is blocked when it doesn’t pass signature requirements.</span></span> <span data-ttu-id="06075-110">Это предотвращает непрозрачное блокирование автономного взаимодействия пользователя драйвера в ядре.</span><span class="sxs-lookup"><span data-stu-id="06075-110">This prevents a later disconnected user experience of the driver being blocked in kernel transparently.</span></span>

<span data-ttu-id="06075-111">Дополнительные сведения см. в [этой записи блога](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), которая сообщает об изменении подписи драйвера.</span><span class="sxs-lookup"><span data-stu-id="06075-111">For more information, please refer to [this blog post](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), which announces the driver signing change.</span></span>

 

 




