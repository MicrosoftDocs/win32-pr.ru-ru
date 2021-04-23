---
description: Значение свойства КОМПАДДЛОКАЛ представляет собой список идентификаторов GUID компонента из столбца ComponentId таблицы Component, разделенных запятыми, которые должны быть установлены локально.
ms.assetid: 10c178c5-1eae-4191-b79c-9285810efb6a
title: КОМПАДДЛОКАЛ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e403459f0355c28d66da00170b9c649084afbb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669462"
---
# <a name="compaddlocal-property"></a><span data-ttu-id="5bacf-103">КОМПАДДЛОКАЛ, свойство</span><span class="sxs-lookup"><span data-stu-id="5bacf-103">COMPADDLOCAL property</span></span>

<span data-ttu-id="5bacf-104">Значение свойства **компаддлокал** представляет собой список идентификаторов GUID компонента из столбца ComponentID [таблицы Component](component-table.md), разделенных запятыми, которые должны быть установлены локально.</span><span class="sxs-lookup"><span data-stu-id="5bacf-104">The value of the **COMPADDLOCAL** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are to be installed locally.</span></span> <span data-ttu-id="5bacf-105">Установщик использует этот список, чтобы определить, какие компоненты устанавливаются локально на основе указанных компонентов.</span><span class="sxs-lookup"><span data-stu-id="5bacf-105">The installer uses this list to determine which features are set to be installed locally, based on the specified components.</span></span> <span data-ttu-id="5bacf-106">Для каждого идентификатора компонента установщик проверяет все компоненты, связанные с этим компонентом, через таблицу [феатурекомпонентс](featurecomponents-table.md) и устанавливает компонент, для установки которого требуется минимальный объем дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="5bacf-106">For each listed component ID, the installer examines all features linked to that component through the [FeatureComponents](featurecomponents-table.md) table, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="5bacf-107">Перечисленные компоненты должны присутствовать в столбце Component таблицы [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5bacf-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bacf-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5bacf-108">Remarks</span></span>

<span data-ttu-id="5bacf-109">Обратите внимание, что в именах компонентов учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="5bacf-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="5bacf-110">Также обратите внимание, что если флаг Саурцеонли bit установлен в столбце Attributes таблицы [Component](component-table.md) компонента, то компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="5bacf-110">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="5bacf-111">Установщик всегда вычисляет следующие свойства в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="5bacf-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="5bacf-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="5bacf-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="5bacf-113">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="5bacf-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="5bacf-114">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="5bacf-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="5bacf-115">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="5bacf-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="5bacf-116">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="5bacf-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="5bacf-117">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="5bacf-117">**ADVERTISE**</span></span>](advertise.md)
7.  <span data-ttu-id="5bacf-118">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="5bacf-118">**COMPADDLOCAL**</span></span>
8.  [<span data-ttu-id="5bacf-119">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="5bacf-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="5bacf-120">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="5bacf-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="5bacf-121">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="5bacf-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="5bacf-122">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="5bacf-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="5bacf-123">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="5bacf-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="5bacf-124">Например, если Командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, все эти функции сначала устанавливаются в local, а затем Мифеатуре — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="5bacf-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="5bacf-125">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый Мифеатуре устанавливается в local, а затем при вычислении АДДСАУРЦЕ = ALL все функции (включая Мифеатуре) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="5bacf-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="5bacf-126">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или при указании любого из указанных выше свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="5bacf-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bacf-127">Требования</span><span class="sxs-lookup"><span data-stu-id="5bacf-127">Requirements</span></span>



| <span data-ttu-id="5bacf-128">Требование</span><span class="sxs-lookup"><span data-stu-id="5bacf-128">Requirement</span></span> | <span data-ttu-id="5bacf-129">Значение</span><span class="sxs-lookup"><span data-stu-id="5bacf-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bacf-130">Версия</span><span class="sxs-lookup"><span data-stu-id="5bacf-130">Version</span></span><br/> | <span data-ttu-id="5bacf-131">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5bacf-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5bacf-132">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5bacf-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5bacf-133">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5bacf-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5bacf-134">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5bacf-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bacf-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5bacf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bacf-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="5bacf-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




