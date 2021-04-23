---
description: Интерфейс Иупдатесервице определяет следующие свойства.
ms.assetid: 33bc28e8-0b83-4d58-a03e-ccf2a97887e6
title: Свойства Иупдатесервице
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ff3cf92c89a5ba02b7d95f1a1c99f33de3202d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497601"
---
# <a name="iupdateservice-properties"></a><span data-ttu-id="3ca87-103">Свойства Иупдатесервице</span><span class="sxs-lookup"><span data-stu-id="3ca87-103">IUpdateService Properties</span></span>

<span data-ttu-id="3ca87-104">Интерфейс [**иупдатесервице**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3ca87-104">The [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface defines the following properties.</span></span>



| <span data-ttu-id="3ca87-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="3ca87-105">Property</span></span>                                                              | <span data-ttu-id="3ca87-106">Описание</span><span class="sxs-lookup"><span data-stu-id="3ca87-106">Description</span></span>                                                                                     |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca87-107">**канрегистервисау**</span><span class="sxs-lookup"><span data-stu-id="3ca87-107">**CanRegisterWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_canregisterwithau)         | <span data-ttu-id="3ca87-108">Возвращает логическое значение, указывающее, может ли служба зарегистрироваться в автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="3ca87-108">Gets a Boolean value that indicates whether the service can register with Automatic Updates.</span></span>    |
| [<span data-ttu-id="3ca87-109">**контентвалидатионцерт**</span><span class="sxs-lookup"><span data-stu-id="3ca87-109">**ContentValidationCert**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_contentvalidationcert) | <span data-ttu-id="3ca87-110">Возвращает хэш SHA-1 сертификата, который используется для подписи содержимого службы.</span><span class="sxs-lookup"><span data-stu-id="3ca87-110">Gets an SHA-1 hash of the certificate that is used to sign the contents of the service.</span></span>         |
| [<span data-ttu-id="3ca87-111">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="3ca87-111">**ExpirationDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_expirationdate)               | <span data-ttu-id="3ca87-112">Возвращает дату истечения срока действия CAB-файла авторизации.</span><span class="sxs-lookup"><span data-stu-id="3ca87-112">Gets the date on which the authorization cabinet file expires.</span></span>                                  |
| [<span data-ttu-id="3ca87-113">**IsManaged**</span><span class="sxs-lookup"><span data-stu-id="3ca87-113">**IsManaged**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_ismanaged)                         | <span data-ttu-id="3ca87-114">Возвращает логическое значение, указывающее, является ли служба управляемой.</span><span class="sxs-lookup"><span data-stu-id="3ca87-114">Gets a Boolean value that indicates whether a service is a managed service.</span></span>                     |
| [<span data-ttu-id="3ca87-115">**исрегистередвисау**</span><span class="sxs-lookup"><span data-stu-id="3ca87-115">**IsRegisteredWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isregisteredwithau)       | <span data-ttu-id="3ca87-116">Возвращает логическое значение, указывающее, зарегистрирована ли служба с автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="3ca87-116">Gets a Boolean value that indicates whether a service is registered with Automatic Updates.</span></span>     |
| [<span data-ttu-id="3ca87-117">**иссканпаккажесервице**</span><span class="sxs-lookup"><span data-stu-id="3ca87-117">**IsScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_isscanpackageservice)   | <span data-ttu-id="3ca87-118">Возвращает логическое значение, указывающее, основана ли служба на пакете сканирования.</span><span class="sxs-lookup"><span data-stu-id="3ca87-118">Gets a Boolean value that indicates whether a service is based on a scan package.</span></span>               |
| [<span data-ttu-id="3ca87-119">**иссуедате**</span><span class="sxs-lookup"><span data-stu-id="3ca87-119">**IssueDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_issuedate)                         | <span data-ttu-id="3ca87-120">Возвращает дату, когда был выдан CAB-файл авторизации.</span><span class="sxs-lookup"><span data-stu-id="3ca87-120">Gets the date on which the authorization cabinet file was issued.</span></span>                               |
| [<span data-ttu-id="3ca87-121">**Имя**</span><span class="sxs-lookup"><span data-stu-id="3ca87-121">**Name**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_name)                                   | <span data-ttu-id="3ca87-122">Возвращает имя службы.</span><span class="sxs-lookup"><span data-stu-id="3ca87-122">Gets the name of the service.</span></span>                                                                   |
| [<span data-ttu-id="3ca87-123">**офферсвиндовсупдатес**</span><span class="sxs-lookup"><span data-stu-id="3ca87-123">**OffersWindowsUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_offerswindowsupdates)   | <span data-ttu-id="3ca87-124">Возвращает логическое значение, указывающее, предлагает ли текущая служба обновления из обновлений Windows.</span><span class="sxs-lookup"><span data-stu-id="3ca87-124">Gets a Boolean value indicates whether the current service offers updates from Windows Updates.</span></span> |
| [<span data-ttu-id="3ca87-125">**редиректурлс**</span><span class="sxs-lookup"><span data-stu-id="3ca87-125">**RedirectUrls**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_redirecturls)                   | <span data-ttu-id="3ca87-126">Возвращает URL-адрес ящика перенаправителя.</span><span class="sxs-lookup"><span data-stu-id="3ca87-126">Gets the URL for the redirector cabinet file.</span></span>                                                   |
| [<span data-ttu-id="3ca87-127">**ServiceID**</span><span class="sxs-lookup"><span data-stu-id="3ca87-127">**ServiceID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceid)                         | <span data-ttu-id="3ca87-128">Возвращает идентификатор службы.</span><span class="sxs-lookup"><span data-stu-id="3ca87-128">Gets the identifier for a service.</span></span>                                                              |
| [<span data-ttu-id="3ca87-129">**ServiceUrl**</span><span class="sxs-lookup"><span data-stu-id="3ca87-129">**ServiceUrl**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_serviceurl)                       | <span data-ttu-id="3ca87-130">Возвращает URL-адрес службы.</span><span class="sxs-lookup"><span data-stu-id="3ca87-130">Gets the URL for the service.</span></span>                                                                   |
| [<span data-ttu-id="3ca87-131">**сетуппрефикс**</span><span class="sxs-lookup"><span data-stu-id="3ca87-131">**SetupPrefix**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservice-get_setupprefix)                     | <span data-ttu-id="3ca87-132">Возвращает префикс для файлов установки.</span><span class="sxs-lookup"><span data-stu-id="3ca87-132">Gets the prefix for the setup files.</span></span>                                                            |



 

 

 



