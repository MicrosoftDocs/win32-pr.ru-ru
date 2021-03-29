---
description: Профиль 802.1 X содержит следующие элементы схемы.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Элементы схемы OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813633"
---
# <a name="onex-schema-elements"></a><span data-ttu-id="15569-103">Элементы схемы OneX</span><span class="sxs-lookup"><span data-stu-id="15569-103">OneX Schema Elements</span></span>

<span data-ttu-id="15569-104">Профиль 802.1 X содержит следующие элементы схемы.</span><span class="sxs-lookup"><span data-stu-id="15569-104">An 802.1X profile contains the following schema elements.</span></span> <span data-ttu-id="15569-105">Все элементы схемы OneX применяются к профилям проводного и беспроводного подключения.</span><span class="sxs-lookup"><span data-stu-id="15569-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="15569-106">Большинство именованных элементов находятся в пространстве имен `https://www.microsoft.com/networking/OneX/v1` , за исключением [**Еапконфиг (OneX)**](onexschema-eapconfig-onex-element.md) , который находится в пространстве имен `https://www.microsoft.com/provisioning/EapHostConfig` .</span><span class="sxs-lookup"><span data-stu-id="15569-106">Most of the named elements are in the namespace `https://www.microsoft.com/networking/OneX/v1`, except for [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) which is in the namespace `https://www.microsoft.com/provisioning/EapHostConfig`.</span></span>

<span data-ttu-id="15569-107">В следующем списке показаны определенные элементы в порядке, в котором элементы отображаются в профиле.</span><span class="sxs-lookup"><span data-stu-id="15569-107">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="15569-108">Упорядочение элементов выполняется принудительно.</span><span class="sxs-lookup"><span data-stu-id="15569-108">The ordering of elements is enforced.</span></span> <span data-ttu-id="15569-109">Не все элементы находятся в каждом профиле, поскольку некоторые элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="15569-109">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="15569-110">В этом списке не отображаются все возможные элементы, которые могут отображаться в профиле, так как элементы можно добавлять в **xs: любые** точки вставки.</span><span class="sxs-lookup"><span data-stu-id="15569-110">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="15569-111">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="15569-111">**OneX**</span></span>](onexschema-onex-element.md)
    -   [<span data-ttu-id="15569-112">**Качеусердата (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-112">**cacheUserData (OneX)**</span></span>](onexschema-cacheuserdata-onex-element.md)
    -   [<span data-ttu-id="15569-113">**Хелдпериод (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-113">**heldPeriod (OneX)**</span></span>](onexschema-heldperiod-onex-element.md)
    -   [<span data-ttu-id="15569-114">**Ауспериод (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-114">**authPeriod (OneX)**</span></span>](onexschema-authperiod-onex-element.md)
    -   [<span data-ttu-id="15569-115">**Стартпериод (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-115">**startPeriod (OneX)**</span></span>](onexschema-startperiod-onex-element.md)
    -   [<span data-ttu-id="15569-116">**Максстарт (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-116">**maxStart (OneX)**</span></span>](onexschema-maxstart-onex-element.md)
    -   [<span data-ttu-id="15569-117">**Максаусфаилурес (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-117">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
    -   [<span data-ttu-id="15569-118">**Суппликантмоде (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-118">**supplicantMode (OneX)**</span></span>](onexschema-supplicantmode-onex-element.md)
    -   [<span data-ttu-id="15569-119">**Аусмоде (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-119">**authMode (OneX)**</span></span>](onexschema-authmode-onex-element.md)
    -   [<span data-ttu-id="15569-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
        -   [<span data-ttu-id="15569-121">**тип (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="15569-121">**type (singleSignOn)**</span></span>](onexschema-type-singlesignon-element.md)
        -   [<span data-ttu-id="15569-122">**Максделай (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="15569-122">**maxDelay (singleSignOn)**</span></span>](onexschema-maxdelay-singlesignon-element.md)
        -   [<span data-ttu-id="15569-123">**Усербаседвиртуаллан (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="15569-123">**userBasedVirtualLan (singleSignOn)**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [<span data-ttu-id="15569-124">**Еапконфиг (OneX)**</span><span class="sxs-lookup"><span data-stu-id="15569-124">**EAPConfig (OneX)**</span></span>](onexschema-eapconfig-onex-element.md)

 

 



