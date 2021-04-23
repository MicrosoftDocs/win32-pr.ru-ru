---
description: Поскольку Инструментарий WMI загружает высокопроизводительный поставщик в интерфейс WMI или клиентское приложение, необходимо спроектировать высокопроизводительный поставщик в качестве внутрипроцессного сервера.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Реализация интерфейса High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693328"
---
# <a name="implementing-the-high-performance-interface"></a><span data-ttu-id="fa456-103">Реализация интерфейса High-Performance</span><span class="sxs-lookup"><span data-stu-id="fa456-103">Implementing the High-Performance Interface</span></span>

<span data-ttu-id="fa456-104">Поскольку Инструментарий WMI загружает высокопроизводительный поставщик в интерфейс WMI или клиентское приложение, необходимо спроектировать высокопроизводительный поставщик в качестве внутрипроцессного сервера.</span><span class="sxs-lookup"><span data-stu-id="fa456-104">Because WMI loads a high-performance provider in-process to either WMI or a client application, you must design your high-performance provider as an in-process server.</span></span> <span data-ttu-id="fa456-105">Кроме того, необходимо реализовать высокопроизводительные методы поставщика в интерфейсах [**ивбемхиперфпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) и [**ивбемрефрешер**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .</span><span class="sxs-lookup"><span data-stu-id="fa456-105">In addition, you must implement the high-performance provider methods in the [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) and [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interfaces.</span></span>

<span data-ttu-id="fa456-106">В качестве внутрипроцессного сервера следует реализовать высокопроизводительный поставщик.</span><span class="sxs-lookup"><span data-stu-id="fa456-106">You should implement a high-performance provider as an in-process server.</span></span> <span data-ttu-id="fa456-107">При реализации безопасности внутрипроцессного сервера следует помнить о том, как поставщик определяет свое расположение.</span><span class="sxs-lookup"><span data-stu-id="fa456-107">One feature you should be aware of when implementing the security of an in-process server is how the provider identifies its own location.</span></span> <span data-ttu-id="fa456-108">При загрузке внутрипроцессного в WMI WMI создает экземпляр поставщика с помощью идентификатора CLSID.</span><span class="sxs-lookup"><span data-stu-id="fa456-108">When loaded in-process to WMI, WMI instantiates the provider using a CLSID.</span></span> <span data-ttu-id="fa456-109">При загрузке в процесс клиентского приложения клиентское приложение создает экземпляр поставщика с помощью свойства **клиентлоадаблеклсид** .</span><span class="sxs-lookup"><span data-stu-id="fa456-109">When loaded in process to a client application, the client application instantiates the provider with the **ClientLoadableCLSID** property.</span></span> <span data-ttu-id="fa456-110">Присваивая различным значениям идентификаторы CLSID и **клиентлоадаблеклсид**, вы разрешаете поставщику определить, загружен ли он внутри процесса в WMI или в клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="fa456-110">By giving different values to a CLSID and **ClientLoadableCLSID**, you allow the provider to determine if it is loaded in-process to WMI or to a client application.</span></span> <span data-ttu-id="fa456-111">Если он находится в процессе WMI, поставщик должен выполнить все необходимое олицетворение клиента с помощью **клиентлоадаблеклсид**.</span><span class="sxs-lookup"><span data-stu-id="fa456-111">If located in a WMI process, the provider should do any necessary client impersonation by using **ClientLoadableCLSID**.</span></span> <span data-ttu-id="fa456-112">При размещении в клиентском процессе поставщик наследует маркер доступа потока, для которого он вызывается.</span><span class="sxs-lookup"><span data-stu-id="fa456-112">If located in a client process, the provider inherits the access token of the thread it is called on.</span></span> <span data-ttu-id="fa456-113">Дополнительные сведения о реализации внутрипроцессного сервера см. в [разделе com статьи](https://msdn.microsoft.com/library/aa139695.aspx) MSDN.</span><span class="sxs-lookup"><span data-stu-id="fa456-113">For more information about implementing an in-process server, see the [COM section](https://msdn.microsoft.com/library/aa139695.aspx) of MSDN.</span></span>

<span data-ttu-id="fa456-114">Как внутрипроцессный сервер, высокопроизводительный поставщик использует объект обновления, чтобы обеспечить актуальность данных для удаленного клиента.</span><span class="sxs-lookup"><span data-stu-id="fa456-114">As an in-process server, a high-performance provider uses a refresher object to keep data current for the remote client.</span></span> <span data-ttu-id="fa456-115">В следующей таблице перечислены методы, которые необходимо реализовать для высокопроизводительного поставщика.</span><span class="sxs-lookup"><span data-stu-id="fa456-115">The following table lists methods that you must implement for a high-performance provider.</span></span>



| <span data-ttu-id="fa456-116">Метод</span><span class="sxs-lookup"><span data-stu-id="fa456-116">Method</span></span>                                                                                              | <span data-ttu-id="fa456-117">Функция</span><span class="sxs-lookup"><span data-stu-id="fa456-117">Feature</span></span>                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="fa456-118">**Ивбемхиперфпровидер:: Куеринстанцес**</span><span class="sxs-lookup"><span data-stu-id="fa456-118">**IWbemHiPerfProvider::QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | <span data-ttu-id="fa456-119">Запросы</span><span class="sxs-lookup"><span data-stu-id="fa456-119">Queries</span></span>                                           |
| [<span data-ttu-id="fa456-120">**Ивбемхиперфпровидер:: GetObject**</span><span class="sxs-lookup"><span data-stu-id="fa456-120">**IWbemHiPerfProvider::GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | <span data-ttu-id="fa456-121">Получение объектов</span><span class="sxs-lookup"><span data-stu-id="fa456-121">Object retrieval</span></span>                                  |
| [<span data-ttu-id="fa456-122">**Ивбемхиперфпровидер:: Креатерефрешер**</span><span class="sxs-lookup"><span data-stu-id="fa456-122">**IWbemHiPerfProvider::CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | <span data-ttu-id="fa456-123">Создает Обновитель</span><span class="sxs-lookup"><span data-stu-id="fa456-123">Creates a refresher</span></span>                               |
| [<span data-ttu-id="fa456-124">**Ивбемхиперфпровидер:: Креатерефрешаблеобжект**</span><span class="sxs-lookup"><span data-stu-id="fa456-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | <span data-ttu-id="fa456-125">Создает обновляемый объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="fa456-125">Creates a refreshable instance object</span></span>             |
| [<span data-ttu-id="fa456-126">**Ивбемхиперфпровидер:: Креатерефрешаблинум**</span><span class="sxs-lookup"><span data-stu-id="fa456-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | <span data-ttu-id="fa456-127">Создает обновляемый перечислитель</span><span class="sxs-lookup"><span data-stu-id="fa456-127">Creates a refreshable enumerator</span></span>                  |
| [<span data-ttu-id="fa456-128">**Ивбемхиперфпровидер:: Стопрефрешинг**</span><span class="sxs-lookup"><span data-stu-id="fa456-128">**IWbemHiPerfProvider::StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | <span data-ttu-id="fa456-129">Останавливает обновление объекта перечислителя или экземпляра</span><span class="sxs-lookup"><span data-stu-id="fa456-129">Stops refreshing an enumerator or instance object</span></span> |
| [<span data-ttu-id="fa456-130">**Ивбемрефрешер:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="fa456-130">**IWbemRefresher::Refresh**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | <span data-ttu-id="fa456-131">Создает Обновитель</span><span class="sxs-lookup"><span data-stu-id="fa456-131">Creates a refresher</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="fa456-132">См. также</span><span class="sxs-lookup"><span data-stu-id="fa456-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa456-133">Создание поставщика экземпляров в поставщике High-Performance</span><span class="sxs-lookup"><span data-stu-id="fa456-133">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



