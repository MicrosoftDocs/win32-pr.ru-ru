---
description: Приложение Впдсервицесаписампле
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Приложение Впдсервицесаписампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656609"
---
# <a name="wpdservicesapisample-application"></a><span data-ttu-id="89d27-103">Приложение Впдсервицесаписампле</span><span class="sxs-lookup"><span data-stu-id="89d27-103">WpdServicesApiSample Application</span></span>

<span data-ttu-id="89d27-104">Служба устройств — это расширение функционального объекта. Помимо логического группирования возможностей устройств, служба устройств предоставляет приложениям возможность программного обнаружения этих возможностей.</span><span class="sxs-lookup"><span data-stu-id="89d27-104">A device service is an extension of a functional object: In addition to logically grouping device capabilities, a device service provides applications with the ability to programmatically discover those capabilities.</span></span>

<span data-ttu-id="89d27-105">Пример приложения Впдсервицесаписампле — это классическое приложение командной строки, которое можно использовать для просмотра служб контактов на устройствах, подключенных к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="89d27-105">The WpdServicesApiSample sample application is a command-line desktop application that you can use to explore Contacts services on devices attached to your computer.</span></span> <span data-ttu-id="89d27-106">Эти службы можно просмотреть, включив поддержку форматов, событий, методов и абстрактных служб.</span><span class="sxs-lookup"><span data-stu-id="89d27-106">You can explore these services by listing supported: formats, events, methods, and abstract services.</span></span> <span data-ttu-id="89d27-107">Кроме того, это приложение можно использовать для получения свойств указанной контактной службы и вызова методов, поддерживаемых этой службой.</span><span class="sxs-lookup"><span data-stu-id="89d27-107">You can also use this application retrieve the properties on a given Contact service and to invoke methods supported by that service.</span></span>

<span data-ttu-id="89d27-108">Если у вас еще нет устройства, поддерживающего службы контактов, вы по-прежнему можете запустить Впдсервицесаписампле, если сначала установить Впдсервицесампледривер, который входит в комплект драйверов для Windows.</span><span class="sxs-lookup"><span data-stu-id="89d27-108">If you don't yet have a device that supports Contacts services, you can still run the WpdServicesApiSample if you first install the WpdServiceSampleDriver that is included in the Windows Driver Kit.</span></span>

<span data-ttu-id="89d27-109">Пример приложения Впдсервицесаписампле включает следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="89d27-109">The WpdServicesApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="89d27-110">**Файл**</span><span class="sxs-lookup"><span data-stu-id="89d27-110">**File**</span></span>                | <span data-ttu-id="89d27-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="89d27-111">**Description**</span></span>                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d27-112">Контентенумератион. cpp</span><span class="sxs-lookup"><span data-stu-id="89d27-112">ContentEnumeration.cpp</span></span>  | <span data-ttu-id="89d27-113">Содержит методы для перечисления содержимого в данной службе контактов.</span><span class="sxs-lookup"><span data-stu-id="89d27-113">Contains methods that enumerate the content on a given Contacts service.</span></span>                                                                                                                                  |
| <span data-ttu-id="89d27-114">Контентпропертиес. cpp</span><span class="sxs-lookup"><span data-stu-id="89d27-114">ContentProperties.cpp</span></span>   | <span data-ttu-id="89d27-115">Содержит методы, считывающие и записывающие свойства указанной службы контактов.</span><span class="sxs-lookup"><span data-stu-id="89d27-115">Contains methods that read and write properties on a given Contacts service.</span></span>                                                                                                                              |
| <span data-ttu-id="89d27-116">Сервицекапабилитиес. cpp</span><span class="sxs-lookup"><span data-stu-id="89d27-116">ServiceCapabilities.cpp</span></span> | <span data-ttu-id="89d27-117">Содержит методы, которые извлекают Поддерживаемые форматы, события и абстрактные службы, поддерживаемые данной службой контактов.</span><span class="sxs-lookup"><span data-stu-id="89d27-117">Contains the methods that retrieve the supported formats, events, and abstract services that are supported by a given Contacts service.</span></span>                                                                   |
| <span data-ttu-id="89d27-118">Сервицеенумератион. cpp</span><span class="sxs-lookup"><span data-stu-id="89d27-118">ServiceEnumeration.cpp</span></span>  | <span data-ttu-id="89d27-119">Содержит вспомогательные функции, которые извлекают сведения об устройстве, такие как понятное имя устройства или поддерживаемые службы контактов.</span><span class="sxs-lookup"><span data-stu-id="89d27-119">Contains the helper functions that retrieve device information such as the device-friendly name or the supported Contacts services.</span></span>                                                                       |
| <span data-ttu-id="89d27-120">Сервицемесодс. cpp</span><span class="sxs-lookup"><span data-stu-id="89d27-120">ServiceMethods.cpp</span></span>      | <span data-ttu-id="89d27-121">Содержит методы, которые извлекают и вызывают методы, поддерживаемые данной службой контактов.</span><span class="sxs-lookup"><span data-stu-id="89d27-121">Contains the methods that retrieve and invoke methods supported by a given Contacts service.</span></span>                                                                                                              |
| <span data-ttu-id="89d27-122">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="89d27-122">Stdafx.cpp</span></span>              | <span data-ttu-id="89d27-123">Включает стандартные файлы.</span><span class="sxs-lookup"><span data-stu-id="89d27-123">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="89d27-124">Впдсервицеаписампле. cpp</span><span class="sxs-lookup"><span data-stu-id="89d27-124">WpdServiceApiSample.cpp</span></span> | <span data-ttu-id="89d27-125">Размещает функцию запуска **\_ тмаин** , которая вызывает локальную функцию **домену** , которая отображает список доступных устройств и задач и вызывает функцию, подходящую для выбора пользователя в меню.</span><span class="sxs-lookup"><span data-stu-id="89d27-125">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 


## <a name="related-topics"></a><span data-ttu-id="89d27-126">См. также</span><span class="sxs-lookup"><span data-stu-id="89d27-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89d27-127">Примеры</span><span class="sxs-lookup"><span data-stu-id="89d27-127">Samples</span></span>](sample.md)
</dt> </dl>

 

 



