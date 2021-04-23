---
description: Поставщик политик WMI предоставляет расширения для групповой политики с помощью классов, позволяя выполнять уточнения в приложении политики.
ms.assetid: 5d4d4fd2-ecd0-4546-b919-1e75199a403c
ms.tgt_platform: multiple
title: Классы поставщиков политик
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2e2a142cf677c8f0b14b41ceb5119e71bcfebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656551"
---
# <a name="policy-provider-classes"></a><span data-ttu-id="70b69-103">Классы поставщиков политик</span><span class="sxs-lookup"><span data-stu-id="70b69-103">Policy Provider Classes</span></span>

<span data-ttu-id="70b69-104">Поставщик политик WMI предоставляет расширения для групповой политики с помощью классов, позволяя выполнять уточнения в приложении политики.</span><span class="sxs-lookup"><span data-stu-id="70b69-104">The WMI policy provider provides extensions to group policy through classes, permitting refinements in the application of policy.</span></span> <span data-ttu-id="70b69-105">Политика задается с помощью язык запросов WMI (WQL) и размещается в Active Directory для простоты развертывания.</span><span class="sxs-lookup"><span data-stu-id="70b69-105">Policy is set using the WMI Query Language (WQL) and resides in the Active Directory for easy deployment.</span></span>

<span data-ttu-id="70b69-106">В следующей таблице перечислены классы для поставщика политики WMI.</span><span class="sxs-lookup"><span data-stu-id="70b69-106">The following table lists the classes for the WMI policy provider.</span></span>



| <span data-ttu-id="70b69-107">Класс</span><span class="sxs-lookup"><span data-stu-id="70b69-107">Class</span></span>                                               | <span data-ttu-id="70b69-108">Описание</span><span class="sxs-lookup"><span data-stu-id="70b69-108">Description</span></span>                                                       |
|-----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="70b69-109">**\_Поставщики MSFT**</span><span class="sxs-lookup"><span data-stu-id="70b69-109">**MSFT\_Providers**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-providers) | <span data-ttu-id="70b69-110">Предоставляет конфигурацию, относящуюся к экземплярам поставщика.</span><span class="sxs-lookup"><span data-stu-id="70b69-110">Exposes configuration relating to provider instances.</span></span>             |
| [<span data-ttu-id="70b69-111">**\_Правило MSFT**</span><span class="sxs-lookup"><span data-stu-id="70b69-111">**MSFT\_Rule**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-rule)                | <span data-ttu-id="70b69-112">Определяет одно правило в области управления (SOM).</span><span class="sxs-lookup"><span data-stu-id="70b69-112">Defines a single rule within a Scope of Management (SOM).</span></span>         |
| [<span data-ttu-id="70b69-113">**MSFT \_ сомфилтер**</span><span class="sxs-lookup"><span data-stu-id="70b69-113">**MSFT\_SomFilter**</span></span>](/previous-versions/windows/desktop/policmanprov/msft-somfilter)      | <span data-ttu-id="70b69-114">Предоставляет список правил, которые оцениваются на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="70b69-114">Provides a list of rules which are evaluated on a target machine.</span></span> |



 

 

 
