---
title: Доступность применимых драйверов графики на Центр обновления Windows
description: Доступность этих драйверов на Центр обновления Windows (WU) определяет, будет ли пользователь автоматически предлагать обновление с Windows 7, Windows 8 или Windows 8.1 до Windows 10.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691198"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a><span data-ttu-id="6f806-103">Доступность применимых драйверов графики на Центр обновления Windows</span><span class="sxs-lookup"><span data-stu-id="6f806-103">Availability of applicable graphics drivers on Windows Update</span></span>

<span data-ttu-id="6f806-104">Доступность этих драйверов на Центр обновления Windows (WU) определяет, будет ли пользователь автоматически предлагать обновление с Windows 7, Windows 8 или Windows 8.1 до Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6f806-104">The availability of these drivers on Windows Update (WU) will determine whether a user is automatically offered an upgrade from Windows 7, Windows 8 or Windows 8.1 to Windows 10.</span></span> <span data-ttu-id="6f806-105">Если при сканировании оборудования обнаружено отсутствие графического драйвера на Центр обновления Windows для графического адаптера на компьютере, пользователи не предлагали обновленную ОС Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6f806-105">If hardware scans showed that there was no graphics driver available on Windows Update for the graphics adapter in the PC, users were not offered the updated Windows 10 OS.</span></span> <span data-ttu-id="6f806-106">Тем не менее пользователи по-прежнему могут получить Windows 10 через другие источники и вручную выполнить обновление.</span><span class="sxs-lookup"><span data-stu-id="6f806-106">However, users can still obtain Windows 10 through other sources and manually perform the upgrade.</span></span>

<span data-ttu-id="6f806-107">Некоторым пользователям не было уверений в том, почему они не предлагали обновление при других пользователях, хотя советник по переходу объяснил, что для оборудования не существовал графический драйвер.</span><span class="sxs-lookup"><span data-stu-id="6f806-107">Some users were unsure of why they were not offered the upgrade when other people were, even though the Upgrade Advisor explained that there was no graphics driver available for their hardware.</span></span>

<span data-ttu-id="6f806-108">Кроме того, некоторые пользователи принудительно находили обновление, а затем обнаружили, что их графические возможности и производительность были вызваны отсутствием драйвера оборудования.</span><span class="sxs-lookup"><span data-stu-id="6f806-108">Additionally, some users forced an upgrade and then found that their graphics functionality and performance suffered due to the lack of a hardware driver.</span></span>

## <a name="mitigations"></a><span data-ttu-id="6f806-109">Устранение проблем</span><span class="sxs-lookup"><span data-stu-id="6f806-109">Mitigations</span></span>

<span data-ttu-id="6f806-110">Чтобы устранить эту ошибку, пользователи могут вручную установить старый драйвер, т. е. из Windows 7, Windows 8 или Windows 8.1, перейдя на веб-сайт IHV или OEM и загрузив драйвер явным образом.</span><span class="sxs-lookup"><span data-stu-id="6f806-110">To mitigate this, users can manually install an older driver, i.e. from Windows 7, Windows 8 or Windows 8.1, by going to the IHV or OEM web site and downloading a driver explicitly.</span></span> <span data-ttu-id="6f806-111">Это необходимо сделать после обновления и не гарантирует работу.</span><span class="sxs-lookup"><span data-stu-id="6f806-111">This must be done after the upgrade and is not guaranteed to work.</span></span> <span data-ttu-id="6f806-112">Нет поддерживаемого решения, если подходящий графический драйвер недоступен в WU.</span><span class="sxs-lookup"><span data-stu-id="6f806-112">There is no supported solution if a suitable graphics driver is not available on WU.</span></span> <span data-ttu-id="6f806-113">Пользователь должен решить, нужно ли:</span><span class="sxs-lookup"><span data-stu-id="6f806-113">The user must decide whether to:</span></span>

-   <span data-ttu-id="6f806-114">Остаться в предыдущей ОС;</span><span class="sxs-lookup"><span data-stu-id="6f806-114">Remain on the previous OS;</span></span>
-   <span data-ttu-id="6f806-115">Примите ограничения для драйвера программного обеспечения, Microsoft Basic видеоадаптер (МСБДА); ни</span><span class="sxs-lookup"><span data-stu-id="6f806-115">Accept the limitations of the software driver, Microsoft Basic Display Adapter (MSBDA); or</span></span>
-   <span data-ttu-id="6f806-116">Приобретите новую графическую карту с поддерживаемым драйвером Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6f806-116">Buy a new graphics card that has a supported Windows 10 driver.</span></span>

## <a name="solutions"></a><span data-ttu-id="6f806-117">Решения</span><span class="sxs-lookup"><span data-stu-id="6f806-117">Solutions</span></span>

<span data-ttu-id="6f806-118">Очень важно, чтобы независимые поставщики программного обеспечения и изготовители оборудования передают свои графические драйверы Windows 10 в WU для любого оборудования, которое они должны поддерживать.</span><span class="sxs-lookup"><span data-stu-id="6f806-118">It’s critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="6f806-119">Обратите внимание, что оборудование, которое достигло конца Live (конца строки), может не иметь драйверов в WU.</span><span class="sxs-lookup"><span data-stu-id="6f806-119">Note that hardware that has reached End-Of-Live (EOL) might not have drivers on WU.</span></span> <span data-ttu-id="6f806-120">В этом случае нет решения — пользователь должен выбрать один из параметров в разделе Устранение рисков выше.</span><span class="sxs-lookup"><span data-stu-id="6f806-120">There is no solution in this case – the user must choose one of the options under Mitigations above.</span></span>

 

 




