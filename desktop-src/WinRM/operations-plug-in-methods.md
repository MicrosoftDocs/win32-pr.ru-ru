---
title: Методы подключаемых модулей операций
description: Методы подключаемых модулей операций
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986052"
---
# <a name="operations-plug-in-methods"></a><span data-ttu-id="81c59-103">Методы подключаемых модулей операций</span><span class="sxs-lookup"><span data-stu-id="81c59-103">Operations Plug-in Methods</span></span>

<span data-ttu-id="81c59-104">Все точки входа подключаемых модулей операций имеют механизм обратного вызова для сообщения об успешном или неуспешном вызове.</span><span class="sxs-lookup"><span data-stu-id="81c59-104">All operations plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="81c59-105">Некоторые механизмы обратного вызова вызываются несколько раз, пока не будут переданы все результаты.</span><span class="sxs-lookup"><span data-stu-id="81c59-105">Some callback mechanisms are called multiple times, until all of the results are reported.</span></span>

<span data-ttu-id="81c59-106">В следующей таблице приведены общие сведения о методах обратного вызова операций.</span><span class="sxs-lookup"><span data-stu-id="81c59-106">The following table provides an overview of the operations callback methods.</span></span>



| <span data-ttu-id="81c59-107">Метод</span><span class="sxs-lookup"><span data-stu-id="81c59-107">Method</span></span>                                                                         | <span data-ttu-id="81c59-108">Описание</span><span class="sxs-lookup"><span data-stu-id="81c59-108">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="81c59-109">**всманплугинфрирекуестдетаилс**</span><span class="sxs-lookup"><span data-stu-id="81c59-109">**WSManPluginFreeRequestDetails**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | <span data-ttu-id="81c59-110">Освобождает память, выделенную для структуры [**\_ \_ запросов подключаемого модуля WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) .</span><span class="sxs-lookup"><span data-stu-id="81c59-110">Releases memory that is allocated for the [**WSMAN\_PLUGIN\_REQUEST**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) structure.</span></span>                                          |
| [<span data-ttu-id="81c59-111">**всманплугинжетоператионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="81c59-111">**WSManPluginGetOperationParameters**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | <span data-ttu-id="81c59-112">Возвращает операционную информацию, например время ожидания и ограничения данных, связанные с операцией.</span><span class="sxs-lookup"><span data-stu-id="81c59-112">Gets operational information, such as time-outs and data restrictions that are associated with an operation.</span></span>                                         |
| [<span data-ttu-id="81c59-113">**всманплугиноператионкомплете**</span><span class="sxs-lookup"><span data-stu-id="81c59-113">**WSManPluginOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | <span data-ttu-id="81c59-114">Записывает данные о завершении операции.</span><span class="sxs-lookup"><span data-stu-id="81c59-114">Records the completion of an operation.</span></span>                                                                                                              |
| [<span data-ttu-id="81c59-115">**всманплугинрецеивересулт**</span><span class="sxs-lookup"><span data-stu-id="81c59-115">**WSManPluginReceiveResult**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | <span data-ttu-id="81c59-116">Сообщает результаты в служба удаленного управления Windows подключаемые модули (WinRM).</span><span class="sxs-lookup"><span data-stu-id="81c59-116">Reports results to Windows Remote Management (WinRM) plug-ins.</span></span>                                                                                       |
| [<span data-ttu-id="81c59-117">**всманплугинрепортконтекст**</span><span class="sxs-lookup"><span data-stu-id="81c59-117">**WSManPluginReportContext**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | <span data-ttu-id="81c59-118">Сообщает оболочке и контекст команды обратно в инфраструктуру WinRM, чтобы выполнять дальнейшие операции с оболочкой или командой.</span><span class="sxs-lookup"><span data-stu-id="81c59-118">Reports the shell and command context back to the WinRM infrastructure so that further operations can be performed against the shell and/or command.</span></span> |



 

 

 




