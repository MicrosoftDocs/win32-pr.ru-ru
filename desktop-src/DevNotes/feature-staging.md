---
description: Промежуточное хранение компонентов
ms.assetid: 9F16C420-BF94-4C92-BC7E-15DD516E5107
title: Промежуточное хранение компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adcb8f20a1bba411effa9a050a4fd429e3b752a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990474"
---
# <a name="feature-staging"></a><span data-ttu-id="806a4-103">Промежуточное хранение компонентов</span><span class="sxs-lookup"><span data-stu-id="806a4-103">Feature Staging</span></span>

<span data-ttu-id="806a4-104">Эти API-интерфейсы предназначены только для использования в инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="806a4-104">These APIs are intended for infrastructure use only.</span></span> <span data-ttu-id="806a4-105">Не используйте эти API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="806a4-105">Do not use these APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="806a4-106">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="806a4-106">In this section</span></span>

-   [<span data-ttu-id="806a4-107">**\_состояние включения \_ компонента**</span><span class="sxs-lookup"><span data-stu-id="806a4-107">**FEATURE\_ENABLED\_STATE**</span></span>](/windows/desktop/api/featurestagingapi/ne-featurestagingapi-feature_enabled_state)
-   [<span data-ttu-id="806a4-108">**\_ошибка функции**</span><span class="sxs-lookup"><span data-stu-id="806a4-108">**FEATURE\_ERROR**</span></span>](/windows/desktop/api/featurestagingapi/ns-featurestagingapi-feature_error)
-   [<span data-ttu-id="806a4-109">**\_время изменения \_ функции**</span><span class="sxs-lookup"><span data-stu-id="806a4-109">**FEATURE\_CHANGE\_TIME**</span></span>](/windows/desktop/api/featurestagingapi/ne-featurestagingapi-feature_change_time)
-   [<span data-ttu-id="806a4-110">**жетфеатуринабледстате**</span><span class="sxs-lookup"><span data-stu-id="806a4-110">**GetFeatureEnabledState**</span></span>](/windows/desktop/api/featurestagingapi/nf-featurestagingapi-getfeatureenabledstate)
-   [<span data-ttu-id="806a4-111">**жетфеатуревариант**</span><span class="sxs-lookup"><span data-stu-id="806a4-111">**GetFeatureVariant**</span></span>](/windows/desktop/api/featurestagingapi/nf-featurestagingapi-getfeaturevariant)
-   [<span data-ttu-id="806a4-112">**рекордфеатуриррор**</span><span class="sxs-lookup"><span data-stu-id="806a4-112">**RecordFeatureError**</span></span>](/windows/desktop/api/featurestagingapi/nf-featurestagingapi-recordfeatureerror)
-   [<span data-ttu-id="806a4-113">**рекордфеатуреусаже**</span><span class="sxs-lookup"><span data-stu-id="806a4-113">**RecordFeatureUsage**</span></span>](/windows/desktop/api/featurestagingapi/nf-featurestagingapi-recordfeatureusage)
-   [<span data-ttu-id="806a4-114">**субскрибефеатурестатечанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="806a4-114">**SubscribeFeatureStateChangeNotification**</span></span>](/windows/desktop/api/featurestagingapi/nf-featurestagingapi-subscribefeaturestatechangenotification)
-   [<span data-ttu-id="806a4-115">**унсубскрибефеатурестатечанженотификатион**</span><span class="sxs-lookup"><span data-stu-id="806a4-115">**UnsubscribeFeatureStateChangeNotification**</span></span>](/windows/desktop/api/featurestagingapi/nf-featurestagingapi-unsubscribefeaturestatechangenotification)

 

 



