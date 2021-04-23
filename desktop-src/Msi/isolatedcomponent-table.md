---
description: Каждая запись таблицы Исолатедкомпонент связывает компонент, указанный в \_ столбце «приложение-компонент» (обычно это exe-файл), с компонентом, указанным в \_ общем столбце Component (обычно это общая библиотека DLL).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Таблица Исолатедкомпонент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682715"
---
# <a name="isolatedcomponent-table"></a><span data-ttu-id="7840b-103">Таблица Исолатедкомпонент</span><span class="sxs-lookup"><span data-stu-id="7840b-103">IsolatedComponent Table</span></span>

<span data-ttu-id="7840b-104">Каждая запись таблицы Исолатедкомпонент связывает компонент, указанный в \_ столбце «приложение-компонент» (обычно это exe-файл), с компонентом, указанным в \_ общем столбце Component (обычно это общая библиотека DLL).</span><span class="sxs-lookup"><span data-stu-id="7840b-104">Each record of the IsolatedComponent table associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span> <span data-ttu-id="7840b-105">[Действие исолатекомпонентс](isolatecomponents-action.md) устанавливает копию компонента, \_ совместно используемого в частном расположении, для использования приложением-компонентом \_ .</span><span class="sxs-lookup"><span data-stu-id="7840b-105">The [IsolateComponents action](isolatecomponents-action.md) installs a copy of Component\_Shared into a private location for use by Component\_Application.</span></span> <span data-ttu-id="7840b-106">Это позволяет изолировать приложение-компонент \_ от других копий общего компонента \_ , которые могут быть установлены в общую папку на компьютере.</span><span class="sxs-lookup"><span data-stu-id="7840b-106">This isolates the Component\_Application from other copies of Component\_Shared that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="7840b-107">См. раздел [изолированные компоненты](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="7840b-107">See [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="7840b-108">Чтобы связать один компонент \_ , общий для нескольких компонентных \_ приложений, включите отдельную запись для каждой пары в таблице исолатедкомпонентс.</span><span class="sxs-lookup"><span data-stu-id="7840b-108">To link one Component\_Shared to multiple Component\_Application, include a separate record for each pair in the IsolatedComponents table.</span></span> <span data-ttu-id="7840b-109">Установщик копирует файлы компонента \_ , которые совместно используются, в каталог каждого \_ установленного приложения компонента.</span><span class="sxs-lookup"><span data-stu-id="7840b-109">The installer copies the files of Component\_Shared into the directory of each Component\_Application that is installed.</span></span>

<span data-ttu-id="7840b-110">Таблица Исолатедкомпонент содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="7840b-110">The IsolatedComponent table has the following columns.</span></span>



| <span data-ttu-id="7840b-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="7840b-111">Column</span></span>                 | <span data-ttu-id="7840b-112">Type</span><span class="sxs-lookup"><span data-stu-id="7840b-112">Type</span></span>                         | <span data-ttu-id="7840b-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="7840b-113">Key</span></span> | <span data-ttu-id="7840b-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="7840b-114">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="7840b-115">\_Общий компонент</span><span class="sxs-lookup"><span data-stu-id="7840b-115">Component\_Shared</span></span>      | [<span data-ttu-id="7840b-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7840b-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="7840b-117">Да</span><span class="sxs-lookup"><span data-stu-id="7840b-117">Y</span></span>   | <span data-ttu-id="7840b-118">Нет</span><span class="sxs-lookup"><span data-stu-id="7840b-118">N</span></span>        |
| <span data-ttu-id="7840b-119">\_Приложение компонента</span><span class="sxs-lookup"><span data-stu-id="7840b-119">Component\_Application</span></span> | [<span data-ttu-id="7840b-120">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="7840b-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="7840b-121">Да</span><span class="sxs-lookup"><span data-stu-id="7840b-121">Y</span></span>   | <span data-ttu-id="7840b-122">Нет</span><span class="sxs-lookup"><span data-stu-id="7840b-122">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7840b-123">Столбцы</span><span class="sxs-lookup"><span data-stu-id="7840b-123">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7840b-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>\_Общий компонент</span><span class="sxs-lookup"><span data-stu-id="7840b-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Component\_Shared</span></span>
</dt> <dd>

<span data-ttu-id="7840b-125">Внешний ключ в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="7840b-125">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="7840b-126">Компонент, содержащий общий файл, обычно DLL.</span><span class="sxs-lookup"><span data-stu-id="7840b-126">The component that contains the shared file, usually a DLL.</span></span> <span data-ttu-id="7840b-127">Библиотека DLL должна быть файлом ключа для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="7840b-127">The DLL should be the key file for this component.</span></span> <span data-ttu-id="7840b-128">Это должен быть компонент, отличный от того, который указан в \_ столбце приложение-компонент.</span><span class="sxs-lookup"><span data-stu-id="7840b-128">This must be a different component than listed in the Component\_Application column.</span></span>

<span data-ttu-id="7840b-129">Общий компонент управляет регистрацией для всех изолированных копий компонента и должен быть установлен флаг **мсидбкомпонентаттрибутесшареддллрефкаунт** в столбце Attributes таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="7840b-129">The shared component controls the registration for all the isolated copies of the component and must have the **msidbComponentAttributesSharedDllRefCount** flag set in the Attributes column of the Component table.</span></span> <span data-ttu-id="7840b-130">Это гарантирует, что установщик сможет управлять жизненным циклом общего компонента.</span><span class="sxs-lookup"><span data-stu-id="7840b-130">This ensures that the installer can manage the life of the shared component.</span></span>

</dd> <dt>

<span data-ttu-id="7840b-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>\_Приложение компонента</span><span class="sxs-lookup"><span data-stu-id="7840b-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Component\_Application</span></span>
</dt> <dd>

<span data-ttu-id="7840b-132">Внешний ключ в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="7840b-132">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="7840b-133">Компонент, содержащий exe, который загружает общий файл.</span><span class="sxs-lookup"><span data-stu-id="7840b-133">The component that contains the .exe which loads the shared file.</span></span> <span data-ttu-id="7840b-134">Exe должен быть файлом ключа для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="7840b-134">The .exe should be the key file for this component.</span></span> <span data-ttu-id="7840b-135">Этот компонент должен отличаться от компонента, указанного в \_ общем столбце Component.</span><span class="sxs-lookup"><span data-stu-id="7840b-135">This must be a different component than listed in the Component\_Shared column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="7840b-136">Проверка</span><span class="sxs-lookup"><span data-stu-id="7840b-136">Validation</span></span>

<dl>

[<span data-ttu-id="7840b-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="7840b-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7840b-138">ICE06</span><span class="sxs-lookup"><span data-stu-id="7840b-138">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7840b-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="7840b-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="7840b-140">ICE62</span><span class="sxs-lookup"><span data-stu-id="7840b-140">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="7840b-141">ICE66</span><span class="sxs-lookup"><span data-stu-id="7840b-141">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="7840b-142">ICE97</span><span class="sxs-lookup"><span data-stu-id="7840b-142">ICE97</span></span>](ice97.md)  
</dl>

 

 



