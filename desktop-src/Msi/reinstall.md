---
description: Значение свойства переустановки представляет собой список функций, разделенных запятыми, которые необходимо переустановить. Перечисленные компоненты должны присутствовать в столбце Feature таблицы Features. Чтобы переустановить все компоненты, используйте команду REINSTALL = ALL в командной строке.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: Переустановить свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651932"
---
# <a name="reinstall-property"></a><span data-ttu-id="52be3-105">Переустановить свойство</span><span class="sxs-lookup"><span data-stu-id="52be3-105">REINSTALL property</span></span>

<span data-ttu-id="52be3-106">Значение свойства **переустановки** представляет собой список функций, разделенных запятыми, которые необходимо переустановить.</span><span class="sxs-lookup"><span data-stu-id="52be3-106">The value of the **REINSTALL** property is a list of features delimited by commas that are to be reinstalled.</span></span> <span data-ttu-id="52be3-107">Перечисленные компоненты должны присутствовать в столбце Feature таблицы [Features](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="52be3-107">The features listed must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="52be3-108">Чтобы переустановить все компоненты, используйте команду REINSTALL = ALL в командной строке.</span><span class="sxs-lookup"><span data-stu-id="52be3-108">To reinstall all features use REINSTALL=ALL on the command line.</span></span>

## <a name="remarks"></a><span data-ttu-id="52be3-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="52be3-109">Remarks</span></span>

<span data-ttu-id="52be3-110">Обратите внимание, что в именах функций учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="52be3-110">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="52be3-111">Если задано свойство **REINSTALL** , необходимо также задать свойство [**REINSTALLMODE**](reinstallmode.md) , чтобы указать тип переустанавливаемой переустановки.</span><span class="sxs-lookup"><span data-stu-id="52be3-111">If the **REINSTALL** property is set, the [**REINSTALLMODE**](reinstallmode.md) property should also be set, to indicate the type of reinstall to be performed.</span></span> <span data-ttu-id="52be3-112">Если свойство **REINSTALLMODE** не задано, то по умолчанию все файлы, установленные в настоящий момент, переустанавливаются, если текущий установленный файл является меньшей версией (или не имеется).</span><span class="sxs-lookup"><span data-stu-id="52be3-112">If the **REINSTALLMODE** property is not set, then by default all files that are currently installed are reinstalled, IF the currently installed file is a lesser version (or is not present).</span></span> <span data-ttu-id="52be3-113">По умолчанию записи реестра не перезаписываются.</span><span class="sxs-lookup"><span data-stu-id="52be3-113">By default, no registry entries are rewritten.</span></span>

<span data-ttu-id="52be3-114">Обратите внимание, что даже если для **переустановки** задано значение ALL, переустанавливаются только те компоненты, которые уже были установлены ранее.</span><span class="sxs-lookup"><span data-stu-id="52be3-114">Note that even if **REINSTALL** is set to ALL, only those features that were already installed previously are reinstalled.</span></span> <span data-ttu-id="52be3-115">Таким словами, если **Переустановка** настроена для продукта, который еще не установлен, никакие действия по установке не будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="52be3-115">Thus, if **REINSTALL** is set for a product that is yet to be installed, no installation action will take place at all.</span></span>

<span data-ttu-id="52be3-116">Установщик всегда вычисляет следующие свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="52be3-116">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="52be3-117">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="52be3-117">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="52be3-118">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="52be3-118">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="52be3-119">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="52be3-119">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="52be3-120">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="52be3-120">**ADDDEFAULT**</span></span>](adddefault.md)
5.  <span data-ttu-id="52be3-121">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="52be3-121">**REINSTALL**</span></span>
6.  [<span data-ttu-id="52be3-122">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="52be3-122">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="52be3-123">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="52be3-123">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="52be3-124">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="52be3-124">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="52be3-125">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="52be3-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
10. [<span data-ttu-id="52be3-126">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="52be3-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
11. [<span data-ttu-id="52be3-127">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="52be3-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="52be3-128">Например, если Командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, все эти функции сначала устанавливаются в local, а затем Мифеатуре — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="52be3-128">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="52be3-129">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый Мифеатуре устанавливается в local, а затем при вычислении АДДСАУРЦЕ = ALL все функции (включая Мифеатуре) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="52be3-129">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="52be3-130">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или при указании любого из указанных выше свойств в командной строке.</span><span class="sxs-lookup"><span data-stu-id="52be3-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="52be3-131">Требования</span><span class="sxs-lookup"><span data-stu-id="52be3-131">Requirements</span></span>



| <span data-ttu-id="52be3-132">Требование</span><span class="sxs-lookup"><span data-stu-id="52be3-132">Requirement</span></span> | <span data-ttu-id="52be3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="52be3-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52be3-134">Версия</span><span class="sxs-lookup"><span data-stu-id="52be3-134">Version</span></span><br/> | <span data-ttu-id="52be3-135">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="52be3-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="52be3-136">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="52be3-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="52be3-137">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="52be3-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="52be3-138">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="52be3-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52be3-139">См. также</span><span class="sxs-lookup"><span data-stu-id="52be3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52be3-140">Свойства</span><span class="sxs-lookup"><span data-stu-id="52be3-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




