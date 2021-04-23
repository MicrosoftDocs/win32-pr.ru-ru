---
title: Иерархия классов объектов WinNT
description: Иерархия классов объектов WinNT начинается с объекта Namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- Службы WinNT Service Provider ADSI, иерархия классов объектов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531835"
---
# <a name="winnt-object-class-hierarchy"></a><span data-ttu-id="ea647-104">Иерархия классов объектов WinNT</span><span class="sxs-lookup"><span data-stu-id="ea647-104">WinNT Object Class Hierarchy</span></span>

<span data-ttu-id="ea647-105">Иерархия классов объектов WinNT начинается с объекта Namespace.</span><span class="sxs-lookup"><span data-stu-id="ea647-105">The WinNT object class hierarchy starts from the Namespace object.</span></span>



| <span data-ttu-id="ea647-106">Класс объекта</span><span class="sxs-lookup"><span data-stu-id="ea647-106">Object class</span></span>                   | <span data-ttu-id="ea647-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ea647-107">Description</span></span>                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ea647-108">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ea647-108">Namespace</span></span><br/>           | <span data-ttu-id="ea647-109">Контейнер объектов верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="ea647-109">Top-level object container.</span></span><br/>                                            |
| <span data-ttu-id="ea647-110">Домен</span><span class="sxs-lookup"><span data-stu-id="ea647-110">Domain</span></span><br/>              | <span data-ttu-id="ea647-111">Домен Windows NT.</span><span class="sxs-lookup"><span data-stu-id="ea647-111">The Windows NT domain.</span></span><br/>                                                 |
| <span data-ttu-id="ea647-112">Пользователь</span><span class="sxs-lookup"><span data-stu-id="ea647-112">User</span></span><br/>                | <span data-ttu-id="ea647-113">Учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea647-113">User account.</span></span><br/>                                                          |
| <span data-ttu-id="ea647-114">Группа</span><span class="sxs-lookup"><span data-stu-id="ea647-114">Group</span></span><br/>               | <span data-ttu-id="ea647-115">Учетная запись группы для управления правами доступа.</span><span class="sxs-lookup"><span data-stu-id="ea647-115">Group account for managing access rights.</span></span><br/>                              |
| <span data-ttu-id="ea647-116">усерграупколлектион</span><span class="sxs-lookup"><span data-stu-id="ea647-116">UserGroupCollection</span></span><br/> | <span data-ttu-id="ea647-117">Набор групп пользователей, реализующих [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="ea647-117">A set of user groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/>  |
| <span data-ttu-id="ea647-118">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="ea647-118">GroupCollection</span></span><br/>     | <span data-ttu-id="ea647-119">Набор других групп, реализующих [**иадсмемберс**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span><span class="sxs-lookup"><span data-stu-id="ea647-119">A set of other groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/> |
| <span data-ttu-id="ea647-120">Компьютер</span><span class="sxs-lookup"><span data-stu-id="ea647-120">Computer</span></span><br/>            | <span data-ttu-id="ea647-121">Сервер или рабочая станция Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="ea647-121">Windows NT 4.0 server or workstation.</span></span><br/>                                  |
| <span data-ttu-id="ea647-122">PrintJob</span><span class="sxs-lookup"><span data-stu-id="ea647-122">PrintJob</span></span><br/>            | <span data-ttu-id="ea647-123">Задание печати в очереди печати.</span><span class="sxs-lookup"><span data-stu-id="ea647-123">Print job in the print queue.</span></span><br/>                                          |
| <span data-ttu-id="ea647-124">принтжобсколлектион</span><span class="sxs-lookup"><span data-stu-id="ea647-124">PrintJobsCollection</span></span><br/> | <span data-ttu-id="ea647-125">Набор заданий печати.</span><span class="sxs-lookup"><span data-stu-id="ea647-125">A set of print jobs.</span></span><br/>                                                   |
| <span data-ttu-id="ea647-126">PrintQueue</span><span class="sxs-lookup"><span data-stu-id="ea647-126">PrintQueue</span></span><br/>          | <span data-ttu-id="ea647-127">Очередь печати в диспетчере очереди принтера.</span><span class="sxs-lookup"><span data-stu-id="ea647-127">Print queue on a printer spooler.</span></span><br/>                                      |
| <span data-ttu-id="ea647-128">Служба</span><span class="sxs-lookup"><span data-stu-id="ea647-128">Service</span></span><br/>             | <span data-ttu-id="ea647-129">Приложение, работающее как служба.</span><span class="sxs-lookup"><span data-stu-id="ea647-129">Application running as a service.</span></span><br/>                                      |
| <span data-ttu-id="ea647-130">FileService</span><span class="sxs-lookup"><span data-stu-id="ea647-130">FileService</span></span><br/>         | <span data-ttu-id="ea647-131">Службы, обращающиеся к файловой системе.</span><span class="sxs-lookup"><span data-stu-id="ea647-131">Services accessing file system.</span></span><br/>                                        |
| <span data-ttu-id="ea647-132">FileShare</span><span class="sxs-lookup"><span data-stu-id="ea647-132">FileShare</span></span><br/>           | <span data-ttu-id="ea647-133">Общая папка.</span><span class="sxs-lookup"><span data-stu-id="ea647-133">File share point.</span></span><br/>                                                      |
| <span data-ttu-id="ea647-134">Ресурс</span><span class="sxs-lookup"><span data-stu-id="ea647-134">Resource</span></span><br/>            | <span data-ttu-id="ea647-135">Ресурс в службе.</span><span class="sxs-lookup"><span data-stu-id="ea647-135">A resource in the service.</span></span><br/>                                             |
| <span data-ttu-id="ea647-136">Сеанс</span><span class="sxs-lookup"><span data-stu-id="ea647-136">Session</span></span><br/>             | <span data-ttu-id="ea647-137">Активное подключение к службе файлов.</span><span class="sxs-lookup"><span data-stu-id="ea647-137">An active file service connection.</span></span><br/>                                     |
| <span data-ttu-id="ea647-138">Пользователь</span><span class="sxs-lookup"><span data-stu-id="ea647-138">User</span></span><br/>                | <span data-ttu-id="ea647-139">Локальная учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea647-139">Local user account.</span></span><br/>                                                    |
| <span data-ttu-id="ea647-140">Группа</span><span class="sxs-lookup"><span data-stu-id="ea647-140">Group</span></span><br/>               | <span data-ttu-id="ea647-141">Локальная группа.</span><span class="sxs-lookup"><span data-stu-id="ea647-141">Local group.</span></span><br/>                                                           |
| <span data-ttu-id="ea647-142">усерколлектион</span><span class="sxs-lookup"><span data-stu-id="ea647-142">UserCollection</span></span><br/>      | <span data-ttu-id="ea647-143">Коллекция локальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ea647-143">Collection of local users.</span></span><br/>                                             |
| <span data-ttu-id="ea647-144">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="ea647-144">GroupCollection</span></span><br/>     | <span data-ttu-id="ea647-145">Коллекция локальных групп.</span><span class="sxs-lookup"><span data-stu-id="ea647-145">Collection of local groups.</span></span><br/>                                            |
| <span data-ttu-id="ea647-146">схема</span><span class="sxs-lookup"><span data-stu-id="ea647-146">Schema</span></span><br/>              | <span data-ttu-id="ea647-147">Контейнер "WinNT Schema".</span><span class="sxs-lookup"><span data-stu-id="ea647-147">WinNT Schema container.</span></span><br/>                                                |
| <span data-ttu-id="ea647-148">Класс</span><span class="sxs-lookup"><span data-stu-id="ea647-148">Class</span></span><br/>               | <span data-ttu-id="ea647-149">Определение класса схемы.</span><span class="sxs-lookup"><span data-stu-id="ea647-149">Schema class definition.</span></span><br/>                                               |
| <span data-ttu-id="ea647-150">Свойство</span><span class="sxs-lookup"><span data-stu-id="ea647-150">Property</span></span><br/>            | <span data-ttu-id="ea647-151">Определение атрибута схемы.</span><span class="sxs-lookup"><span data-stu-id="ea647-151">Schema attribute definition.</span></span><br/>                                           |
| <span data-ttu-id="ea647-152">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ea647-152">Syntax</span></span><br/>              | <span data-ttu-id="ea647-153">Синтаксис свойства.</span><span class="sxs-lookup"><span data-stu-id="ea647-153">Syntax of a property.</span></span><br/>                                                  |



 

 

 





