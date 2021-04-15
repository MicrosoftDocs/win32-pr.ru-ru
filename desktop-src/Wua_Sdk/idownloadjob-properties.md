---
description: Интерфейс Идовнлоаджоб определяет следующие свойства.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Свойства Идовнлоаджоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701647"
---
# <a name="idownloadjob-properties"></a><span data-ttu-id="fdf03-103">Свойства Идовнлоаджоб</span><span class="sxs-lookup"><span data-stu-id="fdf03-103">IDownloadJob Properties</span></span>

<span data-ttu-id="fdf03-104">Интерфейс [**идовнлоаджоб**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fdf03-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following properties.</span></span>



| <span data-ttu-id="fdf03-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="fdf03-105">Property</span></span>                                        | <span data-ttu-id="fdf03-106">Описание</span><span class="sxs-lookup"><span data-stu-id="fdf03-106">Description</span></span>                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdf03-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="fdf03-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | <span data-ttu-id="fdf03-108">Возвращает объект состояния, относящегося к вызывающему объекту, который передается в метод [**иупдатедовнлоадер. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .</span><span class="sxs-lookup"><span data-stu-id="fdf03-108">Gets the caller-specific state object that is passed to the [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) method.</span></span>           |
| [<span data-ttu-id="fdf03-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="fdf03-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | <span data-ttu-id="fdf03-110">Возвращает параметр, указывающий, полностью ли был обработан вызов [**иупдатедовнлоадер. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .</span><span class="sxs-lookup"><span data-stu-id="fdf03-110">Gets the setting that indicates whether the call to [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) was processed completely.</span></span> |
| [<span data-ttu-id="fdf03-111">**Обновления**</span><span class="sxs-lookup"><span data-stu-id="fdf03-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | <span data-ttu-id="fdf03-112">Возвращает интерфейс, содержащий доступную только для чтения коллекцию обновлений, указанных в скачивании.</span><span class="sxs-lookup"><span data-stu-id="fdf03-112">Gets an interface that contains a read-only collection of the updates that are specified in a download.</span></span>                                                  |



 

 

 



