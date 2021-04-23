---
description: В следующих обзорах описываются типы системных сведений.
ms.assetid: cb7b50fc-6591-48a9-b3a7-327de9a6dc06
title: Сведения о системе Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1df90d6e7a5a90d9ee108d67e5f9182ffca59f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662831"
---
# <a name="windows-system-information"></a><span data-ttu-id="03b98-103">Сведения о системе Windows</span><span class="sxs-lookup"><span data-stu-id="03b98-103">Windows System Information</span></span>

<span data-ttu-id="03b98-104">В следующих обзорах описываются типы системных сведений.</span><span class="sxs-lookup"><span data-stu-id="03b98-104">The following overviews describe the types of system information available.</span></span>



| <span data-ttu-id="03b98-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="03b98-105">Overview</span></span>                                                | <span data-ttu-id="03b98-106">Описание</span><span class="sxs-lookup"><span data-stu-id="03b98-106">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03b98-107">Дескрипторы и объекты</span><span class="sxs-lookup"><span data-stu-id="03b98-107">Handles and Objects</span></span>](handles-and-objects.md)          | <span data-ttu-id="03b98-108">*Объект* — это структура данных, представляющая системный ресурс, например файл, поток или графическое изображение.</span><span class="sxs-lookup"><span data-stu-id="03b98-108">An *object* is a data structure that represents a system resource, such as a file, thread, or graphic image.</span></span> <span data-ttu-id="03b98-109">Приложение не может напрямую обращаться к данным объекта или системному ресурсу, который представляет объект.</span><span class="sxs-lookup"><span data-stu-id="03b98-109">An application cannot directly access object data or the system resource that an object represents.</span></span> <span data-ttu-id="03b98-110">Вместо этого приложение должно получить *обработчик* объекта, который можно использовать для проверки или изменения системного ресурса.</span><span class="sxs-lookup"><span data-stu-id="03b98-110">Instead, an application must obtain an object *handle*, which it can use to examine or modify the system resource.</span></span> |
| [<span data-ttu-id="03b98-111">Реестр</span><span class="sxs-lookup"><span data-stu-id="03b98-111">Registry</span></span>](registry.md)                                | <span data-ttu-id="03b98-112">Системная база данных, в которой приложения и системное хранилище и извлекаются сведения о конфигурации.</span><span class="sxs-lookup"><span data-stu-id="03b98-112">A system-defined database in which applications and the system store and retrieve configuration information.</span></span>                                                                                                                                                                                                                        |
| [<span data-ttu-id="03b98-113">Информация о системе</span><span class="sxs-lookup"><span data-stu-id="03b98-113">System Information</span></span>](system-information.md)            | <span data-ttu-id="03b98-114">Возвращает или задает конфигурацию системы, параметры, версию и метрики.</span><span class="sxs-lookup"><span data-stu-id="03b98-114">Retrieves or sets system configuration, settings, version, and metrics.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="03b98-115">Time</span><span class="sxs-lookup"><span data-stu-id="03b98-115">Time</span></span>](time.md)                                        | <span data-ttu-id="03b98-116">Возвращает или задает системное время.</span><span class="sxs-lookup"><span data-stu-id="03b98-116">Retrieves or sets the system time.</span></span>                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="03b98-117">Поставщик времени</span><span class="sxs-lookup"><span data-stu-id="03b98-117">Time Provider</span></span>](time-provider.md)                      | <span data-ttu-id="03b98-118">Получает точные отметки времени от оборудования или сети и предоставляет метки времени другим клиентам в сети.</span><span class="sxs-lookup"><span data-stu-id="03b98-118">Retrieves accurate time stamps from hardware or the network, and provides time stamps to other clients on the network.</span></span>                                                                                                                                                                                                              |
| [<span data-ttu-id="03b98-119">Платформа оценки WaaS</span><span class="sxs-lookup"><span data-stu-id="03b98-119">WaaS Assessment Platform</span></span>](update-assessor-service.md) | <span data-ttu-id="03b98-120">Платформа оценки обновлений Windows как услуга (WaaS) предоставляет сведения об обновлениях Windows на устройстве.</span><span class="sxs-lookup"><span data-stu-id="03b98-120">The Windows as a Service (WaaS) Update Assessment Platform provides information on a device's Windows updates.</span></span>                                                                                                                                                                                                                      |



 

## <a name="additional-resources"></a><span data-ttu-id="03b98-121">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="03b98-121">Additional Resources</span></span>



|                                                                                                                                   |                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03b98-122">Форум общих проблем разработки Windows</span><span class="sxs-lookup"><span data-stu-id="03b98-122">General Windows Development Issues Forum</span></span>](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsgeneraldevelopmentissues) | <span data-ttu-id="03b98-123">Обсуждение сведений о системе Windows и других общих проблем, связанных с разработкой приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="03b98-123">Discuss Windows System Information and other general issues about developing applications for Windows.</span></span><br/> |



 

 

 




