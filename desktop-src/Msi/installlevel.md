---
description: Свойство ИНСТАЛЛЛЕВЕЛ — это начальный уровень, на котором функции выбираются &\# 0034; в&\# 0034; для установки по умолчанию.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: ИНСТАЛЛЛЕВЕЛ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688879"
---
# <a name="installlevel-property"></a><span data-ttu-id="fd13e-103">ИНСТАЛЛЛЕВЕЛ, свойство</span><span class="sxs-lookup"><span data-stu-id="fd13e-103">INSTALLLEVEL property</span></span>

<span data-ttu-id="fd13e-104">Свойство **инсталллевел** — это начальный уровень, при котором функции выбираются по умолчанию для установки.</span><span class="sxs-lookup"><span data-stu-id="fd13e-104">The **INSTALLLEVEL** property is the initial level at which features are selected "ON" for installation by default.</span></span> <span data-ttu-id="fd13e-105">Компонент устанавливается, только если значение в поле Level [таблицы Feature](feature-table.md) меньше или равно текущему значению инсталллевел.</span><span class="sxs-lookup"><span data-stu-id="fd13e-105">A feature is installed only if the value in the Level field of the [Feature table](feature-table.md) is less than or equal to the current INSTALLLEVEL value.</span></span> <span data-ttu-id="fd13e-106">Уровень установки для любой установки определяется свойством **инсталллевел** и может быть целым, от 1 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="fd13e-106">The installation level for any installation is specified by the **INSTALLLEVEL** property, and can be an integral from 1 to 32,767.</span></span> <span data-ttu-id="fd13e-107">Дополнительные сведения об уровнях установки см. в статье [Таблица функций](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="fd13e-107">For further discussion of installation levels, see [Feature Table](feature-table.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="fd13e-108">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="fd13e-108">Default Value</span></span>

<span data-ttu-id="fd13e-109">Если значение не указано, по умолчанию устанавливается уровень 1.</span><span class="sxs-lookup"><span data-stu-id="fd13e-109">If no value is specified, the install level defaults to 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd13e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd13e-110">Remarks</span></span>

<span data-ttu-id="fd13e-111">Уровень установки, заданный свойством **инсталллевел** , может быть переопределен следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="fd13e-111">The installation level specified by the **INSTALLLEVEL** property can be overridden by the following properties:</span></span>

-   [<span data-ttu-id="fd13e-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="fd13e-112">**ADDLOCAL**</span></span>](addlocal.md)
-   [<span data-ttu-id="fd13e-113">**аддсаурце**</span><span class="sxs-lookup"><span data-stu-id="fd13e-113">**ADDSOURCE**</span></span>](addsource.md)
-   [<span data-ttu-id="fd13e-114">**адддефаулт**</span><span class="sxs-lookup"><span data-stu-id="fd13e-114">**ADDDEFAULT**</span></span>](adddefault.md)
-   [<span data-ttu-id="fd13e-115">**компаддлокал**</span><span class="sxs-lookup"><span data-stu-id="fd13e-115">**COMPADDLOCAL**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="fd13e-116">**компаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="fd13e-116">**COMPADDSOURCE**</span></span>](compaddsource.md)
-   [<span data-ttu-id="fd13e-117">**филеаддлокал**</span><span class="sxs-lookup"><span data-stu-id="fd13e-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="fd13e-118">**филеаддсаурце**</span><span class="sxs-lookup"><span data-stu-id="fd13e-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="fd13e-119">**ОТМЕНИТ**</span><span class="sxs-lookup"><span data-stu-id="fd13e-119">**REMOVE**</span></span>](remove.md)
-   [<span data-ttu-id="fd13e-120">**КАКОМУ**</span><span class="sxs-lookup"><span data-stu-id="fd13e-120">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="fd13e-121">**РЕКЛАМИРОВАТЬ**</span><span class="sxs-lookup"><span data-stu-id="fd13e-121">**ADVERTISE**</span></span>](advertise.md)

<span data-ttu-id="fd13e-122">Например, при установке параметра ADDLOCAL = ALL все компоненты устанавливаются локально независимо от значения свойства **инсталллевел** .</span><span class="sxs-lookup"><span data-stu-id="fd13e-122">For example, setting ADDLOCAL=ALL installs all features locally regardless of the value of the **INSTALLLEVEL** property.</span></span> <span data-ttu-id="fd13e-123">Если значение столбца Level в [таблице Feature](feature-table.md) равно 0, эта функция не установлена и не отображается в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="fd13e-123">If the value of the Level column in the [Feature table](feature-table.md) is 0, that feature is not installed and not displayed in the UI.</span></span>

<span data-ttu-id="fd13e-124">Администратор может навсегда отключить функцию, применив преобразование настройки, которое задает значение 0 в столбце Level для этой функции.</span><span class="sxs-lookup"><span data-stu-id="fd13e-124">An administrator can permanently disable a feature by applying a customization transform that sets a 0 in the Level column for that feature.</span></span> <span data-ttu-id="fd13e-125">Применение преобразования настройки предотвращает установку и отображение компонента, даже если пользователь выбирает полную установку с помощью пользовательского интерфейса или устанавливает параметр ADDLOCAL в значение ALL в командной строке.</span><span class="sxs-lookup"><span data-stu-id="fd13e-125">The application of the customization transform prevents the installation and display of the feature even if the user selects a complete installation using the UI or by setting ADDLOCAL to ALL on the command line.</span></span> <span data-ttu-id="fd13e-126">См. [Пример преобразования настройки](a-customization-transform-example.md).</span><span class="sxs-lookup"><span data-stu-id="fd13e-126">See [A Customization Transform Example](a-customization-transform-example.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd13e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="fd13e-127">Requirements</span></span>



| <span data-ttu-id="fd13e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="fd13e-128">Requirement</span></span> | <span data-ttu-id="fd13e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fd13e-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd13e-130">Версия</span><span class="sxs-lookup"><span data-stu-id="fd13e-130">Version</span></span><br/> | <span data-ttu-id="fd13e-131">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fd13e-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fd13e-132">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fd13e-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fd13e-133">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd13e-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fd13e-134">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fd13e-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd13e-135">См. также</span><span class="sxs-lookup"><span data-stu-id="fd13e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd13e-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="fd13e-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




