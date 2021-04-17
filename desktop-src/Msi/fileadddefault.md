---
description: Значение свойства ФИЛЕАДДДЕФАУЛТ представляет собой список файловых ключей, разделенных запятыми, которые устанавливаются в их конфигурации по умолчанию.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: ФИЛЕАДДДЕФАУЛТ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685130"
---
# <a name="fileadddefault-property"></a><span data-ttu-id="a2300-103">ФИЛЕАДДДЕФАУЛТ, свойство</span><span class="sxs-lookup"><span data-stu-id="a2300-103">FILEADDDEFAULT property</span></span>

<span data-ttu-id="a2300-104">Значение свойства **филеадддефаулт** представляет собой список файловых ключей, разделенных запятыми, которые устанавливаются в их конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2300-104">The value of the **FILEADDDEFAULT** property is a list of file keys delimited by commas that are installed in their default configuration.</span></span> <span data-ttu-id="a2300-105">Для каждого ключа файла в списке установщик определяет компонент, который управляет этим файлом, и устанавливает компонент, требующий наименьшего места на диске.</span><span class="sxs-lookup"><span data-stu-id="a2300-105">For each file key in the list, the installer determines the component that controls that file and installs the feature that requires the least disk space.</span></span> <span data-ttu-id="a2300-106">Ключи файлов в списке должны присутствовать в столбце File таблицы [File](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="a2300-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="a2300-107">Компонент устанавливается в том же состоянии установки, что и если пользователь запросил установку по запросу этой функции.</span><span class="sxs-lookup"><span data-stu-id="a2300-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="a2300-108">Состояние определяется тем, какие биты задаются для функции в столбце Attributes [таблицы Feature](feature-table.md), а какие биты задаются для компонентов компонента в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a2300-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2300-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2300-109">Remarks</span></span>

<span data-ttu-id="a2300-110">Обратите внимание, что в именах ключей файлов учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="a2300-110">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="a2300-111">Также обратите внимание, что если флаг Саурцеонли bit установлен в столбце Attributes таблицы [Component](component-table.md) компонента, то компонент устанавливается для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="a2300-111">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="a2300-112">Установщик всегда вычисляет следующие свойства в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="a2300-112">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="a2300-113">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="a2300-113">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="a2300-114">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="a2300-114">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="a2300-115">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="a2300-115">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="a2300-116">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="a2300-116">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="a2300-117">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="a2300-117">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="a2300-118">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="a2300-118">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="a2300-119">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="a2300-119">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="a2300-120">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="a2300-120">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="a2300-121">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="a2300-121">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="a2300-122">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="a2300-122">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="a2300-123">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="a2300-123">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. <span data-ttu-id="a2300-124">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="a2300-124">**FILEADDDEFAULT**</span></span>

<span data-ttu-id="a2300-125">Например, если Командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, все эти функции сначала устанавливаются в local, а затем Мифеатуре — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="a2300-125">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="a2300-126">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый Мифеатуре устанавливается в local, а затем при вычислении АДДСАУРЦЕ = ALL все функции (включая Мифеатуре) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="a2300-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="a2300-127">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или при указании любого из указанных выше свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="a2300-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2300-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a2300-128">Requirements</span></span>



| <span data-ttu-id="a2300-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a2300-129">Requirement</span></span> | <span data-ttu-id="a2300-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a2300-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2300-131">Версия</span><span class="sxs-lookup"><span data-stu-id="a2300-131">Version</span></span><br/> | <span data-ttu-id="a2300-132">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a2300-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a2300-133">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a2300-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a2300-134">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a2300-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a2300-135">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a2300-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2300-136">См. также</span><span class="sxs-lookup"><span data-stu-id="a2300-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2300-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="a2300-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




