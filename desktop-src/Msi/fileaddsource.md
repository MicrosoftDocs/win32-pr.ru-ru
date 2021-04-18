---
description: Значение свойства ФИЛЕАДДСАУРЦЕ указывает список файловых ключей, разделенных запятыми, которые должны быть установлены для запуска с исходного носителя.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: ФИЛЕАДДСАУРЦЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b99ea1d9f4d6e212b74d6c4ee54655dce98c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685128"
---
# <a name="fileaddsource-property"></a><span data-ttu-id="59ee2-103">ФИЛЕАДДСАУРЦЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="59ee2-103">FILEADDSOURCE property</span></span>

<span data-ttu-id="59ee2-104">Значение свойства **филеаддсаурце** указывает список файловых ключей, разделенных запятыми, которые должны быть установлены для запуска с исходного носителя.</span><span class="sxs-lookup"><span data-stu-id="59ee2-104">The value of the **FILEADDSOURCE** property denotes a list of file keys delimited by commas that are to be installed to run from the source media.</span></span> <span data-ttu-id="59ee2-105">Для каждого ключа файла в списке установщик определяет компонент, который управляет этим файлом, затем проверяет все компоненты, связанные с этим компонентом, с помощью таблицы [феатурекомпонентс](featurecomponents-table.md) и устанавливает компонент, требующий наименьшего объема дискового пространства.</span><span class="sxs-lookup"><span data-stu-id="59ee2-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="59ee2-106">Ключи файлов в списке должны присутствовать в столбце File таблицы [File](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="59ee2-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="59ee2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59ee2-107">Remarks</span></span>

<span data-ttu-id="59ee2-108">Обратите внимание, что в именах ключей файлов учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="59ee2-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="59ee2-109">Также обратите внимание, что если флаг LocalOnly bit установлен в столбце Attributes таблицы [Component](component-table.md) компонента, то компонент устанавливается для локального запуска.</span><span class="sxs-lookup"><span data-stu-id="59ee2-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="59ee2-110">Установщик всегда вычисляет следующие свойства в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="59ee2-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="59ee2-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="59ee2-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="59ee2-112">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="59ee2-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="59ee2-113">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="59ee2-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="59ee2-114">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="59ee2-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="59ee2-115">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="59ee2-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="59ee2-116">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="59ee2-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="59ee2-117">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="59ee2-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="59ee2-118">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="59ee2-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="59ee2-119">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="59ee2-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="59ee2-120">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="59ee2-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. <span data-ttu-id="59ee2-121">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="59ee2-121">**FILEADDSOURCE**</span></span>
12. [<span data-ttu-id="59ee2-122">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="59ee2-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="59ee2-123">Например, если Командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, все эти функции сначала устанавливаются в local, а затем Мифеатуре — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="59ee2-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="59ee2-124">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый Мифеатуре устанавливается в local, а затем при вычислении АДДСАУРЦЕ = ALL все функции (включая Мифеатуре) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="59ee2-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="59ee2-125">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или при указании любого из указанных выше свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="59ee2-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ee2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="59ee2-126">Requirements</span></span>



| <span data-ttu-id="59ee2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="59ee2-127">Requirement</span></span> | <span data-ttu-id="59ee2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="59ee2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ee2-129">Версия</span><span class="sxs-lookup"><span data-stu-id="59ee2-129">Version</span></span><br/> | <span data-ttu-id="59ee2-130">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="59ee2-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="59ee2-131">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="59ee2-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="59ee2-132">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="59ee2-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="59ee2-133">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="59ee2-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59ee2-134">См. также</span><span class="sxs-lookup"><span data-stu-id="59ee2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59ee2-135">Свойства</span><span class="sxs-lookup"><span data-stu-id="59ee2-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




