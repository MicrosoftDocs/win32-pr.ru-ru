---
description: Значение свойства АДДСАУРЦЕ представляет собой список компонентов, разделенных запятыми и устанавливаемых для запуска из источника.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: АДДСАУРЦЕ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669464"
---
# <a name="addsource-property"></a><span data-ttu-id="01591-103">АДДСАУРЦЕ, свойство</span><span class="sxs-lookup"><span data-stu-id="01591-103">ADDSOURCE property</span></span>

<span data-ttu-id="01591-104">Значение свойства **аддсаурце** представляет собой список компонентов, разделенных запятыми и устанавливаемых для запуска из источника.</span><span class="sxs-lookup"><span data-stu-id="01591-104">The value of the **ADDSOURCE** property is a list of features that are delimited by commas, and are to be installed to run from the source.</span></span> <span data-ttu-id="01591-105">Функции должны присутствовать в столбце Feature [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="01591-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="01591-106">Чтобы установить все компоненты как запускаемые из источника, используйте АДДСАУРЦЕ = ALL в командной строке.</span><span class="sxs-lookup"><span data-stu-id="01591-106">To install all features as run from source, use ADDSOURCE=ALL on the command line.</span></span> <span data-ttu-id="01591-107">Не вводите АДДСАУРЦЕ = ALL в [таблицу свойств](property-table.md), так как при этом создается пакет с запуском из источника, который не может быть корректно удален.</span><span class="sxs-lookup"><span data-stu-id="01591-107">Do not enter ADDSOURCE=ALL into the [Property Table](property-table.md), because this generates a run-from-source package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="01591-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01591-108">Remarks</span></span>

<span data-ttu-id="01591-109">В именах функций учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="01591-109">The feature names are case sensitive.</span></span> <span data-ttu-id="01591-110">Если флаг bit LocalOnly установлен в столбце Attributes [таблицы Component](component-table.md) компонента для компонента в списке, этот компонент устанавливается для локального запуска.</span><span class="sxs-lookup"><span data-stu-id="01591-110">If the LocalOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed to run locally.</span></span>

<span data-ttu-id="01591-111">Установщик всегда вычисляет следующие свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="01591-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="01591-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="01591-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="01591-113">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="01591-113">**REMOVE**</span></span>](remove.md)
3.  <span data-ttu-id="01591-114">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="01591-114">**ADDSOURCE**</span></span>
4.  [<span data-ttu-id="01591-115">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="01591-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="01591-116">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="01591-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="01591-117">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="01591-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="01591-118">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="01591-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="01591-119">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="01591-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="01591-120">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="01591-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="01591-121">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="01591-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="01591-122">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="01591-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="01591-123">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="01591-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="01591-124">Пример:</span><span class="sxs-lookup"><span data-stu-id="01591-124">For example:</span></span>

-   <span data-ttu-id="01591-125">Если командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = **мифеатуре**, все функции сначала устанавливаются в локальный режим, а затем **мифеатуре** — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="01591-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="01591-126">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL =**мифеатуре**, то первый **мифеатуре** устанавливается в local, а затем при вычислении аддсаурце = ALL все функции (включая **мифеатуре**) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="01591-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="01591-127">Установщик задает для предварительно [**выбранных**](preselected.md) свойств значение "1" во время возобновления приостановленной установки или если в командной строке указано любое из указанных выше свойств.</span><span class="sxs-lookup"><span data-stu-id="01591-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="01591-128">Требования</span><span class="sxs-lookup"><span data-stu-id="01591-128">Requirements</span></span>



| <span data-ttu-id="01591-129">Требование</span><span class="sxs-lookup"><span data-stu-id="01591-129">Requirement</span></span> | <span data-ttu-id="01591-130">Значение</span><span class="sxs-lookup"><span data-stu-id="01591-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01591-131">Версия</span><span class="sxs-lookup"><span data-stu-id="01591-131">Version</span></span><br/> | <span data-ttu-id="01591-132">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="01591-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="01591-133">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="01591-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="01591-134">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="01591-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="01591-135">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="01591-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01591-136">См. также</span><span class="sxs-lookup"><span data-stu-id="01591-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01591-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="01591-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




