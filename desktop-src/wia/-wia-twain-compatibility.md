---
description: WIA обеспечивает уровень совместимости TWAIN, позволяющий приложениям, поддерживающим TWAIN, взаимодействовать с устройствами Windows для получения изображений (WIA).
ms.assetid: 8e5673b9-c234-4722-b244-41aae015ac0c
title: Совместимость с TWAIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc7d0beb9a6001a0cbb4dc0bc032cf4df781736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692413"
---
# <a name="twain-compatibility"></a><span data-ttu-id="30ea1-103">Совместимость с TWAIN</span><span class="sxs-lookup"><span data-stu-id="30ea1-103">TWAIN Compatibility</span></span>

<span data-ttu-id="30ea1-104">WIA обеспечивает уровень совместимости TWAIN, позволяющий приложениям, поддерживающим TWAIN, взаимодействовать с устройствами Windows для получения изображений (WIA).</span><span class="sxs-lookup"><span data-stu-id="30ea1-104">WIA provides a TWAIN compatibility layer that allows TWAIN-aware applications to communicate with Windows Image Acquisition (WIA) devices.</span></span> <span data-ttu-id="30ea1-105">Приложения, поддерживающие TWAIN, не имеют полного доступа к функциональным возможностям WIA.</span><span class="sxs-lookup"><span data-stu-id="30ea1-105">TWAIN-aware applications do not have full access to WIA functionality.</span></span> <span data-ttu-id="30ea1-106">Например, приложение не может подавлять пользовательский интерфейс, используя уровень совместимости TWAIN.</span><span class="sxs-lookup"><span data-stu-id="30ea1-106">For example, an application cannot suppress the user interface using the TWAIN compatibility layer.</span></span>

<span data-ttu-id="30ea1-107">Устройства WIA дважды появляются в приложении, которое учитывает WIA и TWAIN: один раз через нормальную связь WIA и один раз через слой совместимости TWAIN.</span><span class="sxs-lookup"><span data-stu-id="30ea1-107">WIA devices appear twice to an application that is aware of both WIA and TWAIN: once through normal WIA communication, and once through the TWAIN compatibility layer.</span></span> <span data-ttu-id="30ea1-108">Чтобы не перечислять устройство WIA дважды, приложение, которое знает как WIA, так и TWAIN, должно отфильтровать устройства WIA, которые проходят через слой совместимости TWAIN.</span><span class="sxs-lookup"><span data-stu-id="30ea1-108">To avoid listing a WIA device twice, an application that is aware of both WIA and TWAIN must filter out the WIA devices that come through the TWAIN compatibility layer.</span></span> <span data-ttu-id="30ea1-109">Все устройства WIA, которые проходят через слой совместимости TWAIN, имеют префикс "WIA-", поэтому их легко фильтровать.</span><span class="sxs-lookup"><span data-stu-id="30ea1-109">All WIA devices that come through the TWAIN compatibility layer have "WIA-" as a prefix, so it is easy to filter them.</span></span>

 

 



