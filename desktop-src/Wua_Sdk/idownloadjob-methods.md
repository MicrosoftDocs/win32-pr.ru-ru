---
description: Интерфейс Идовнлоаджоб определяет следующие методы.
ms.assetid: b9a6b722-2e32-4177-bcef-514412e132ec
title: Методы Идовнлоаджоб
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f68acd6d7fef37c4ce9309c559a1de1b4d516dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542295"
---
# <a name="idownloadjob-methods"></a><span data-ttu-id="dd414-103">Методы Идовнлоаджоб</span><span class="sxs-lookup"><span data-stu-id="dd414-103">IDownloadJob Methods</span></span>

<span data-ttu-id="dd414-104">Интерфейс [**идовнлоаджоб**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) определяет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dd414-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following methods.</span></span>



| <span data-ttu-id="dd414-105">Метод</span><span class="sxs-lookup"><span data-stu-id="dd414-105">Method</span></span>                                            | <span data-ttu-id="dd414-106">Описание</span><span class="sxs-lookup"><span data-stu-id="dd414-106">Description</span></span>                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd414-107">**Чистку**</span><span class="sxs-lookup"><span data-stu-id="dd414-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup)           | <span data-ttu-id="dd414-108">Ожидает завершения асинхронной операции и освобождает все обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="dd414-108">Waits for an asynchronous operation to be completed and releases all callbacks.</span></span>                                        |
| [<span data-ttu-id="dd414-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="dd414-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-getprogress)   | <span data-ttu-id="dd414-110">Возвращает интерфейс [**идовнлоадпрогресс**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) , который описывает текущий ход выполнения загрузки.</span><span class="sxs-lookup"><span data-stu-id="dd414-110">Returns an [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface that describes the current progress of a download.</span></span> |
| [<span data-ttu-id="dd414-111">**рекуестаборт**</span><span class="sxs-lookup"><span data-stu-id="dd414-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-requestabort) | <span data-ttu-id="dd414-112">Выполняет запрос на завершение асинхронной загрузки.</span><span class="sxs-lookup"><span data-stu-id="dd414-112">Makes a request to end an asynchronous download.</span></span>                                                                       |



 

 

 



