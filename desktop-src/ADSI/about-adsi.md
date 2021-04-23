---
title: Сведения об интерфейсах служб Active Directory
description: Active Directory интерфейсов служб (ADSI) абстрагирует возможности служб каталогов от разных поставщиков сети в распределенных вычислительных средах для предоставления единого набора интерфейсов службы каталогов для управления сетевыми ресурсами.
ms.assetid: 6d601af5-7470-42c2-b99e-21174ea008b1
ms.tgt_platform: multiple
keywords:
- Сведения об интерфейсах Active Directory Service Interfaces ADSI
- ADSI ADSI, сведения
- Интерфейсы служб Active Directory ADSI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc083b33a633335da12915257fcddff1174a6858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132818"
---
# <a name="about-active-directory-service-interfaces"></a><span data-ttu-id="95c39-106">Сведения об интерфейсах служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="95c39-106">About Active Directory Service Interfaces</span></span>

<span data-ttu-id="95c39-107">Active Directory интерфейсов служб (ADSI) абстрагирует возможности служб каталогов от разных поставщиков сети в распределенных вычислительных средах для предоставления единого набора интерфейсов службы каталогов для управления сетевыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="95c39-107">Active Directory Service Interfaces (ADSI) abstracts the capabilities of directory services from different network providers in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="95c39-108">Администраторы и разработчики могут использовать службы ADSI для перечисления ресурсов в службе каталогов и управления ими независимо от того, какая сетевая среда содержит этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="95c39-108">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="95c39-109">ADSI упрощает выполнение стандартных административных задач, таких как добавление новых пользователей, Управление принтерами и поиск ресурсов в среде распределенных вычислений.</span><span class="sxs-lookup"><span data-stu-id="95c39-109">ADSI makes it easier to perform common administrative tasks, such as adding new users, managing printers, and locating resources throughout the distributed computing environment.</span></span>

<span data-ttu-id="95c39-110">Интерфейсы ADSI позволяют разработчикам легко «включать в каталог» свои приложения.</span><span class="sxs-lookup"><span data-stu-id="95c39-110">ADSI makes it easy for developers to "directory enable" their applications.</span></span> <span data-ttu-id="95c39-111">Администраторы и разработчики работают с одним набором интерфейсов службы каталогов независимо от того, какие службы каталогов установлены.</span><span class="sxs-lookup"><span data-stu-id="95c39-111">Administrators and developers handle a single set of directory service interfaces, regardless of which directory services are installed.</span></span>

<span data-ttu-id="95c39-112">В этом введении рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="95c39-112">The following topics are discussed in this introduction:</span></span>

-   [<span data-ttu-id="95c39-113">Несколько служб каталогов</span><span class="sxs-lookup"><span data-stu-id="95c39-113">Multiple Directory Services</span></span>](multiple-directory-services.md)
-   [<span data-ttu-id="95c39-114">Кто будет использовать интерфейсы служб Active Directory?</span><span class="sxs-lookup"><span data-stu-id="95c39-114">Who Will Use Active Directory Service Interfaces?</span></span>](who-will-use-active-directory-service-interfaces.md)
-   [<span data-ttu-id="95c39-115">Службы каталогов сегодня</span><span class="sxs-lookup"><span data-stu-id="95c39-115">Directory Services Today</span></span>](directory-services-today.md)
-   [<span data-ttu-id="95c39-116">Преимущества использования интерфейсов служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="95c39-116">Benefits of Using Active Directory Service Interfaces</span></span>](benefits-of-using-active-directory-service-interfaces.md)
-   [<span data-ttu-id="95c39-117">Архитектура интерфейсов служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="95c39-117">Active Directory Service Interfaces Architecture</span></span>](active-directory-service-interfaces-architecture.md)
-   [<span data-ttu-id="95c39-118">Поддержка языков программирования</span><span class="sxs-lookup"><span data-stu-id="95c39-118">Programming Language Support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="95c39-119">Свойства и атрибуты ADSI</span><span class="sxs-lookup"><span data-stu-id="95c39-119">ADSI Properties and Attributes</span></span>](adsi-properties-and-attributes.md)

## <a name="what-you-should-know-before-reading-this-guide"></a><span data-ttu-id="95c39-120">Что необходимо узнать перед чтением этого руководством</span><span class="sxs-lookup"><span data-stu-id="95c39-120">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="95c39-121">В этом руководство предполагается, что вы знакомы с моделью COM и автоматизацией и знаете, как программировать в Visual Basic или C/C++.</span><span class="sxs-lookup"><span data-stu-id="95c39-121">This guide assumes that you are familiar with the Component Object Model (COM) and Automation, and that you know how to program in either Visual Basic or C/C++.</span></span>

<span data-ttu-id="95c39-122">Некоторые термины, используемые в этом пошаговом руководству, являются уникальными для среды либо ADSI, либо службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="95c39-122">Some of the terms used in this guide are unique to either ADSI or the directory services environment.</span></span> <span data-ttu-id="95c39-123">Другие термины будут знакомы, но могут иметь немного разные значения в этих средах.</span><span class="sxs-lookup"><span data-stu-id="95c39-123">Other terms will be familiar but may have slightly different meanings in these environments.</span></span>

## <a name="further-reading-about-adsi-and-related-topics"></a><span data-ttu-id="95c39-124">Дополнительные материалы по ADSI и связанным темам</span><span class="sxs-lookup"><span data-stu-id="95c39-124">Further Reading about ADSI and Related Topics</span></span>

<span data-ttu-id="95c39-125">Дополнительные сведения об интерфейсах служб Active Directory и технологиях, на которых они основаны, могут оказаться полезными следующие источники.</span><span class="sxs-lookup"><span data-stu-id="95c39-125">For more information about Active Directory Service Interfaces and the technologies on which they are based, you may find the following sources helpful.</span></span>

<span data-ttu-id="95c39-126">Брокксчмидт, Краиг.</span><span class="sxs-lookup"><span data-stu-id="95c39-126">Brockschmidt, Kraig.</span></span> <span data-ttu-id="95c39-127">*Внутри OLE*, 2-го выпуска.</span><span class="sxs-lookup"><span data-stu-id="95c39-127">*Inside OLE*, 2nd edition.</span></span> <span data-ttu-id="95c39-128">Redmond, штат Вашингтон: Microsoft Press, 1995.</span><span class="sxs-lookup"><span data-stu-id="95c39-128">Redmond, WA: Microsoft Press, 1995.</span></span>

<span data-ttu-id="95c39-129">Chappell, Дэвид.</span><span class="sxs-lookup"><span data-stu-id="95c39-129">Chappell, David.</span></span> <span data-ttu-id="95c39-130">*Основные сведения об ActiveX и OLE*.</span><span class="sxs-lookup"><span data-stu-id="95c39-130">*Understanding ActiveX and OLE*.</span></span> <span data-ttu-id="95c39-131">Redmond, штат Вашингтон: Microsoft Press, 1996.</span><span class="sxs-lookup"><span data-stu-id="95c39-131">Redmond, WA: Microsoft Press, 1996.</span></span>

<span data-ttu-id="95c39-132">Хахн, Андрей.</span><span class="sxs-lookup"><span data-stu-id="95c39-132">Hahn, Steven.</span></span> <span data-ttu-id="95c39-133">*Справочник программиста по ASP ADSI*.</span><span class="sxs-lookup"><span data-stu-id="95c39-133">*ADSI ASP Programmer's Reference*.</span></span> <span data-ttu-id="95c39-134">Wrox нажмите Ltd., 1998.</span><span class="sxs-lookup"><span data-stu-id="95c39-134">Wrox Press Ltd., 1998.</span></span>

<span data-ttu-id="95c39-135">Харрисон, романский.</span><span class="sxs-lookup"><span data-stu-id="95c39-135">Harrison, Richard.</span></span> <span data-ttu-id="95c39-136">*Веб-Безопасность ASP/MTS/ADSI*.</span><span class="sxs-lookup"><span data-stu-id="95c39-136">*ASP/MTS/ADSI Web Security*.</span></span> <span data-ttu-id="95c39-137">Prentice зал, 1999.</span><span class="sxs-lookup"><span data-stu-id="95c39-137">Prentice Hall, 1999.</span></span>

<span data-ttu-id="95c39-138">Справочник по Microsoft OLE DB программиста версии 1,0, 1996.</span><span class="sxs-lookup"><span data-stu-id="95c39-138">Microsoft's OLE DB Programmer's Reference Version 1.0, 1996.</span></span>

<span data-ttu-id="95c39-139">*Справочник программиста по OLE 2, том два*.</span><span class="sxs-lookup"><span data-stu-id="95c39-139">*OLE 2 Programmer's Reference, Volume Two*.</span></span> <span data-ttu-id="95c39-140">Redmond, штат Вашингтон: Microsoft Press, 1994.</span><span class="sxs-lookup"><span data-stu-id="95c39-140">Redmond, WA: Microsoft Press, 1994.</span></span>

<span data-ttu-id="95c39-141">Rogerson's, Дэйл.</span><span class="sxs-lookup"><span data-stu-id="95c39-141">Rogerson, Dale.</span></span> <span data-ttu-id="95c39-142">*Внутри com*.</span><span class="sxs-lookup"><span data-stu-id="95c39-142">*Inside COM*.</span></span> <span data-ttu-id="95c39-143">Redmond, штат Вашингтон: Microsoft Press, 1997.</span><span class="sxs-lookup"><span data-stu-id="95c39-143">Redmond, WA: Microsoft Press, 1997.</span></span>

<span data-ttu-id="95c39-144">*Спецификация Active Directory служб версии 2,0*.</span><span class="sxs-lookup"><span data-stu-id="95c39-144">*The Active Directory Service Design Specification Version 2.0*.</span></span>

<span data-ttu-id="95c39-145">*Спецификация объектной модели компонента*.</span><span class="sxs-lookup"><span data-stu-id="95c39-145">*The Component Object Model Specification*.</span></span>

<span data-ttu-id="95c39-146">(Эти ресурсы могут быть недоступны в некоторых языках и странах или регионах.)</span><span class="sxs-lookup"><span data-stu-id="95c39-146">(These resources may not be available in some languages and countries/regions.)</span></span>

 

 




