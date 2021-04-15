---
description: Значение свойства АДДДЕФАУЛТ представляет собой список функций, разделенных запятыми, которые должны быть установлены в конфигурации по умолчанию.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: АДДДЕФАУЛТ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651720"
---
# <a name="adddefault-property"></a><span data-ttu-id="d3d49-103">АДДДЕФАУЛТ, свойство</span><span class="sxs-lookup"><span data-stu-id="d3d49-103">ADDDEFAULT property</span></span>

<span data-ttu-id="d3d49-104">Значение свойства **адддефаулт** представляет собой список функций, разделенных запятыми, которые должны быть установлены в конфигурации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3d49-104">The value of the **ADDDEFAULT** property is a list of features delimited by commas, which are to be installed in their default configuration.</span></span> <span data-ttu-id="d3d49-105">Функции должны присутствовать в столбце Feature [таблицы Feature.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="d3d49-105">The features must be present in the Feature column of the [Feature Table.](feature-table.md)</span></span> <span data-ttu-id="d3d49-106">Чтобы установить все компоненты в конфигурации по умолчанию, используйте АДДДЕФАУЛТ = ALL в командной строке.</span><span class="sxs-lookup"><span data-stu-id="d3d49-106">To install all features in their default configurations, use ADDDEFAULT=ALL on the command line.</span></span>

<span data-ttu-id="d3d49-107">Функция, указанная в свойстве **адддефаулт** , устанавливается в том же состоянии установки, что и если пользователь запросил установку компонента по запросу.</span><span class="sxs-lookup"><span data-stu-id="d3d49-107">A feature listed in the **ADDDEFAULT** property is installed in the same installation state as if the user requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="d3d49-108">Состояние определяется битами, заданными для функции в столбце Attributes [таблицы Feature](feature-table.md), и какие биты задаются для компонентов компонента в столбце Attributes [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d3d49-108">The state is determined by the bits that are set for the feature in the Attributes column of the [Feature Table](feature-table.md), and which bits are set for the feature components in the Attributes column of the [Component Table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3d49-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3d49-109">Remarks</span></span>

<span data-ttu-id="d3d49-110">В именах функций учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="d3d49-110">The feature names are case sensitive.</span></span>

<span data-ttu-id="d3d49-111">Установщик всегда вычисляет следующие свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d3d49-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="d3d49-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d3d49-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="d3d49-113">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="d3d49-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="d3d49-114">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="d3d49-114">**ADDSOURCE**</span></span>](addsource.md)
4.  <span data-ttu-id="d3d49-115">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="d3d49-115">**ADDDEFAULT**</span></span>
5.  [<span data-ttu-id="d3d49-116">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="d3d49-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="d3d49-117">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="d3d49-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="d3d49-118">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="d3d49-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="d3d49-119">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="d3d49-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="d3d49-120">**компадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="d3d49-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="d3d49-121">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="d3d49-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="d3d49-122">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="d3d49-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="d3d49-123">**филеадддефаулт**</span><span class="sxs-lookup"><span data-stu-id="d3d49-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="d3d49-124">Пример:</span><span class="sxs-lookup"><span data-stu-id="d3d49-124">For example:</span></span>

-   <span data-ttu-id="d3d49-125">Если командная строка указывает: ADDLOCAL = ALL, АДДСАУРЦЕ = Мифеатуре, все функции сначала устанавливаются в локальный режим, а затем **мифеатуре** — в значение Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="d3d49-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="d3d49-126">Если командная строка имеет значение: АДДСАУРЦЕ = ALL, ADDLOCAL = Мифеатуре, то первый **мифеатуре** устанавливается в local, а затем при вычислении АДДСАУРЦЕ = ALL все функции (включая **мифеатуре**) сбрасываются в исходный код.</span><span class="sxs-lookup"><span data-stu-id="d3d49-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="d3d49-127">Установщик задает для предварительно [**выбранных**](preselected.md) свойств значение "1" во время возобновления приостановленной установки или если в командной строке указано любое из указанных выше свойств.</span><span class="sxs-lookup"><span data-stu-id="d3d49-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d49-128">Требования</span><span class="sxs-lookup"><span data-stu-id="d3d49-128">Requirements</span></span>



| <span data-ttu-id="d3d49-129">Требование</span><span class="sxs-lookup"><span data-stu-id="d3d49-129">Requirement</span></span> | <span data-ttu-id="d3d49-130">Значение</span><span class="sxs-lookup"><span data-stu-id="d3d49-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d49-131">Версия</span><span class="sxs-lookup"><span data-stu-id="d3d49-131">Version</span></span><br/> | <span data-ttu-id="d3d49-132">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d3d49-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d3d49-133">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d3d49-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d3d49-134">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d3d49-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d3d49-135">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d49-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d3d49-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d3d49-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d49-137">Свойства</span><span class="sxs-lookup"><span data-stu-id="d3d49-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




