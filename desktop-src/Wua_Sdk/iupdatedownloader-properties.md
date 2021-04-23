---
description: Интерфейс Иупдатедовнлоадер определяет следующие свойства.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Свойства Иупдатедовнлоадер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810211"
---
# <a name="iupdatedownloader-properties"></a><span data-ttu-id="cc50f-103">Свойства Иупдатедовнлоадер</span><span class="sxs-lookup"><span data-stu-id="cc50f-103">IUpdateDownloader Properties</span></span>

<span data-ttu-id="cc50f-104">Интерфейс [**иупдатедовнлоадер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cc50f-104">The [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) interface defines the following properties.</span></span>



| <span data-ttu-id="cc50f-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="cc50f-105">Property</span></span>                                                             | <span data-ttu-id="cc50f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cc50f-106">Description</span></span>                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc50f-107">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="cc50f-107">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | <span data-ttu-id="cc50f-108">Возвращает и задает текущее клиентское приложение.</span><span class="sxs-lookup"><span data-stu-id="cc50f-108">Gets and sets the current client application.</span></span>                                                                                                                              |
| [<span data-ttu-id="cc50f-109">**Принудительно**</span><span class="sxs-lookup"><span data-stu-id="cc50f-109">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | <span data-ttu-id="cc50f-110">Возвращает и задает логическое значение, указывающее, будет ли агент Центр обновления Windows (WUA) принудительно загружать обновления, которые уже установлены или не могут быть установлены.</span><span class="sxs-lookup"><span data-stu-id="cc50f-110">Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed.</span></span> |
| [<span data-ttu-id="cc50f-111">**Priority**</span><span class="sxs-lookup"><span data-stu-id="cc50f-111">**Priority**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | <span data-ttu-id="cc50f-112">Возвращает и задает уровень приоритета загрузки.</span><span class="sxs-lookup"><span data-stu-id="cc50f-112">Gets and sets the priority level of the download.</span></span>                                                                                                                          |
| [<span data-ttu-id="cc50f-113">**Обновления**</span><span class="sxs-lookup"><span data-stu-id="cc50f-113">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | <span data-ttu-id="cc50f-114">Возвращает и задает интерфейс, который содержит доступную только для чтения коллекцию обновлений, указанных для загрузки.</span><span class="sxs-lookup"><span data-stu-id="cc50f-114">Gets and sets an interface that contains a read-only collection of the updates that are specified for download.</span></span>                                                            |



 

 

 



