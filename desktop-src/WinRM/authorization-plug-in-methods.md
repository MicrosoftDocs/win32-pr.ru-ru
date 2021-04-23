---
title: Методы подключаемого модуля авторизации
description: Все точки входа подключаемых модулей авторизации имеют механизм обратного вызова для сообщения об успешном или неуспешном вызове. Некоторые механизмы обратного вызова вызываются несколько раз до тех пор, пока не будут переданы все результаты.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700567"
---
# <a name="authorization-plug-in-methods"></a><span data-ttu-id="08005-104">Методы подключаемого модуля авторизации</span><span class="sxs-lookup"><span data-stu-id="08005-104">Authorization Plug-in Methods</span></span>

<span data-ttu-id="08005-105">Все точки входа подключаемых модулей авторизации имеют механизм обратного вызова для сообщения об успешном или неуспешном вызове.</span><span class="sxs-lookup"><span data-stu-id="08005-105">All authorization plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="08005-106">Некоторые механизмы обратного вызова вызываются несколько раз до тех пор, пока не будут переданы все результаты.</span><span class="sxs-lookup"><span data-stu-id="08005-106">Some callback mechanisms are called multiple times until all of the results are reported.</span></span>

<span data-ttu-id="08005-107">В следующей таблице приведены общие сведения о методах обратного вызова авторизации.</span><span class="sxs-lookup"><span data-stu-id="08005-107">The following table provides an overview of the authorization callback methods.</span></span>



| <span data-ttu-id="08005-108">Метод</span><span class="sxs-lookup"><span data-stu-id="08005-108">Method</span></span>                                                                           | <span data-ttu-id="08005-109">Описание</span><span class="sxs-lookup"><span data-stu-id="08005-109">Description</span></span>                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="08005-110">**всманплугинаусзоператионкомплете**</span><span class="sxs-lookup"><span data-stu-id="08005-110">**WSManPluginAuthzOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | <span data-ttu-id="08005-111">Сообщает об успешной или неудачной операции пользователя.</span><span class="sxs-lookup"><span data-stu-id="08005-111">Reports either a successful or failed user operation.</span></span>                |
| [<span data-ttu-id="08005-112">**всманплугинаусзкуерикуотакомплете**</span><span class="sxs-lookup"><span data-stu-id="08005-112">**WSManPluginAuthzQueryQuotaComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | <span data-ttu-id="08005-113">Сообщает сведения о квоте, относящиеся к указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="08005-113">Reports quota details that are relevant for the specified user.</span></span>      |
| [<span data-ttu-id="08005-114">**всманплугинаусзусеркомплете**</span><span class="sxs-lookup"><span data-stu-id="08005-114">**WSManPluginAuthzUserComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | <span data-ttu-id="08005-115">Сообщает об успешной или неудачной авторизации подключения пользователя.</span><span class="sxs-lookup"><span data-stu-id="08005-115">Reports either a successful or failed user connection authorization.</span></span> |



 

 

 




