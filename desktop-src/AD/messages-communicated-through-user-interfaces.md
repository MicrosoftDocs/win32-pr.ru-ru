---
title: Сообщения, отправляемые через пользовательские интерфейсы
description: В этом разделе перечислены сообщения, которые служба каталогов может отправить из пользовательского интерфейса.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Сообщения, отправляемые через пользовательские интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab0d01717129db284f05b2361b2a067d611a33e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067368"
---
# <a name="messages-communicated-through-user-interfaces"></a><span data-ttu-id="0cc5f-104">Сообщения, отправляемые через пользовательские интерфейсы</span><span class="sxs-lookup"><span data-stu-id="0cc5f-104">Messages Communicated through User Interfaces</span></span>

<span data-ttu-id="0cc5f-105">В этом разделе перечислены сообщения, которые служба каталогов может отправить из пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0cc5f-105">This topic lists messages that a directory service can send from a user interface.</span></span>

## <a name="common-query-page-messages"></a><span data-ttu-id="0cc5f-106">Общие сообщения страницы запросов</span><span class="sxs-lookup"><span data-stu-id="0cc5f-106">Common Query Page Messages</span></span>

<span data-ttu-id="0cc5f-107">Следующие сообщения отправляются на страницу расширения формы запроса службы каталогов в функции обратного вызова [**ккпажепрок**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :</span><span class="sxs-lookup"><span data-stu-id="0cc5f-107">The following messages are sent to a directory service query form extension page in the [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) callback function:</span></span>

-   [<span data-ttu-id="0cc5f-108">**ККПМ \_ клеарформ**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-108">**CQPM\_CLEARFORM**</span></span>](cqpm-clearform.md)
-   [<span data-ttu-id="0cc5f-109">**\_включить ККПМ**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-109">**CQPM\_ENABLE**</span></span>](cqpm-enable.md)
-   [<span data-ttu-id="0cc5f-110">**ККПМ \_ Parameters**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-110">**CQPM\_GETPARAMETERS**</span></span>](cqpm-getparameters.md)
-   [<span data-ttu-id="0cc5f-111">**ККПМ \_ хандлерспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-111">**CQPM\_HANDLERSPECIFIC**</span></span>](cqpm-handlerspecific.md)
-   [<span data-ttu-id="0cc5f-112">**\_Справка ККПМ**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-112">**CQPM\_HELP**</span></span>](cqpm-help.md)
-   [<span data-ttu-id="0cc5f-113">**\_Инициализация ККПМ**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-113">**CQPM\_INITIALIZE**</span></span>](cqpm-initialize.md)
-   [<span data-ttu-id="0cc5f-114">**ККПМ \_ сохранить**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-114">**CQPM\_PERSIST**</span></span>](cqpm-persist.md)
-   [<span data-ttu-id="0cc5f-115">**\_выпуск ККПМ**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-115">**CQPM\_RELEASE**</span></span>](cqpm-release.md)
-   [<span data-ttu-id="0cc5f-116">**ККПМ \_ сетдефаултпараметерс**</span><span class="sxs-lookup"><span data-stu-id="0cc5f-116">**CQPM\_SETDEFAULTPARAMETERS**</span></span>](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a><span data-ttu-id="0cc5f-117">Прочие сообщения</span><span class="sxs-lookup"><span data-stu-id="0cc5f-117">Miscellaneous Messages</span></span>

<span data-ttu-id="0cc5f-118">В следующей таблице перечислены сообщения, которые может отправить Служба каталогов.</span><span class="sxs-lookup"><span data-stu-id="0cc5f-118">The following table lists messages that a directory service can send.</span></span>



| <span data-ttu-id="0cc5f-119">Сообщение</span><span class="sxs-lookup"><span data-stu-id="0cc5f-119">Message</span></span>                  | <span data-ttu-id="0cc5f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0cc5f-120">Value</span></span>                     | <span data-ttu-id="0cc5f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="0cc5f-121">Description</span></span>                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc5f-122">\_сообщение дспроп аттрчанжед \_</span><span class="sxs-lookup"><span data-stu-id="0cc5f-122">DSPROP\_ATTRCHANGED\_MSG</span></span> | <span data-ttu-id="0cc5f-123">"Дспропаттрчанжед"</span><span class="sxs-lookup"><span data-stu-id="0cc5f-123">"DsPropAttrChanged"</span></span>       | <span data-ttu-id="0cc5f-124">Сообщение, отправленное для синхронизации страниц свойств и средств администрирования службы каталогов, объявленных в DSClient. h.</span><span class="sxs-lookup"><span data-stu-id="0cc5f-124">A message sent for synchronizing property pages and the directory service administration tools, declared in Dsclient.h.</span></span>                                                                                                                       |
| <span data-ttu-id="0cc5f-125">ДСКПМ \_ жеткласслист</span><span class="sxs-lookup"><span data-stu-id="0cc5f-125">DSQPM\_GETCLASSLIST</span></span>      | <span data-ttu-id="0cc5f-126">ККПМ \_ хандлерспеЦифик + 0</span><span class="sxs-lookup"><span data-stu-id="0cc5f-126">CQPM\_HANDLERSPECIFIC+0</span></span>   | <span data-ttu-id="0cc5f-127">Сообщение страницы, отправленное на страницы формы для получения списка классов для запроса, которое используется селектором полей и свойством для построения его списка классов вывода.</span><span class="sxs-lookup"><span data-stu-id="0cc5f-127">A page message sent to the form pages for retrieving a list of classes for query, used by the field selector and property well to build its list of display classes.</span></span> <span data-ttu-id="0cc5f-128">wParam = Flags и lParam = ЛПЛПДСКУЕРИКЛАССЛИСТ, объявленные в dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="0cc5f-128">wParam = flags and lParam = LPLPDSQUERYCLASSLIST, declared in Dsquery.h.</span></span> |
| <span data-ttu-id="0cc5f-129">ДСКПМ \_ хелптопикс</span><span class="sxs-lookup"><span data-stu-id="0cc5f-129">DSQPM\_HELPTOPICS</span></span>        | <span data-ttu-id="0cc5f-130">(ККПМ \_ ХАНДЛЕРСПЕЦИФИК + 1)</span><span class="sxs-lookup"><span data-stu-id="0cc5f-130">(CQPM\_HANDLERSPECIFIC+1)</span></span> | <span data-ttu-id="0cc5f-131">Сообщение страницы, отправленное на страницы формы для обработки запроса "разделы справки".</span><span class="sxs-lookup"><span data-stu-id="0cc5f-131">A page message sent to the form pages for handling the "Help Topics" request.</span></span> <span data-ttu-id="0cc5f-132">wParam = 0, lParam = Хвндпарент, объявленный в dsquery. h.</span><span class="sxs-lookup"><span data-stu-id="0cc5f-132">wParam = 0, lParam = hWndParent, declared in Dsquery.h.</span></span>                                                                                                         |



 

 

 




