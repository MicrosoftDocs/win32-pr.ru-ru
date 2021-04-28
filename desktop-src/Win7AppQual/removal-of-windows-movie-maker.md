---
description: Удаление Windows Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Удаление Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116272"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="d2749-103">Удаление Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="d2749-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d2749-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="d2749-104">Affected Platforms</span></span>

<span data-ttu-id="d2749-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="d2749-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="d2749-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d2749-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="d2749-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="d2749-107">Feature Impact</span></span>

 <span data-ttu-id="d2749-108">**Серьезность** — высокая</span><span class="sxs-lookup"><span data-stu-id="d2749-108">**Severity** - High</span></span>  
<span data-ttu-id="d2749-109">**Частота** — средний</span><span class="sxs-lookup"><span data-stu-id="d2749-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="d2749-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d2749-110">Description</span></span>

<span data-ttu-id="d2749-111">Корпорация Майкрософт не является рекомендуемой и удаляет служебную программу Windows Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="d2749-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="d2749-112">В том числе:</span><span class="sxs-lookup"><span data-stu-id="d2749-112">This includes:</span></span>

-   <span data-ttu-id="d2749-113">Все точки входа в Windows Movie Maker (например, меню "Пуск", запуск > запуск)</span><span class="sxs-lookup"><span data-stu-id="d2749-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="d2749-114">Все двоичные файлы, которые использовались Windows Movie Maker (все, что было в% ProgramFiles% \\ Movie Maker)</span><span class="sxs-lookup"><span data-stu-id="d2749-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="d2749-115">Однако файлы проекта студии фильма пользователя останутся в системе и будут доступны другим приложениям, поддерживающим этот формат файлов.</span><span class="sxs-lookup"><span data-stu-id="d2749-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="d2749-116">Проявление</span><span class="sxs-lookup"><span data-stu-id="d2749-116">Manifestation</span></span>

<span data-ttu-id="d2749-117">Удаление Windows Movie Maker приводит к следующим результатам:</span><span class="sxs-lookup"><span data-stu-id="d2749-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="d2749-118">Любая попытка запустить Windows Movie Maker со своими аргументами командной строки завершится ошибкой</span><span class="sxs-lookup"><span data-stu-id="d2749-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="d2749-119">Все подключаемые модули, которые были установлены для включения новых преобразований и анимации, останутся установленными, но не будут доступны конечному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d2749-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="d2749-120">Решение</span><span class="sxs-lookup"><span data-stu-id="d2749-120">Solution</span></span>

<span data-ttu-id="d2749-121">Чтобы иметь такие функциональные возможности в будущем, пользователю потребуется установить аналогичное приложение от корпорации Майкрософт или другого поставщика программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d2749-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



