---
description: Интерфейс Иаутоматикупдатессеттингс определяет следующие методы.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Методы Иаутоматикупдатессеттингс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898514"
---
# <a name="iautomaticupdatessettings-methods"></a><span data-ttu-id="15f65-103">Методы Иаутоматикупдатессеттингс</span><span class="sxs-lookup"><span data-stu-id="15f65-103">IAutomaticUpdatesSettings Methods</span></span>

<span data-ttu-id="15f65-104">Интерфейс [**иаутоматикупдатессеттингс**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) определяет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="15f65-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following methods.</span></span>



| <span data-ttu-id="15f65-105">Метод</span><span class="sxs-lookup"><span data-stu-id="15f65-105">Method</span></span>                                               | <span data-ttu-id="15f65-106">Описание</span><span class="sxs-lookup"><span data-stu-id="15f65-106">Description</span></span>                                      |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="15f65-107">**Обновить**</span><span class="sxs-lookup"><span data-stu-id="15f65-107">**Refresh**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | <span data-ttu-id="15f65-108">Извлекает последние параметры автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="15f65-108">Retrieves the latest Automatic Updates settings.</span></span> |
| [<span data-ttu-id="15f65-109">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="15f65-109">**Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | <span data-ttu-id="15f65-110">Применяет текущие параметры автоматическое обновление.</span><span class="sxs-lookup"><span data-stu-id="15f65-110">Applies the current Automatic Updates settings.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="15f65-111">В Windows RT вы больше не можете использовать метод [**иаутоматикупдатессеттингс:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) для настройки параметров центр обновления Windows программным способом.</span><span class="sxs-lookup"><span data-stu-id="15f65-111">On Windows RT, you can no longer use the [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) method to configure Windows Update settings programmatically.</span></span> <span data-ttu-id="15f65-112">Операция настройки завершается сбоем, если для задания любого значения, отличного от 4 ([**аунлсчедулединсталлатион**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)), используется команда **Save** .</span><span class="sxs-lookup"><span data-stu-id="15f65-112">The configuration operation fails if you use **Save** to set any value other than 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span></span>

 

 

 



