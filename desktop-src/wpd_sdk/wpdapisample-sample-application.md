---
description: Приложение Впдаписампле
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Приложение Впдаписампле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809538"
---
# <a name="wpdapisample-application"></a><span data-ttu-id="5fecc-103">Приложение Впдаписампле</span><span class="sxs-lookup"><span data-stu-id="5fecc-103">WpdApiSample Application</span></span>

<span data-ttu-id="5fecc-104">Пример приложения Впдаписампле — это классическое приложение командной строки, которое позволяет перечислить подключенные устройства, исследовать устройства, объекты запросов для свойств и атрибутов, отправлять и получать объекты и т. д.</span><span class="sxs-lookup"><span data-stu-id="5fecc-104">The WpdApiSample sample application is a command-line desktop application that enables you to enumerate connected devices, explore devices, query objects for properties and attributes, send and retrieve objects, and so on.</span></span> <span data-ttu-id="5fecc-105">При запуске приложение открывает командное окно со списком задач, которые можно выполнять.</span><span class="sxs-lookup"><span data-stu-id="5fecc-105">On startup, the application opens a command window that lists the tasks you can perform.</span></span>

<span data-ttu-id="5fecc-106">Пример приложения Впдаписампле включает следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="5fecc-106">The WpdApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="5fecc-107">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5fecc-107">**File**</span></span>               | <span data-ttu-id="5fecc-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5fecc-108">**Description**</span></span>                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fecc-109">Контентенумератион. cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-109">ContentEnumeration.cpp</span></span> | <span data-ttu-id="5fecc-110">Содержит функции, которые перечисляют все объекты на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5fecc-110">Contains functions that enumerate all the objects on a device.</span></span>                                                                                                                                            |
| <span data-ttu-id="5fecc-111">Контентпропертиес. cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-111">ContentProperties.cpp</span></span>  | <span data-ttu-id="5fecc-112">Содержит функции, считывающие и записывающие свойства объекта и выполняющие задания и запросы на получение набора свойств.</span><span class="sxs-lookup"><span data-stu-id="5fecc-112">Contains functions that read and write object properties and make bulk property set/get requests.</span></span>                                                                                                         |
| <span data-ttu-id="5fecc-113">Контенттрансфер. cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-113">ContentTransfer.cpp</span></span>    | <span data-ttu-id="5fecc-114">Содержит функции, которые передают содержимое на устройство или с устройства, считывает требования к типу объекта и создают папку на устройстве.</span><span class="sxs-lookup"><span data-stu-id="5fecc-114">Contains functions that transfer content to or from the device, read object type requirements, and create a folder on the device.</span></span>                                                                         |
| <span data-ttu-id="5fecc-115">Девицекапабилитиес. cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-115">DeviceCapabilities.cpp</span></span> | <span data-ttu-id="5fecc-116">Содержит функции для перечисления типов функциональных объектов на устройстве, перечисления типов содержимого, поддерживаемых каждым типом функционального объекта, и отображения профилей объектов отрисовки.</span><span class="sxs-lookup"><span data-stu-id="5fecc-116">Contains functions to list the functional object types on the device, list the content types supported by each functional object type, and display rendering object profiles.</span></span>                             |
| <span data-ttu-id="5fecc-117">Девицеенумератион. cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-117">DeviceEnumeration.cpp</span></span>  | <span data-ttu-id="5fecc-118">Список понятных имен, изготовителей и описаний всех подключенных устройств.</span><span class="sxs-lookup"><span data-stu-id="5fecc-118">Lists the friendly names, manufacturers, and descriptions of all connected devices.</span></span>                                                                                                                       |
| <span data-ttu-id="5fecc-119">Девицеевентс. cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-119">DeviceEvents.cpp</span></span>       | <span data-ttu-id="5fecc-120">Содержит функции, которые регистрируют события устройства и их параметры при каждом срабатывании событий.</span><span class="sxs-lookup"><span data-stu-id="5fecc-120">Contains functions that log device events and their parameters whenever events are fired.</span></span>                                                                                                                 |
| <span data-ttu-id="5fecc-121">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-121">Stdafx.cpp</span></span>             | <span data-ttu-id="5fecc-122">Включает стандартные файлы.</span><span class="sxs-lookup"><span data-stu-id="5fecc-122">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="5fecc-123">Впдаписампле. cpp</span><span class="sxs-lookup"><span data-stu-id="5fecc-123">WpdApiSample.cpp</span></span>       | <span data-ttu-id="5fecc-124">Размещает функцию запуска **\_ тмаин** , которая вызывает локальную функцию **домену** , которая отображает список доступных устройств и задач и вызывает функцию, подходящую для выбора пользователя в меню.</span><span class="sxs-lookup"><span data-stu-id="5fecc-124">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5fecc-125">См. также</span><span class="sxs-lookup"><span data-stu-id="5fecc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fecc-126">Образец</span><span class="sxs-lookup"><span data-stu-id="5fecc-126">Sample</span></span>](sample.md)
</dt> </dl>

 

 



