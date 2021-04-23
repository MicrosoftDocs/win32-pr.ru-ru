---
description: Интерфейс Иупдатесеарчер определяет следующие свойства.
ms.assetid: 65a39383-f326-4735-b2af-6df7a77ffba6
title: Свойства Иупдатесеарчер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777c2489afe10f73c41badfb346053aefad7022
ms.sourcegitcommit: aab10824ee4883c70e1afba428b679a17915a5aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2021
ms.locfileid: "104354015"
---
# <a name="iupdatesearcher-properties"></a><span data-ttu-id="8d61d-103">Свойства Иупдатесеарчер</span><span class="sxs-lookup"><span data-stu-id="8d61d-103">IUpdateSearcher Properties</span></span>

<span data-ttu-id="8d61d-104">Интерфейс [**иупдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8d61d-104">The [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) interface defines the following properties.</span></span>



| <span data-ttu-id="8d61d-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="8d61d-105">Property</span></span>                                                                                           | <span data-ttu-id="8d61d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8d61d-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d61d-107">**канаутоматикаллюпградесервице**</span><span class="sxs-lookup"><span data-stu-id="8d61d-107">**CanAutomaticallyUpgradeService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_canautomaticallyupgradeservice)            | <span data-ttu-id="8d61d-108">Возвращает и задает логическое значение, указывающее, приводит ли будущие вызовы методов [**бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) и [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) к автоматическому обновлению до центр обновления Windows Agent (WUA).</span><span class="sxs-lookup"><span data-stu-id="8d61d-108">Gets and sets a Boolean value that indicates whether future calls to the [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) and [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search) methods result in an automatic upgrade to Windows Update Agent (WUA).</span></span> |
| [<span data-ttu-id="8d61d-109">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="8d61d-109">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_clientapplicationid)                                  | <span data-ttu-id="8d61d-110">Определяет текущее клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="8d61d-110">Identifies the current client application.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="8d61d-111">**инклудепотентиаллисуперседедупдатес**</span><span class="sxs-lookup"><span data-stu-id="8d61d-111">**IncludePotentiallySupersededUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_includepotentiallysupersededupdates) | <span data-ttu-id="8d61d-112">Возвращает и задает логическое значение, указывающее, содержат ли результаты поиска обновления, заменяемые другими обновлениями в результатах поиска.</span><span class="sxs-lookup"><span data-stu-id="8d61d-112">Gets and sets a Boolean value that indicates whether the search results include updates that are superseded by other updates in the search results.</span></span>                                                                                          |
| [<span data-ttu-id="8d61d-113">**Миграция по сети**</span><span class="sxs-lookup"><span data-stu-id="8d61d-113">**Online**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_online)                                                            | <span data-ttu-id="8d61d-114">Возвращает и задает логическое значение, указывающее, переходит ли [**упдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) в оперативный режим для поиска обновлений.</span><span class="sxs-lookup"><span data-stu-id="8d61d-114">Gets and sets a Boolean value that indicates whether the [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) goes online to search for updates.</span></span>                                                                                                        |
| [<span data-ttu-id="8d61d-115">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="8d61d-115">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serviceid)                                                      | <span data-ttu-id="8d61d-116">Возвращает и задает сайт для поиска, если сайт для поиска не является Центр обновления Windows сайтом.</span><span class="sxs-lookup"><span data-stu-id="8d61d-116">Gets and sets a site to search when the site to search is not a Windows Update site.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="8d61d-117">**ServerSelection**</span><span class="sxs-lookup"><span data-stu-id="8d61d-117">**ServerSelection**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-get_serverselection)                                          | <span data-ttu-id="8d61d-118">Возвращает и задает значение [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) , указывающее сервер для поиска обновлений.</span><span class="sxs-lookup"><span data-stu-id="8d61d-118">Gets and sets a [**ServerSelection**](/openspecs/windows_protocols/ms-uamg/07e2bfa4-6795-4189-b007-cc50b476181a) value that indicates the server to search for updates.</span></span>                                                                                                                            |




 

 

 



