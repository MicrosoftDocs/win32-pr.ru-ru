---
description: Значение свойства КОМПАДДДЕФАУЛТ представляет собой список идентификаторов GUID компонента из столбца ComponentId таблицы Component, разделенных запятыми, которые устанавливаются в их конфигурации по умолчанию.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: КОМПАДДДЕФАУЛТ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651803"
---
# <a name="compadddefault-property"></a><span data-ttu-id="a8083-103">КОМПАДДДЕФАУЛТ, свойство</span><span class="sxs-lookup"><span data-stu-id="a8083-103">COMPADDDEFAULT property</span></span>

<span data-ttu-id="a8083-104">Значение свойства **компадддефаулт** представляет собой список идентификаторов GUID компонента из столбца ComponentID [таблицы Component](component-table.md), разделенных запятыми, которые устанавливаются в их конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8083-104">The value of the **COMPADDDEFAULT** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are installed in their default configuration.</span></span> <span data-ttu-id="a8083-105">Для каждого идентификатора компонента в списке установщик устанавливает компонент, требующий наименьшего места на диске.</span><span class="sxs-lookup"><span data-stu-id="a8083-105">For each component ID in the list, the installer installs the feature that requires the least disk space.</span></span> <span data-ttu-id="a8083-106">Идентификаторы компонентов в списке должны присутствовать в столбце ComponentId [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a8083-106">The component IDs in the list must be present in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="a8083-107">Компонент устанавливается в том же состоянии установки, что и если пользователь запросил установку по запросу этой функции.</span><span class="sxs-lookup"><span data-stu-id="a8083-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="a8083-108">Состояние определяется тем, какие биты задаются для функции в столбце Attributes [таблицы Feature](feature-table.md), а какие биты задаются для компонентов компонента в столбце Attributes таблицы Component.</span><span class="sxs-lookup"><span data-stu-id="a8083-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8083-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8083-109">Remarks</span></span>

<span data-ttu-id="a8083-110">Обратите внимание, что если флаг Саурцеонли bit задан в столбце Attributes таблицы [Component](component-table.md) компонента, то компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="a8083-110">Note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="a8083-111">Установщик всегда вычисляет следующие свойства в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="a8083-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="a8083-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a8083-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="a8083-113">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="a8083-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="a8083-114">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="a8083-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="a8083-115">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="a8083-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="a8083-116">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="a8083-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="a8083-117">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="a8083-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="a8083-118">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="a8083-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="a8083-119">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="a8083-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  <span data-ttu-id="a8083-120">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="a8083-120">**COMPADDDEFAULT**</span></span>
10. [<span data-ttu-id="a8083-121">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="a8083-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="a8083-122">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="a8083-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="a8083-123">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="a8083-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="a8083-124">Например, если Командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, все эти функции сначала устанавливаются в local, а затем Мифеатуре — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="a8083-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="a8083-125">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый Мифеатуре устанавливается в local, а затем при вычислении АДДСАУРЦЕ = ALL все функции (включая Мифеатуре) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="a8083-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="a8083-126">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или при указании любого из указанных выше свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="a8083-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8083-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a8083-127">Requirements</span></span>



| <span data-ttu-id="a8083-128">Требование</span><span class="sxs-lookup"><span data-stu-id="a8083-128">Requirement</span></span> | <span data-ttu-id="a8083-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a8083-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8083-130">Версия</span><span class="sxs-lookup"><span data-stu-id="a8083-130">Version</span></span><br/> | <span data-ttu-id="a8083-131">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8083-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a8083-132">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8083-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a8083-133">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8083-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a8083-134">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a8083-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8083-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a8083-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8083-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8083-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




