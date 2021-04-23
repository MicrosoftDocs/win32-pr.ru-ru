---
description: Некоторые приложения разработаны таким образом, чтобы запретить установку нескольких экземпляров приложения на компьютер.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Ограничения разработки приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682342"
---
# <a name="application-design-restrictions"></a><span data-ttu-id="44725-103">Ограничения разработки приложений</span><span class="sxs-lookup"><span data-stu-id="44725-103">Application Design Restrictions</span></span>

<span data-ttu-id="44725-104">Некоторые приложения разработаны таким образом, чтобы запретить установку нескольких экземпляров приложения на компьютер.</span><span class="sxs-lookup"><span data-stu-id="44725-104">Some applications are designed in a way that prevents multiple instances of the application from being installed on a computer.</span></span> <span data-ttu-id="44725-105">Благодаря такому ограничению приложение не может использовать функцию "секции".</span><span class="sxs-lookup"><span data-stu-id="44725-105">With such a limitation, an application cannot make use of the partitions feature.</span></span> <span data-ttu-id="44725-106">Чтобы можно было использовать секции для этого приложения, может потребоваться изменить следующие компоненты разработки приложения.</span><span class="sxs-lookup"><span data-stu-id="44725-106">The following application design features might need to be modified before partitions can be used for that application.</span></span>

## <a name="tables-and-arrays"></a><span data-ttu-id="44725-107">Таблицы и массивы</span><span class="sxs-lookup"><span data-stu-id="44725-107">Tables and Arrays</span></span>

<span data-ttu-id="44725-108">Некоторые приложения создают таблицы базы данных, таблицы в памяти или массивы, использующие CLSID в качестве уникального раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="44725-108">Some applications create database tables, in-memory tables, or arrays that use a CLSID as a unique registry key.</span></span> <span data-ttu-id="44725-109">На компьютере без разделов этот раздел реестра обычно является компьютером/CLSID (по одному идентификатору CLSID на компьютер).</span><span class="sxs-lookup"><span data-stu-id="44725-109">On a computer without partitions, this registry key is typically computer/CLSID (one CLSID per computer).</span></span>

<span data-ttu-id="44725-110">И наоборот, на компьютере с разделами этот раздел реестра является ИДЕНТИФИКАТОРом компьютера/секции, ИДЕНТИФИКАТОРом приложения или CLSID (несколькими экземплярами идентификатора CLSID на компьютер).</span><span class="sxs-lookup"><span data-stu-id="44725-110">Conversely, on a computer with partitions, this registry key is computer/partition ID/application ID/CLSID (multiple instances of a CLSID per computer).</span></span> <span data-ttu-id="44725-111">Поскольку функция partitions позволяет использовать на компьютере несколько экземпляров идентификатора CLSID, приложения, содержащие элементы дизайна, требующие уникального идентификатора CLSID на компьютер, могут быть неблагоприятно затронуты.</span><span class="sxs-lookup"><span data-stu-id="44725-111">Because the partitions feature allows multiple instances of a CLSID to exist on a computer, applications that contain design elements that require a unique CLSID per computer might be adversely affected.</span></span>

## <a name="global-resources"></a><span data-ttu-id="44725-112">Глобальные ресурсы</span><span class="sxs-lookup"><span data-stu-id="44725-112">Global Resources</span></span>

<span data-ttu-id="44725-113">Некоторые приложения используют глобальные ресурсы, такие как общая память, файлы данных и записи реестра.</span><span class="sxs-lookup"><span data-stu-id="44725-113">Some applications use global resources such as shared memory, data files, and registry entries.</span></span> <span data-ttu-id="44725-114">Это может вызвать проблемы, если несколько экземпляров такого приложения выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="44725-114">This could cause problems if multiple instances of such an application are executing simultaneously.</span></span>

<span data-ttu-id="44725-115">Например, если компонент использует общую память для взаимодействия с другими компонентами, необходимо изменить компонент, чтобы каждый экземпляр компонента выделил свою собственную общую память.</span><span class="sxs-lookup"><span data-stu-id="44725-115">For example, if a component uses shared memory for interacting with other components, the component will need to be modified so that each instance of the component allocates its own shared memory.</span></span>

## <a name="type-libraries"></a><span data-ttu-id="44725-116">Библиотеки типов</span><span class="sxs-lookup"><span data-stu-id="44725-116">Type Libraries</span></span>

<span data-ttu-id="44725-117">Библиотеки типов предоставляют сведения о интерфейсах и методах компонента.</span><span class="sxs-lookup"><span data-stu-id="44725-117">Type libraries provide information about a component's interfaces and methods.</span></span> <span data-ttu-id="44725-118">Эти сведения используются в нескольких целях, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="44725-118">This information is used for several purposes, including the following:</span></span>

-   <span data-ttu-id="44725-119">Маршалирование данных между компонентами при вызовах функций</span><span class="sxs-lookup"><span data-stu-id="44725-119">Marshaling data between components when function calls are made</span></span>
-   <span data-ttu-id="44725-120">Помощь в очередях компонентов COM+ и службах событий COM+</span><span class="sxs-lookup"><span data-stu-id="44725-120">Helping the COM+ Queued Components and COM+ Events services</span></span>
-   <span data-ttu-id="44725-121">Предоставление правильных сведений в редакторе Visual Basic Майкрософт</span><span class="sxs-lookup"><span data-stu-id="44725-121">Providing the correct information within a Microsoft Visual Basic editor</span></span>

<span data-ttu-id="44725-122">Ссылки на библиотеку типов устанавливаются в реестр компьютера.</span><span class="sxs-lookup"><span data-stu-id="44725-122">References to a type library are installed in the registry of a computer.</span></span> <span data-ttu-id="44725-123">При разработке приложений, которые будут вызываться из секций, важно, чтобы в реестре была установлена последняя версия библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="44725-123">When developing applications that will be invoked from within partitions, it is important that the latest version of a type library is installed in the registry.</span></span> <span data-ttu-id="44725-124">Это гарантирует, что используемый редактор Visual Basic будет получать точную информацию о методах, доступных для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="44725-124">This ensures that the Visual Basic editor being used will get accurate information about the methods available for that component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44725-125">См. также</span><span class="sxs-lookup"><span data-stu-id="44725-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44725-126">Компоненты и разделы, помещенные в очередь COM+</span><span class="sxs-lookup"><span data-stu-id="44725-126">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="44725-127">Реализация секционирования</span><span class="sxs-lookup"><span data-stu-id="44725-127">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="44725-128">Регистрация и Активация компонентов в секциях</span><span class="sxs-lookup"><span data-stu-id="44725-128">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="44725-129">Что такое разделы COM+?</span><span class="sxs-lookup"><span data-stu-id="44725-129">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



