---
description: Поставщик класса можно смоделировать как принудительный или опрашивающий поставщик, который указывает, как поставщик предполагает взаимодействие с WMI.
ms.assetid: d1852784-8440-4b8a-9cdd-896e51cdee98
ms.tgt_platform: multiple
title: Определение состояния отправки или извлечения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee037b4c81e43080ee119540b05568eb00cdc70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711735"
---
# <a name="determining-push-or-pull-status"></a><span data-ttu-id="b29ef-103">Определение состояния отправки или извлечения</span><span class="sxs-lookup"><span data-stu-id="b29ef-103">Determining Push or Pull Status</span></span>

<span data-ttu-id="b29ef-104">Поставщик класса можно смоделировать как принудительный или опрашивающий поставщик, который указывает, как поставщик предполагает взаимодействие с WMI.</span><span class="sxs-lookup"><span data-stu-id="b29ef-104">You can model a class provider as a push or pull provider, which specifies how a provider expects to interact with WMI.</span></span> <span data-ttu-id="b29ef-105">Поставщики опрашивающей репликации получают запрос от WMI и отвечают на запрос либо путем динамического создания данных, либо их извлечения из локального кэша.</span><span class="sxs-lookup"><span data-stu-id="b29ef-105">Pull providers receive a request from WMI and satisfy the request either by generating the data dynamically or retrieving it from a local cache.</span></span> <span data-ttu-id="b29ef-106">Поставщики опрашивающей репликации также должны реализовывать большое количество интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="b29ef-106">Pull providers also must implement a large number of interfaces.</span></span>

<span data-ttu-id="b29ef-107">Поставщик опроса создает определения классов динамически.</span><span class="sxs-lookup"><span data-stu-id="b29ef-107">A pull provider generates class definitions dynamically.</span></span> <span data-ttu-id="b29ef-108">Как правило, данные, управляемые поставщиком извлечения, часто меняются, что требует, чтобы поставщик либо динамически создавал класс, либо получать класс из локального кэша всякий раз, когда приложение выдает запрос.</span><span class="sxs-lookup"><span data-stu-id="b29ef-108">Typically, the data managed by a pull provider changes frequently, requiring the provider to either generate the class dynamically or retrieve the class from a local cache whenever an application issues a request.</span></span> <span data-ttu-id="b29ef-109">Поставщик опрашивающей репликации должен реализовывать собственные механизмы получения данных, кэширования и уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="b29ef-109">A pull provider must implement its own data retrieval, cache, and event notification mechanisms.</span></span> <span data-ttu-id="b29ef-110">Поскольку большинство поставщиков являются поставщиками извлечения, в документации в этом файле предполагается, что вы создаете поставщик опрашивающей репликации, если явно не указано иное.</span><span class="sxs-lookup"><span data-stu-id="b29ef-110">Because most providers are pull providers, the documentation in this file assumes you are building a pull provider unless explicitly stated otherwise.</span></span>

<span data-ttu-id="b29ef-111">В отличие от этого, WMI использует данные из репозитория WMI для обработки всех запросов приложений для поставщиков push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b29ef-111">In contrast, WMI uses data in the WMI repository to handle all application requests for push providers.</span></span> <span data-ttu-id="b29ef-112">Поставщики push-уведомлений также используют меньше методов интерфейса и поэтому проще реализовать.</span><span class="sxs-lookup"><span data-stu-id="b29ef-112">Push providers also use fewer interface methods, and thus are easier to implement.</span></span> <span data-ttu-id="b29ef-113">Поставщик услуг push-уведомлений использует репозиторий WMI в качестве области хранения для получения сведений об управляемом объекте и обновляет эти сведения только во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="b29ef-113">A push provider uses the WMI repository as a storage area for information on the managed object, and updates that information only during initialization.</span></span> <span data-ttu-id="b29ef-114">Например, поставщик класса WDM, включенный в раздел WMI пакета средств разработки программного обеспечения (SDK) для Microsoft Windows, моделируется как поставщик услуг push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="b29ef-114">For example, the WDM class provider included in the WMI section of the Microsoft Windows Software Development Kit (SDK) is modeled as a push provider.</span></span>

<span data-ttu-id="b29ef-115">Используя репозиторий WMI в качестве области хранения, поставщик услуг push-уведомлений получает следующие преимущества по сравнению с поставщиком по запросу:</span><span class="sxs-lookup"><span data-stu-id="b29ef-115">By using the WMI repository as a storage area, a push provider gains the following benefits over a pull provider:</span></span>

-   <span data-ttu-id="b29ef-116">Поставщику не требуется реализовывать локальный кэш для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="b29ef-116">The provider does not need to implement a local cache to store data.</span></span>
-   <span data-ttu-id="b29ef-117">Поставщику не требуется поддержка извлечения данных; Вместо этого поставщик может использовать инструментарий WMI для предоставления поддержки получения.</span><span class="sxs-lookup"><span data-stu-id="b29ef-117">The provider does not need to support data retrieval; instead, the provider can rely on WMI to provide retrieval support.</span></span>
-   <span data-ttu-id="b29ef-118">Когда приложение запрашивает данные, предоставленные поставщиком, WMI выполняет этот запрос.</span><span class="sxs-lookup"><span data-stu-id="b29ef-118">When an application requests data supplied by the provider, WMI fulfills that request.</span></span>
-   <span data-ttu-id="b29ef-119">Поставщик может также использовать инструментарий WMI для поддержки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="b29ef-119">The provider can also rely on WMI to support event notification.</span></span>

<span data-ttu-id="b29ef-120">Однако, поскольку поставщик push-уведомлений обновляется только во время инициализации, любые изменения в классе могут не отражаться в репозитории WMI в течение некоторого времени.</span><span class="sxs-lookup"><span data-stu-id="b29ef-120">However, because a push provider updates only during initialization, any changes to a class may not be reflected in the WMI repository for some time.</span></span> <span data-ttu-id="b29ef-121">Таким образом, модель поставщика push-уведомлений лучше всего работает с классами, которые изменяют небольшие или другие, полностью статичными.</span><span class="sxs-lookup"><span data-stu-id="b29ef-121">Therefore, the push provider model works best with classes that change little or else are completely static.</span></span>

 

 



