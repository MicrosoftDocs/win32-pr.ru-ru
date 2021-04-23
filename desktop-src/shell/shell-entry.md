---
description: Пользовательский интерфейс Windows предоставляет пользователям доступ к широкому спектру объектов, необходимых для запуска приложений и управления операционной системой.
title: Оболочка Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985612"
---
# <a name="windows-shell"></a><span data-ttu-id="00e98-103">Оболочка Windows</span><span class="sxs-lookup"><span data-stu-id="00e98-103">Windows Shell</span></span>

<span data-ttu-id="00e98-104">Пользовательский интерфейс Windows предоставляет пользователям доступ к широкому спектру объектов, необходимых для запуска приложений и управления операционной системой.</span><span class="sxs-lookup"><span data-stu-id="00e98-104">The Windows UI provides users with access to a wide variety of objects necessary for running applications and managing the operating system.</span></span> <span data-ttu-id="00e98-105">Самыми многочисленными и знакомыми этими объектами являются папки и файлы, расположенные на дисках компьютера.</span><span class="sxs-lookup"><span data-stu-id="00e98-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="00e98-106">Существует также ряд виртуальных объектов, позволяющих пользователю выполнять такие задачи, как отправка файлов на удаленные принтеры или доступ к корзине.</span><span class="sxs-lookup"><span data-stu-id="00e98-106">There are also a number of virtual objects that allow the user to perform tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="00e98-107">Оболочка организует эти объекты в иерархическое пространство имен и предоставляет пользователям и приложениям единообразный и эффективный способ доступа к объектам и управления ими.</span><span class="sxs-lookup"><span data-stu-id="00e98-107">The Shell organizes these objects into a hierarchical namespace and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="shell-development-scenarios"></a><span data-ttu-id="00e98-108">Сценарии разработки оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-108">Shell Development Scenarios</span></span>

<span data-ttu-id="00e98-109">Следующие сценарии разработки относятся к разработке приложений:</span><span class="sxs-lookup"><span data-stu-id="00e98-109">The following development scenarios relate to application development:</span></span>

-   <span data-ttu-id="00e98-110">Расширение оболочки, которая состоит из создания источника данных (и использования модели данных оболочки)</span><span class="sxs-lookup"><span data-stu-id="00e98-110">Extending the Shell, which consists of creating a data source (versus consuming the Shell data model)</span></span>
-   <span data-ttu-id="00e98-111">Реализация подмножества задач источника данных оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-111">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="00e98-112">Поддержка библиотек и представлений элементов в проводнике Windows</span><span class="sxs-lookup"><span data-stu-id="00e98-112">Supporting libraries and item views in Windows Explorer</span></span>
-   <span data-ttu-id="00e98-113">Использование диалогового окна «common File»</span><span class="sxs-lookup"><span data-stu-id="00e98-113">Using the common file dialog</span></span>
-   <span data-ttu-id="00e98-114">Реализация элементов панели управления</span><span class="sxs-lookup"><span data-stu-id="00e98-114">Implementing Control Panel items</span></span>
-   <span data-ttu-id="00e98-115">Управление уведомлениями</span><span class="sxs-lookup"><span data-stu-id="00e98-115">Managing notifications</span></span>

<span data-ttu-id="00e98-116">Следующие сценарии разработки относятся к владению File Format:</span><span class="sxs-lookup"><span data-stu-id="00e98-116">The following development scenarios relate to file format ownership:</span></span>

-   <span data-ttu-id="00e98-117">Реализация подмножества задач источника данных оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-117">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="00e98-118">Реализация любого обработчика</span><span class="sxs-lookup"><span data-stu-id="00e98-118">Implementing any handler</span></span>
-   <span data-ttu-id="00e98-119">Поддержка поиска на рабочем столе</span><span class="sxs-lookup"><span data-stu-id="00e98-119">Supporting desktop search</span></span>

<span data-ttu-id="00e98-120">Следующие сценарии разработки относятся к владению хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="00e98-120">The following development scenarios relate to data storage ownership:</span></span>

-   <span data-ttu-id="00e98-121">Поддержка поиска на рабочем столе и OpenSearch</span><span class="sxs-lookup"><span data-stu-id="00e98-121">Supporting desktop search and OpenSearch</span></span>
-   <span data-ttu-id="00e98-122">Реализация подмножества задач «Источник данных оболочки» (виртуальные папки)</span><span class="sxs-lookup"><span data-stu-id="00e98-122">Implementing a subset of the Shell data source tasks (virtual folders)</span></span>
-   <span data-ttu-id="00e98-123">Вспомогательные библиотеки в проводнике Windows</span><span class="sxs-lookup"><span data-stu-id="00e98-123">Supporting libraries in Windows Explorer</span></span>

<span data-ttu-id="00e98-124">Следующий сценарий разработки относится к поддержке устройств:</span><span class="sxs-lookup"><span data-stu-id="00e98-124">The following development scenario relates to device support:</span></span>

-   <span data-ttu-id="00e98-125">Автоматический запуск и автоматическое воспроизведение</span><span class="sxs-lookup"><span data-stu-id="00e98-125">Auto run and auto play</span></span>

## <a name="windows-shell-sdk-documentation"></a><span data-ttu-id="00e98-126">Документация по пакету SDK оболочки Windows</span><span class="sxs-lookup"><span data-stu-id="00e98-126">Windows Shell SDK Documentation</span></span>

<span data-ttu-id="00e98-127">Эта документация разбивается на три основных раздела:</span><span class="sxs-lookup"><span data-stu-id="00e98-127">This documentation is broken into three major sections:</span></span>

-   <span data-ttu-id="00e98-128">[Руководство разработчика по оболочке](intro.md) содержит основные материалы о принципах работы оболочки и использовании API оболочки в приложении.</span><span class="sxs-lookup"><span data-stu-id="00e98-128">The [Shell Developer's Guide](intro.md) provides conceptual material about how the Shell works and how to use the Shell's API in your application.</span></span>
-   <span data-ttu-id="00e98-129">В разделе [справочника по оболочке](shell-reference-bumper.md) документируется программные элементы, составляющие различные API-интерфейсы оболочки.</span><span class="sxs-lookup"><span data-stu-id="00e98-129">The [Shell Reference](shell-reference-bumper.md) section documents programming elements that make up the various Shell APIs.</span></span>
-   <span data-ttu-id="00e98-130">[Примеры оболочки](samples-entry.md) содержат ссылки на связанные примеры кода.</span><span class="sxs-lookup"><span data-stu-id="00e98-130">[Shell Samples](samples-entry.md) provides links to related code samples.</span></span>

<span data-ttu-id="00e98-131">В следующей таблице приведена схема раздела Справочника по оболочке.</span><span class="sxs-lookup"><span data-stu-id="00e98-131">The following table provides an outline of the Shell Reference section.</span></span> <span data-ttu-id="00e98-132">Если не указано иное, все программные элементы задокументированы в неуправляемом C++.</span><span class="sxs-lookup"><span data-stu-id="00e98-132">Unless otherwise noted, all programming elements are documented in unmanaged C++.</span></span>



| <span data-ttu-id="00e98-133">Section</span><span class="sxs-lookup"><span data-stu-id="00e98-133">Section</span></span>                                                               | <span data-ttu-id="00e98-134">Описание</span><span class="sxs-lookup"><span data-stu-id="00e98-134">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00e98-135">Классы оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-135">Shell Classes</span></span>](classes.md)                                          | <span data-ttu-id="00e98-136">В этом разделе описывается выбор классов оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="00e98-136">This section describes select Windows Shell classes.</span></span>                                                                 |
| [<span data-ttu-id="00e98-137">Интерфейсы оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-137">Shell Interfaces</span></span>](interfaces.md)                                    | <span data-ttu-id="00e98-138">В этом разделе описываются интерфейсы модели COM компонента оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="00e98-138">This section describes the Windows Shell Component Object Model (COM) interfaces.</span></span>                                    |
| [<span data-ttu-id="00e98-139">Функции оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-139">Shell Functions</span></span>](functions.md)                                      | <span data-ttu-id="00e98-140">В этом разделе описываются функции оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="00e98-140">This section describes the Windows Shell functions.</span></span>                                                                  |
| [<span data-ttu-id="00e98-141">Функции обратного вызова оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-141">Shell Callback Functions</span></span>](callbacks.md)                             | <span data-ttu-id="00e98-142">В этом разделе описываются шаблоны функций обратного вызова оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="00e98-142">This section describes the Windows Shell callback functions templates.</span></span>                                               |
| [<span data-ttu-id="00e98-143">Константы, перечисления и флаги оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-143">Shell Constants, Enumerations, and Flags</span></span>](consts-enums-flags.md)    | <span data-ttu-id="00e98-144">В этом разделе описываются константы, перечисления и флаги оболочки Windows, используемые в интерфейсах API оболочки.</span><span class="sxs-lookup"><span data-stu-id="00e98-144">This section describes the Windows Shell constants, enumerations, and flags used in the Shell APIs.</span></span>                  |
| [<span data-ttu-id="00e98-145">Упрощенные служебные функции оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-145">Shell Lightweight Utility Functions</span></span>](shlwapi.md)                    | <span data-ttu-id="00e98-146">В этом разделе описываются функции упрощенной служебной программы оболочки Windows, предоставляемые в Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="00e98-146">This section describes the Windows Shell lightweight utility functions provided in Shlwapi.dll.</span></span>                      |
| [<span data-ttu-id="00e98-147">Макросы оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-147">Shell Macros</span></span>](macros.md)                                            | <span data-ttu-id="00e98-148">В этом разделе описываются макросы служебной программы оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="00e98-148">This section describes the Windows Shell utility macros.</span></span>                                                             |
| [<span data-ttu-id="00e98-149">Сообщения и уведомления оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-149">Shell Messages and Notifications</span></span>](messages.md)                      | <span data-ttu-id="00e98-150">В этом разделе описываются сообщения и уведомления, отправляемые элементами оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="00e98-150">This section describes the messages and notifications sent by elements of the Windows Shell.</span></span>                         |
| [<span data-ttu-id="00e98-151">Объекты оболочки для сценариев и Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="00e98-151">Shell Objects for Scripting and Microsoft Visual Basic</span></span>](objects.md) | <span data-ttu-id="00e98-152">В этом разделе описываются объекты Windows, реализованные оболочкой для использования в сценариях и Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="00e98-152">This section describes the Windows objects implemented by the Shell for use in scripting and Microsoft Visual Basic.</span></span> |
| [<span data-ttu-id="00e98-153">Объекты оболочки для C++</span><span class="sxs-lookup"><span data-stu-id="00e98-153">Shell Objects for C++</span></span>](objects-cpp.md)                              | <span data-ttu-id="00e98-154">В этом разделе описываются объекты Windows в C++, реализованные оболочкой.</span><span class="sxs-lookup"><span data-stu-id="00e98-154">This section describes the C++ Windows objects implemented by the Shell.</span></span>                                             |
| [<span data-ttu-id="00e98-155">Схемы оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-155">Shell Schemas</span></span>](schemas.md)                                          | <span data-ttu-id="00e98-156">В этом разделе описывается библиотека, свойства и передаваемые схемы манифестов, используемые оболочкой Windows.</span><span class="sxs-lookup"><span data-stu-id="00e98-156">This section describes library, property, and transfer manifest schemas used by the Windows Shell.</span></span>                   |
| [<span data-ttu-id="00e98-157">Структуры оболочки</span><span class="sxs-lookup"><span data-stu-id="00e98-157">Shell Structures</span></span>](structures.md)                                    | <span data-ttu-id="00e98-158">В этом разделе описываются структуры оболочки Windows, используемые в интерфейсах API оболочки.</span><span class="sxs-lookup"><span data-stu-id="00e98-158">This section describes the Windows Shell structures used in the Shell APIs.</span></span>                                          |



 

 

 



