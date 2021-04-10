---
description: Определяет элементы конфигурации 802.1 X.
ms.assetid: 4755356e-cb4b-4eed-a494-ca0d17f5184f
title: Схема OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9df45ed7981c055e955afe72333a42db99ddb21a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264377"
---
# <a name="onex-schema"></a><span data-ttu-id="9bdcb-103">Схема OneX</span><span class="sxs-lookup"><span data-stu-id="9bdcb-103">OneX Schema</span></span>

<span data-ttu-id="9bdcb-104">Схема OneX определяет элементы конфигурации 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-104">The OneX Schema defines 802.1X configuration elements.</span></span> <span data-ttu-id="9bdcb-105">Все элементы схемы OneX применяются к профилям проводного и беспроводного подключения.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="9bdcb-106">Список определенных элементов см. в разделе [элементы схемы OneX](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="9bdcb-106">For a list of defined elements, see [OneX Schema Elements](onexschema-elements.md).</span></span>

<span data-ttu-id="9bdcb-107">Корневым элементом профиля 802.1 X является элемент [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9bdcb-107">The root element of an 802.1X profile is the [**OneX**](onexschema-onex-element.md) element.</span></span> <span data-ttu-id="9bdcb-108">Каждый профиль будет иметь только один корневой элемент.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-108">Each profile will have exactly one root element.</span></span> <span data-ttu-id="9bdcb-109">Элемент **OneX** находится в `https://www.microsoft.com/networking/OneX/v1` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="9bdcb-109">The **OneX** element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="9bdcb-110">Чтобы просмотреть образцы профилей для беспроводных сетей, включающих элементы конфигурации 802.1 X, см. следующие примеры профилей:</span><span class="sxs-lookup"><span data-stu-id="9bdcb-110">To view sample profiles for wireless networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="9bdcb-111">Образец профиля начальной загрузки</span><span class="sxs-lookup"><span data-stu-id="9bdcb-111">Bootstrap Profile Sample</span></span>](bootstrap-profile-sample.md)
-   [<span data-ttu-id="9bdcb-112">Пример профиля FIPS</span><span class="sxs-lookup"><span data-stu-id="9bdcb-112">FIPS Profile Sample</span></span>](fips-profile-sample.md)
-   [<span data-ttu-id="9bdcb-113">Пример профиля с одним Sign-On</span><span class="sxs-lookup"><span data-stu-id="9bdcb-113">Single Sign-On Profile Sample</span></span>](single-sign-on-profile-sample.md)
-   [<span data-ttu-id="9bdcb-114">Пример профиля WPA-Enterprise с PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="9bdcb-114">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="9bdcb-115">Пример профиля WPA-Enterprise с TLS</span><span class="sxs-lookup"><span data-stu-id="9bdcb-115">WPA-Enterprise with TLS Profile Sample</span></span>](wpa-enterprise-with-tls-profile-sample.md)
-   [<span data-ttu-id="9bdcb-116">Пример профиля WPA2-Enterprise с PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="9bdcb-116">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa2-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="9bdcb-117">Пример профиля WPA2-Enterprise с TLS</span><span class="sxs-lookup"><span data-stu-id="9bdcb-117">WPA2-Enterprise with TLS Profile Sample</span></span>](wpa2-enterprise-with-tls-profile-sample.md)

<span data-ttu-id="9bdcb-118">Чтобы просмотреть образцы профилей для проводных сетей, содержащих элементы конфигурации 802.1 X, см. следующие примеры профилей:</span><span class="sxs-lookup"><span data-stu-id="9bdcb-118">To view sample profiles for wired networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="9bdcb-119">Пример профиля сертификата компьютера</span><span class="sxs-lookup"><span data-stu-id="9bdcb-119">Machine Certificate Profile Sample</span></span>](machine-certificate-profile-sample.md)
-   [<span data-ttu-id="9bdcb-120">Пример профиля PEAP</span><span class="sxs-lookup"><span data-stu-id="9bdcb-120">PEAP Profile Sample</span></span>](peap-profile-sample.md)
-   [<span data-ttu-id="9bdcb-121">Пример профиля сертификата смарт-карты</span><span class="sxs-lookup"><span data-stu-id="9bdcb-121">Smart Card Certificate Sample Profile</span></span>](smart-card-certificate-profile-sample.md)

 

 



