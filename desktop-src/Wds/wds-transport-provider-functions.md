---
title: Функции поставщика транспорта WDS
description: Пользовательские поставщики содержимого могут предоставлять следующие функции обратного вызова серверу многоадресной рассылки.
ms.assetid: 30ec1969-4e90-458e-8a9f-39a7bbf4cd79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e67747d8ef5738a4bf3bee8ff2ffb3b35cf43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779391"
---
# <a name="wds-transport-provider-functions"></a><span data-ttu-id="a2970-103">Функции поставщика транспорта WDS</span><span class="sxs-lookup"><span data-stu-id="a2970-103">WDS Transport Provider Functions</span></span>

<span data-ttu-id="a2970-104">Пользовательские поставщики содержимого могут предоставлять следующие функции обратного вызова серверу многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="a2970-104">User-defined content providers can expose the following callback functions to the multicast server.</span></span>



| <span data-ttu-id="a2970-105">Функция</span><span class="sxs-lookup"><span data-stu-id="a2970-105">Function</span></span>                                                                               | <span data-ttu-id="a2970-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a2970-106">Description</span></span>                                                                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2970-107">*вдстранспортпровидерклосеконтент*</span><span class="sxs-lookup"><span data-stu-id="a2970-107">*WdsTransportProviderCloseContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderclosecontent)             | <span data-ttu-id="a2970-108">Закрывает поток содержимого, указанный в маркере.</span><span class="sxs-lookup"><span data-stu-id="a2970-108">Closes a content stream specified by a handle.</span></span>                                                                          |
| [<span data-ttu-id="a2970-109">*вдстранспортпровидерклосеинстанце*</span><span class="sxs-lookup"><span data-stu-id="a2970-109">*WdsTransportProviderCloseInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercloseinstance)           | <span data-ttu-id="a2970-110">Закрывает экземпляр поставщика содержимого, указанный в маркере.</span><span class="sxs-lookup"><span data-stu-id="a2970-110">Closes an instance of a content provider specified by a handle.</span></span>                                                         |
| [<span data-ttu-id="a2970-111">*вдстранспортпровидеркомпареконтент*</span><span class="sxs-lookup"><span data-stu-id="a2970-111">*WdsTransportProviderCompareContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercomparecontent)         | <span data-ttu-id="a2970-112">Сравнивает указанное имя и экземпляр содержимого с открытым потоком содержимого, чтобы определить, совпадают ли они.</span><span class="sxs-lookup"><span data-stu-id="a2970-112">Compares a specified content name and instance to an open content stream to determine if they are the same.</span></span>             |
| [<span data-ttu-id="a2970-113">*вдстранспортпровидеркреатеинстанце*</span><span class="sxs-lookup"><span data-stu-id="a2970-113">*WdsTransportProviderCreateInstance*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidercreateinstance)         | <span data-ttu-id="a2970-114">Открывает новый экземпляр поставщика содержимого.</span><span class="sxs-lookup"><span data-stu-id="a2970-114">Opens a new instance of a content provider.</span></span>                                                                             |
| [<span data-ttu-id="a2970-115">*вдстранспортпровидердумпстате*</span><span class="sxs-lookup"><span data-stu-id="a2970-115">*WdsTransportProviderDumpState*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderdumpstate)                   | <span data-ttu-id="a2970-116">Указывает поставщику транспорта распечатать сводку состояния и другие важные сведения в журнале трассировки.</span><span class="sxs-lookup"><span data-stu-id="a2970-116">Instructs the transport provider to print a summary of its state and any other relevant information to the tracing log.</span></span> |
| [<span data-ttu-id="a2970-117">*вдстранспортпровидержетконтентметадата*</span><span class="sxs-lookup"><span data-stu-id="a2970-117">*WdsTransportProviderGetContentMetadata*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentmetadata) | <span data-ttu-id="a2970-118">Извлекает метаданные для открытого потока содержимого.</span><span class="sxs-lookup"><span data-stu-id="a2970-118">Retrieves metadata for an open content stream.</span></span>                                                                          |
| [<span data-ttu-id="a2970-119">*вдстранспортпровидержетконтентсизе*</span><span class="sxs-lookup"><span data-stu-id="a2970-119">*WdsTransportProviderGetContentSize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidergetcontentsize)         | <span data-ttu-id="a2970-120">Возвращает размер открытого потока содержимого.</span><span class="sxs-lookup"><span data-stu-id="a2970-120">Retrieves the size of an open content stream.</span></span>                                                                           |
| [<span data-ttu-id="a2970-121">*вдстранспортпровидеринитиализе*</span><span class="sxs-lookup"><span data-stu-id="a2970-121">*WdsTransportProviderInitialize*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize)                 | <span data-ttu-id="a2970-122">Инициализирует поставщик содержимого.</span><span class="sxs-lookup"><span data-stu-id="a2970-122">Initializes a content provider.</span></span>                                                                                         |
| [<span data-ttu-id="a2970-123">*вдстранспортпровидеропенконтент*</span><span class="sxs-lookup"><span data-stu-id="a2970-123">*WdsTransportProviderOpenContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideropencontent)               | <span data-ttu-id="a2970-124">Открывает новое статическое представление потока содержимого.</span><span class="sxs-lookup"><span data-stu-id="a2970-124">Opens a new static view of a content stream.</span></span>                                                                            |
| [<span data-ttu-id="a2970-125">*вдстранспортпровидерреадконтент*</span><span class="sxs-lookup"><span data-stu-id="a2970-125">*WdsTransportProviderReadContent*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderreadcontent)               | <span data-ttu-id="a2970-126">Считывает содержимое из открытого потока содержимого.</span><span class="sxs-lookup"><span data-stu-id="a2970-126">Reads content from an open content stream.</span></span>                                                                              |
| [<span data-ttu-id="a2970-127">*вдстранспортпровидеррефрешсеттингс*</span><span class="sxs-lookup"><span data-stu-id="a2970-127">*WdsTransportProviderRefreshSettings*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderrefreshsettings)       | <span data-ttu-id="a2970-128">Предписывает поставщику транспорта пересчитать все необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="a2970-128">Instructs the transport provider to reread any relevant settings.</span></span>                                                       |
| [<span data-ttu-id="a2970-129">*вдстранспортпровидершутдовн*</span><span class="sxs-lookup"><span data-stu-id="a2970-129">*WdsTransportProviderShutdown*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovidershutdown)                     | <span data-ttu-id="a2970-130">Шутсдовн поставщика содержимого.</span><span class="sxs-lookup"><span data-stu-id="a2970-130">Shutsdown the content provider.</span></span>                                                                                         |
| [<span data-ttu-id="a2970-131">*вдстранспортпровидерусеракцессчекк*</span><span class="sxs-lookup"><span data-stu-id="a2970-131">*WdsTransportProviderUserAccessCheck*</span></span>](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportprovideruseraccesscheck)       | <span data-ttu-id="a2970-132">Указывает доступ к потоку содержимого на основе маркера пользователя.</span><span class="sxs-lookup"><span data-stu-id="a2970-132">Specifies access to a content stream based on a user's token.</span></span>                                                           |



 

 

 




