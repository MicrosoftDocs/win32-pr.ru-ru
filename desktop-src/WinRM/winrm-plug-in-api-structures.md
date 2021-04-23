---
title: Структуры API подключаемых модулей WinRM
description: Структуры API подключаемых модулей WinRM
ms.assetid: 745619bc-c7b3-48fa-8212-cb1b5b9ed4db
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685bcf87ef8c634db367db62b3ec1472b50e3b6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331280"
---
# <a name="winrm-plug-in-api-structures"></a><span data-ttu-id="0efb4-103">Структуры API подключаемых модулей WinRM</span><span class="sxs-lookup"><span data-stu-id="0efb4-103">WinRM Plug-in API Structures</span></span>

<span data-ttu-id="0efb4-104">В следующей таблице приведены общие сведения о структурах в интерфейсе прикладного программирования (API) подключаемого модуля служба удаленного управления Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="0efb4-104">The following table provides an overview of the structures in the Windows Remote Management (WinRM) plug-in application programming interface (API).</span></span>



| <span data-ttu-id="0efb4-105">Структура</span><span class="sxs-lookup"><span data-stu-id="0efb4-105">Structure</span></span>                                                        | <span data-ttu-id="0efb4-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0efb4-106">Description</span></span>                                                                              |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0efb4-107">**\_Квота на авторизацию WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="0efb4-107">**WSMAN\_AUTHZ\_QUOTA**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_authz_quota)                 | <span data-ttu-id="0efb4-108">Определяет сведения о квотах для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="0efb4-108">Defines quota information on a per-user basis.</span></span>                                           |
| [<span data-ttu-id="0efb4-109">**\_сведения о сертификате WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="0efb4-109">**WSMAN\_CERTIFICATE\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_certificate_details) | <span data-ttu-id="0efb4-110">Представляет поля в сертификате клиента.</span><span class="sxs-lookup"><span data-stu-id="0efb4-110">Represents the fields within the client certificate.</span></span>                                     |
| [<span data-ttu-id="0efb4-111">**\_ \_ набор аргументов команды \_ WSMan**</span><span class="sxs-lookup"><span data-stu-id="0efb4-111">**WSMAN\_COMMAND\_ARG\_SET**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_command_arg_set)        | <span data-ttu-id="0efb4-112">Представляет набор аргументов, передаваемых в командную строку.</span><span class="sxs-lookup"><span data-stu-id="0efb4-112">Represents the set of arguments that are passed in to the command line.</span></span>                  |
| [<span data-ttu-id="0efb4-113">**\_Фильтр WSMan**</span><span class="sxs-lookup"><span data-stu-id="0efb4-113">**WSMAN\_FILTER**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_filter)                            | <span data-ttu-id="0efb4-114">Определяет фильтрацию, используемую для операции.</span><span class="sxs-lookup"><span data-stu-id="0efb4-114">Defines the filtering used for an operation.</span></span>                                             |
| [<span data-ttu-id="0efb4-115">**\_фрагмент WSMan**</span><span class="sxs-lookup"><span data-stu-id="0efb4-115">**WSMAN\_FRAGMENT**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_fragment)                        | <span data-ttu-id="0efb4-116">Определяет сведения о фрагменте для операции.</span><span class="sxs-lookup"><span data-stu-id="0efb4-116">Defines the fragment information for an operation.</span></span>                                       |
| [<span data-ttu-id="0efb4-117">**\_ \_ сведения о операции WSMan**</span><span class="sxs-lookup"><span data-stu-id="0efb4-117">**WSMAN\_OPERATION\_INFO**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_operation_info)           | <span data-ttu-id="0efb4-118">Представляет конкретную конечную точку ресурса, для которой подключаемый модуль должен выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="0efb4-118">Represents a specific resource end-point for which the plug-in must perform the request.</span></span> |
| [<span data-ttu-id="0efb4-119">**\_запрос подключаемого модуля WSMan \_**</span><span class="sxs-lookup"><span data-stu-id="0efb4-119">**WSMAN\_PLUGIN\_REQUEST**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request)           | <span data-ttu-id="0efb4-120">Содержит сведения о запросе и передается в каждую операцию подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="0efb4-120">Contains information about the request and is passed into every plug-in operation.</span></span>       |
| [<span data-ttu-id="0efb4-121">**\_ \_ сведения об отправителе WSMan**</span><span class="sxs-lookup"><span data-stu-id="0efb4-121">**WSMAN\_SENDER\_DETAILS**</span></span>](/windows/desktop/api/Wsman/ns-wsman-wsman_sender_details)           | <span data-ttu-id="0efb4-122">Указывает сведения о клиенте для каждого входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="0efb4-122">Specifies client details for every inbound request.</span></span>                                      |



 

 

 




