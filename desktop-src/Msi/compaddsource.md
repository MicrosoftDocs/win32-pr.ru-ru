---
description: Значение свойства КОМПАДДСАУРЦЕ представляет собой список идентификаторов GUID компонента из столбца ComponentId таблицы Component, разделенных запятыми, которые должны быть установлены для запуска с исходного носителя.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: КОМПАДДСАУРЦЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651802"
---
# <a name="compaddsource-property"></a><span data-ttu-id="df9c6-103">КОМПАДДСАУРЦЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="df9c6-103">COMPADDSOURCE property</span></span>

<span data-ttu-id="df9c6-104">Значение свойства **компаддсаурце** представляет собой список идентификаторов GUID компонента из столбца ComponentID таблицы [Component](component-table.md) , разделенных запятыми, которые должны быть установлены для запуска с исходного носителя.</span><span class="sxs-lookup"><span data-stu-id="df9c6-104">The value of the **COMPADDSOURCE** property is a list of component GUIDs from the ComponentId column of the [Component](component-table.md) table, delimited by commas, that are to be installed to run from the source media.</span></span> <span data-ttu-id="df9c6-105">Установщик использует это значение, чтобы определить, какие компоненты установлены для запуска из источника на основе указанных компонентов.</span><span class="sxs-lookup"><span data-stu-id="df9c6-105">The installer uses this value to determine which features are set to be installed to run from source, based on the specified components.</span></span> <span data-ttu-id="df9c6-106">Для каждого идентификатора компонента установщик проверяет все компоненты, связанные (через таблицу [феатурекомпонентс](featurecomponents-table.md) ), и устанавливает компонент, для установки которого требуется минимальный объем дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="df9c6-106">For each listed component ID, the installer examines all features linked (through the [FeatureComponents](featurecomponents-table.md) table) to that component, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="df9c6-107">Перечисленные компоненты должны присутствовать в столбце Component таблицы [Component](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="df9c6-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="df9c6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df9c6-108">Remarks</span></span>

<span data-ttu-id="df9c6-109">Обратите внимание, что в именах компонентов учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="df9c6-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="df9c6-110">Также обратите внимание, что если флаг LocalOnly bit установлен в столбце Attributes таблицы [Component](component-table.md) компонента, то компонент устанавливается для локального запуска.</span><span class="sxs-lookup"><span data-stu-id="df9c6-110">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="df9c6-111">Установщик всегда вычисляет следующие свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="df9c6-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="df9c6-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="df9c6-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="df9c6-113">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="df9c6-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="df9c6-114">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="df9c6-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="df9c6-115">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="df9c6-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="df9c6-116">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="df9c6-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="df9c6-117">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="df9c6-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="df9c6-118">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="df9c6-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  <span data-ttu-id="df9c6-119">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="df9c6-119">**COMPADDSOURCE**</span></span>
9.  [<span data-ttu-id="df9c6-120">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="df9c6-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="df9c6-121">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="df9c6-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="df9c6-122">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="df9c6-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="df9c6-123">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="df9c6-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="df9c6-124">Например, если Командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, все эти функции сначала устанавливаются в local, а затем Мифеатуре — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="df9c6-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="df9c6-125">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый Мифеатуре устанавливается в local, а затем при вычислении АДДСАУРЦЕ = ALL все функции (включая Мифеатуре) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="df9c6-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="df9c6-126">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или при указании любого из указанных выше свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="df9c6-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="df9c6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="df9c6-127">Requirements</span></span>



| <span data-ttu-id="df9c6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="df9c6-128">Requirement</span></span> | <span data-ttu-id="df9c6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="df9c6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df9c6-130">Версия</span><span class="sxs-lookup"><span data-stu-id="df9c6-130">Version</span></span><br/> | <span data-ttu-id="df9c6-131">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df9c6-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="df9c6-132">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df9c6-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="df9c6-133">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="df9c6-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="df9c6-134">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="df9c6-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df9c6-135">См. также</span><span class="sxs-lookup"><span data-stu-id="df9c6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9c6-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="df9c6-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




