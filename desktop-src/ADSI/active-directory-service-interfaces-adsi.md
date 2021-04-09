---
title: Интерфейсы служб Active Directory
description: Общие сведения об интерфейсах служб Active Directory Services со ссылками на различные руководства.
ms.assetid: b24f9789-b9f5-49c4-9812-298bae8b28a9
ms.tgt_platform: multiple
keywords:
- ADSI ADSI
- Интерфейсы служб Active Directory (см. ADSI)
- ADSI ADSI, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15cc702fec86f1202f1fbd00ba575fd848e4ab74
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070619"
---
# <a name="active-directory-service-interfaces"></a><span data-ttu-id="6d39e-106">Интерфейсы служб Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d39e-106">Active Directory Service Interfaces</span></span>

## <a name="purpose"></a><span data-ttu-id="6d39e-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="6d39e-107">Purpose</span></span>

<span data-ttu-id="6d39e-108">Интерфейсы служб Active Directory (ADSI) — это набор COM-интерфейсов, используемых для доступа к функциям служб каталогов из разных поставщиков сети.</span><span class="sxs-lookup"><span data-stu-id="6d39e-108">Active Directory Service Interfaces (ADSI) is a set of COM interfaces used to access the features of directory services from different network providers.</span></span> <span data-ttu-id="6d39e-109">ADSI используется в распределенных вычислительных средах для предоставления единого набора интерфейсов службы каталогов для управления сетевыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="6d39e-109">ADSI is used in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="6d39e-110">Администраторы и разработчики могут использовать службы ADSI для перечисления ресурсов в службе каталогов и управления ими независимо от того, какая сетевая среда содержит этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="6d39e-110">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="6d39e-111">ADSI позволяет выполнять стандартные административные задачи, такие как добавление новых пользователей, Управление принтерами и поиск ресурсов в распределенной вычислительной среде.</span><span class="sxs-lookup"><span data-stu-id="6d39e-111">ADSI enables common administrative tasks, such as adding new users, managing printers, and locating resources in a distributed computing environment.</span></span>

> [!Note]  
> <span data-ttu-id="6d39e-112">Следующая документация предназначена для компьютерных программистов.</span><span class="sxs-lookup"><span data-stu-id="6d39e-112">The following documentation is for computer programmers.</span></span> <span data-ttu-id="6d39e-113">Если вы являетесь конечным пользователем, пытающимся выполнить отладку ошибки печати или проблемы с домашней сетью, см. [форумы сообщества Майкрософт](https://answers.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6d39e-113">If you are an end-user trying to debug a printing error or home network issue, see the [Microsoft community forums](https://answers.microsoft.com).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="6d39e-114">Где применимо</span><span class="sxs-lookup"><span data-stu-id="6d39e-114">Where applicable</span></span>

<span data-ttu-id="6d39e-115">Сетевые администраторы могут использовать ADSI для автоматизации распространенных задач, таких как добавление пользователей и групп, Управление принтерами и настройка разрешений для сетевых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d39e-115">Network Administrators can use ADSI to automate common tasks, such as adding users and groups, managing printers, and setting permissions on network resources.</span></span>

<span data-ttu-id="6d39e-116">Независимые поставщики программного обеспечения и разработчики конечных пользователей могут использовать ADSI для включения в каталог своих продуктов и приложений.</span><span class="sxs-lookup"><span data-stu-id="6d39e-116">Independent Software Vendors and end-user developers can use ADSI to "directory enable" their products and applications.</span></span> <span data-ttu-id="6d39e-117">Службы могут публиковать себя в каталоге, клиенты могут использовать каталог для поиска служб, и оба они могут использовать каталог для поиска других интересующих объектов и управления ими.</span><span class="sxs-lookup"><span data-stu-id="6d39e-117">Services can publish themselves in a directory, clients can use the directory to find the services, and both can use the directory to find and manipulate other objects of interest.</span></span> <span data-ttu-id="6d39e-118">Так как интерфейсы служб Active Directory не зависят от базовых служб каталогов, продукты и приложения с поддержкой каталогов могут успешно взаимодействовать в нескольких средах сети и каталогов.</span><span class="sxs-lookup"><span data-stu-id="6d39e-118">Because Active Directory Service Interfaces are independent of the underlying directory service(s), directory-enabled products and applications can operate successfully in multiple network and directory environments.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6d39e-119">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="6d39e-119">Developer audience</span></span>

<span data-ttu-id="6d39e-120">Клиентские приложения ADSI можно писать на многих языках.</span><span class="sxs-lookup"><span data-stu-id="6d39e-120">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="6d39e-121">Для большинства административных задач ADSI определяет интерфейсы и объекты, доступные из совместимых с автоматизацией языков, таких как Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) и Java, на более производительные и эффективные языки, такие как C и C++.</span><span class="sxs-lookup"><span data-stu-id="6d39e-121">For most administrative tasks, ADSI defines interfaces and objects accessible from Automation-compliant languages like Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and Java to the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="6d39e-122">Хорошим основанием программирования COM является полезность программисту ADSI.</span><span class="sxs-lookup"><span data-stu-id="6d39e-122">A good foundation in COM programming is useful to the ADSI programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6d39e-123">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="6d39e-123">Run-time requirements</span></span>

<span data-ttu-id="6d39e-124">Active Directory выполняется на контроллерах домена Windows Server.</span><span class="sxs-lookup"><span data-stu-id="6d39e-124">Active Directory runs on Windows Server domain controllers.</span></span> <span data-ttu-id="6d39e-125">Однако клиентские приложения, использующие ADSI, могут быть написаны и запущены в Windows.</span><span class="sxs-lookup"><span data-stu-id="6d39e-125">However, client applications using ADSI may be written and run on Windows.</span></span> <span data-ttu-id="6d39e-126">Кроме того, разработчикам требуется пакет средств разработки программного обеспечения платформы (SDK), также доступный на веб-сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="6d39e-126">In addition, developers will want the Platform Software Development Kit (SDK), also available on the MSDN website.</span></span> <span data-ttu-id="6d39e-127">Чтобы исследовать содержимое Active Directory, используйте оснастку MMC Active Directory пользователи и компьютеры.</span><span class="sxs-lookup"><span data-stu-id="6d39e-127">To investigate the contents of Active Directory, use the Active Directory Users and Computers MMC snap-in.</span></span> <span data-ttu-id="6d39e-128">Эта оснастка заменяет средство Адсвв, доступное для предыдущих версий Windows.</span><span class="sxs-lookup"><span data-stu-id="6d39e-128">This snap-in replaces the Adsvw tool that was available for previous versions of Windows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6d39e-129">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="6d39e-129">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6d39e-130">О ADSI</span><span class="sxs-lookup"><span data-stu-id="6d39e-130">About ADSI</span></span>](about-adsi.md)
</dt> <dd>

<span data-ttu-id="6d39e-131">Общие сведения о ADSI.</span><span class="sxs-lookup"><span data-stu-id="6d39e-131">General information about ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="6d39e-132">Использование ADSI</span><span class="sxs-lookup"><span data-stu-id="6d39e-132">Using ADSI</span></span>](using-adsi.md)
</dt> <dd>

<span data-ttu-id="6d39e-133">Рекомендации программиста по использованию ADSI.</span><span class="sxs-lookup"><span data-stu-id="6d39e-133">Programmer's Guide to using ADSI.</span></span>

</dd> <dt>

[<span data-ttu-id="6d39e-134">Краткие руководства по использованию ADSI</span><span class="sxs-lookup"><span data-stu-id="6d39e-134">ADSI Quick-start Tutorials</span></span>](adsi-quick-start-tutorials.md)
</dt> <dd>

<span data-ttu-id="6d39e-135">Использование ADSI с автоматизацией для управления каталогами.</span><span class="sxs-lookup"><span data-stu-id="6d39e-135">Using ADSI with Automation to manage directories.</span></span>

</dd> <dt>

[<span data-ttu-id="6d39e-136">Справочник по ADSI</span><span class="sxs-lookup"><span data-stu-id="6d39e-136">ADSI Reference</span></span>](adsi-reference.md)
</dt> <dd>

<span data-ttu-id="6d39e-137">Документация по интерфейсам и методам ADSI.</span><span class="sxs-lookup"><span data-stu-id="6d39e-137">Documentation of ADSI interfaces and methods.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6d39e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="6d39e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d39e-139">Модель COM</span><span class="sxs-lookup"><span data-stu-id="6d39e-139">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> <dt>

[<span data-ttu-id="6d39e-140">COM-клиенты и серверы</span><span class="sxs-lookup"><span data-stu-id="6d39e-140">COM Clients and Servers</span></span>](../com/com-clients-and-servers.md)
</dt> <dt>

[<span data-ttu-id="6d39e-141">Доменные службы Active Directory</span><span class="sxs-lookup"><span data-stu-id="6d39e-141">Active Directory Domain Services</span></span>](../ad/active-directory-domain-services.md)
</dt> </dl>

 

 