---
description: Интерфейс Идовнлоадпрогресс определяет следующие свойства.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Свойства Идовнлоадпрогресс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991175"
---
# <a name="idownloadprogress-properties"></a><span data-ttu-id="1073e-103">Свойства Идовнлоадпрогресс</span><span class="sxs-lookup"><span data-stu-id="1073e-103">IDownloadProgress Properties</span></span>

<span data-ttu-id="1073e-104">Интерфейс [**идовнлоадпрогресс**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1073e-104">The [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="1073e-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="1073e-105">Property</span></span>                                                                               | <span data-ttu-id="1073e-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1073e-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1073e-107">**куррентупдатебитесдовнлоадед**</span><span class="sxs-lookup"><span data-stu-id="1073e-107">**CurrentUpdateBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | <span data-ttu-id="1073e-108">Возвращает строку, которая указывает, сколько данных было передано для файла содержимого или файлов загружаемого обновления в байтах.</span><span class="sxs-lookup"><span data-stu-id="1073e-108">Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.</span></span>  |
| [<span data-ttu-id="1073e-109">**куррентупдатебитестодовнлоад**</span><span class="sxs-lookup"><span data-stu-id="1073e-109">**CurrentUpdateBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | <span data-ttu-id="1073e-110">Возвращает строку, которая определяет объем данных, которые должны быть переданы для файла содержимого или файлов, загружаемых при обновлении, в байтах.</span><span class="sxs-lookup"><span data-stu-id="1073e-110">Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.</span></span> |
| [<span data-ttu-id="1073e-111">**куррентупдатедовнлоадфасе**</span><span class="sxs-lookup"><span data-stu-id="1073e-111">**CurrentUpdateDownloadPhase**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | <span data-ttu-id="1073e-112">Возвращает значение перечисления [**довнлоадфасе**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) , указывающее фазу загрузки, которая выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="1073e-112">Gets a [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) enumeration value that specifies the phase of the download that is currently in progress.</span></span>          |
| [<span data-ttu-id="1073e-113">**куррентупдатеиндекс**</span><span class="sxs-lookup"><span data-stu-id="1073e-113">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | <span data-ttu-id="1073e-114">Возвращает значение индекса, начинающееся с нуля, указывающее обновление, которое загружается в данный момент, когда было выбрано несколько обновлений.</span><span class="sxs-lookup"><span data-stu-id="1073e-114">Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.</span></span>             |
| [<span data-ttu-id="1073e-115">**куррентупдатеперценткомплете**</span><span class="sxs-lookup"><span data-stu-id="1073e-115">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="1073e-116">Возвращает оценку процента текущего обновления, которое было загружено.</span><span class="sxs-lookup"><span data-stu-id="1073e-116">Gets an estimate of the percentage of the current update that has been downloaded.</span></span>                                                               |
| [<span data-ttu-id="1073e-117">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="1073e-117">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | <span data-ttu-id="1073e-118">Возвращает оценку процента всех загруженных обновлений.</span><span class="sxs-lookup"><span data-stu-id="1073e-118">Gets an estimate of the percentage of all the updates that have been downloaded.</span></span>                                                                 |
| [<span data-ttu-id="1073e-119">**TotalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="1073e-119">**TotalBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | <span data-ttu-id="1073e-120">Возвращает строку, указывающую общий объем скачанных данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="1073e-120">Gets a string that specifies the total amount of data that has been downloaded, in bytes.</span></span>                                                        |
| [<span data-ttu-id="1073e-121">**тоталбитестодовнлоад**</span><span class="sxs-lookup"><span data-stu-id="1073e-121">**TotalBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | <span data-ttu-id="1073e-122">Возвращает строку, представляющую оценку общего объема данных, которые будут скачаны в байтах.</span><span class="sxs-lookup"><span data-stu-id="1073e-122">Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.</span></span>                                        |



 

 

 



