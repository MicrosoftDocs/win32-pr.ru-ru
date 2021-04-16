---
description: Значением свойства ADDLOCAL является список компонентов, разделенных запятыми и устанавливаемых локально.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: Свойство ADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669466"
---
# <a name="addlocal-property"></a><span data-ttu-id="64ded-103">Свойство ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="64ded-103">ADDLOCAL property</span></span>

<span data-ttu-id="64ded-104">Значением свойства **ADDLOCAL** является список компонентов, разделенных запятыми и устанавливаемых локально.</span><span class="sxs-lookup"><span data-stu-id="64ded-104">The value of the **ADDLOCAL** property is a list of features that are delimited by commas, and are to be installed locally.</span></span> <span data-ttu-id="64ded-105">Функции должны присутствовать в столбце Feature [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="64ded-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="64ded-106">Чтобы установить все компоненты локально, используйте параметр ADDLOCAL = ALL в командной строке.</span><span class="sxs-lookup"><span data-stu-id="64ded-106">To install all features locally, use ADDLOCAL=ALL on the command line.</span></span> <span data-ttu-id="64ded-107">Не вводите параметр ADDLOCAL = ALL в [таблицу свойств](property-table.md), так как при этом создается локально установленный пакет, который невозможно правильно удалить.</span><span class="sxs-lookup"><span data-stu-id="64ded-107">Do not enter ADDLOCAL=ALL into the [Property Table](property-table.md), because this generates a locally installed package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="64ded-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64ded-108">Remarks</span></span>

<span data-ttu-id="64ded-109">В именах компонентов учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="64ded-109">Feature names are case sensitive.</span></span> <span data-ttu-id="64ded-110">Если флаг bit Саурцеонли установлен в столбце Attributes [таблицы Component](component-table.md) компонента для компонента в списке, этот компонент устанавливается как запуск из источника.</span><span class="sxs-lookup"><span data-stu-id="64ded-110">If the SourceOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed as run from source.</span></span>

<span data-ttu-id="64ded-111">Установщик всегда вычисляет следующие свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="64ded-111">The installer always evaluates the following properties in the following order:</span></span>

1.  <span data-ttu-id="64ded-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="64ded-112">**ADDLOCAL**</span></span>
2.  [<span data-ttu-id="64ded-113">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="64ded-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="64ded-114">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="64ded-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="64ded-115">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="64ded-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="64ded-116">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="64ded-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="64ded-117">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="64ded-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="64ded-118">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="64ded-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="64ded-119">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="64ded-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="64ded-120">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="64ded-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="64ded-121">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="64ded-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="64ded-122">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="64ded-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="64ded-123">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="64ded-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="64ded-124">Пример:</span><span class="sxs-lookup"><span data-stu-id="64ded-124">For example:</span></span>

-   <span data-ttu-id="64ded-125">Если командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = **мифеатуре**, все функции сначала устанавливаются в локальный режим, а затем **мифеатуре** — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="64ded-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="64ded-126">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL =**мифеатуре**, то первый **мифеатуре** устанавливается в local, а затем при вычислении аддсаурце = ALL все функции (включая **мифеатуре**) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="64ded-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="64ded-127">Установщик задает для свойства предварительно [**выбранных**](preselected.md) значений значение "1" во время возобновления приостановленной установки или если в командной строке указаны какие-либо из предыдущих свойств.</span><span class="sxs-lookup"><span data-stu-id="64ded-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the previous properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="64ded-128">Требования</span><span class="sxs-lookup"><span data-stu-id="64ded-128">Requirements</span></span>



| <span data-ttu-id="64ded-129">Требование</span><span class="sxs-lookup"><span data-stu-id="64ded-129">Requirement</span></span> | <span data-ttu-id="64ded-130">Значение</span><span class="sxs-lookup"><span data-stu-id="64ded-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64ded-131">Версия</span><span class="sxs-lookup"><span data-stu-id="64ded-131">Version</span></span><br/> | <span data-ttu-id="64ded-132">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64ded-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="64ded-133">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64ded-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="64ded-134">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="64ded-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="64ded-135">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="64ded-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="64ded-136">См. также</span><span class="sxs-lookup"><span data-stu-id="64ded-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64ded-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="64ded-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




