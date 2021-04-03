---
description: Интерфейс Исеарчжоб определяет следующие свойства.
ms.assetid: 9e1675e9-fe40-4209-aba9-1cabb4f3ea4c
title: Свойства Исеарчжоб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5c49a5af7435819750451c89ca68f976d76f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145733"
---
# <a name="isearchjob-properties"></a><span data-ttu-id="52e81-103">Свойства Исеарчжоб</span><span class="sxs-lookup"><span data-stu-id="52e81-103">ISearchJob Properties</span></span>

<span data-ttu-id="52e81-104">Интерфейс [**исеарчжоб**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) определяет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="52e81-104">The [**ISearchJob**](/windows/desktop/api/Wuapi/nn-wuapi-isearchjob) interface defines the following properties.</span></span>



| <span data-ttu-id="52e81-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="52e81-105">Property</span></span>                                      | <span data-ttu-id="52e81-106">Описание</span><span class="sxs-lookup"><span data-stu-id="52e81-106">Description</span></span>                                                                                                                                                 |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52e81-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="52e81-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_asyncstate)   | <span data-ttu-id="52e81-108">Возвращает объект состояния, относящегося к вызывающему объекту, который передается в метод [**иупдатесеарч. бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) .</span><span class="sxs-lookup"><span data-stu-id="52e81-108">Gets the caller-specific state object that is passed to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method.</span></span>                         |
| [<span data-ttu-id="52e81-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="52e81-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-get_iscompleted) | <span data-ttu-id="52e81-110">Возвращает логическое значение, указывающее, полностью ли обрабатывается вызов метода [**иупдатесеарч. бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) .</span><span class="sxs-lookup"><span data-stu-id="52e81-110">Gets a Boolean value that indicates whether the call to the [**IUpdateSearch.BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch) method is completely processed.</span></span> |



 

 

 



