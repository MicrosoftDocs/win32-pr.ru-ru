---
description: Интерфейс Иинсталлатионпрогресс определяет следующие свойства.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Свойства Иинсталлатионпрогресс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692482"
---
# <a name="iinstallationprogress-properties"></a><span data-ttu-id="c92ad-103">Свойства Иинсталлатионпрогресс</span><span class="sxs-lookup"><span data-stu-id="c92ad-103">IInstallationProgress Properties</span></span>

<span data-ttu-id="c92ad-104">Интерфейс [**иинсталлатионпрогресс**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c92ad-104">The [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="c92ad-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="c92ad-105">Property</span></span>                                                                                   | <span data-ttu-id="c92ad-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c92ad-106">Description</span></span>                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c92ad-107">**куррентупдатеиндекс**</span><span class="sxs-lookup"><span data-stu-id="c92ad-107">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | <span data-ttu-id="c92ad-108">Возвращает значение индекса, начинающееся с нуля, указывающее обновление, которое устанавливается или удаляется, если было выбрано несколько обновлений.</span><span class="sxs-lookup"><span data-stu-id="c92ad-108">Gets a zero-based index value that specifies the update that is currently being installed or uninstalled when multiple updates have been selected.</span></span> |
| [<span data-ttu-id="c92ad-109">**куррентупдатеперценткомплете**</span><span class="sxs-lookup"><span data-stu-id="c92ad-109">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="c92ad-110">Возвращает время, в течение которого выполнялась установка или удаление текущего обновления в процентах.</span><span class="sxs-lookup"><span data-stu-id="c92ad-110">Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.</span></span>                                    |
| [<span data-ttu-id="c92ad-111">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="c92ad-111">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | <span data-ttu-id="c92ad-112">Возвращает время, в течение которого весь процесс установки или удаления был выполнен, в процентах.</span><span class="sxs-lookup"><span data-stu-id="c92ad-112">Gets how far the overall installation or uninstallation process has progressed, as a percentage.</span></span>                                                   |



 

 

 



