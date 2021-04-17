---
description: Установщик задает для свойства Аутофнорбдискспаце значение true, если на любом томе, который является целью установки, недостаточно места на диске для размещения установки.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Аутофнорбдискспаце, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652071"
---
# <a name="outofnorbdiskspace-property"></a><span data-ttu-id="7a183-103">Аутофнорбдискспаце, свойство</span><span class="sxs-lookup"><span data-stu-id="7a183-103">OutOfNoRbDiskSpace property</span></span>

<span data-ttu-id="7a183-104">Установщик задает для свойства **Аутофнорбдискспаце** значение true, если на любом томе, который является целью установки, недостаточно места на диске для размещения установки.</span><span class="sxs-lookup"><span data-stu-id="7a183-104">The installer sets the **OutOfNoRbDiskSpace** property to True if any volume that is a target of the installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="7a183-105">В этом случае свойство **аутофнорбдискспаце** имеет значение true, даже если функция отката была отключена.</span><span class="sxs-lookup"><span data-stu-id="7a183-105">In this case, the **OutOfNoRbDiskSpace** property is set to True even if rollback has been disabled.</span></span> <span data-ttu-id="7a183-106">Если на всех томах достаточно свободного места, значение равно false.</span><span class="sxs-lookup"><span data-stu-id="7a183-106">If all volumes have sufficient space, the value is False.</span></span>

<span data-ttu-id="7a183-107">Разработчик пакета установки может решить ситуацию, когда свойство [**аутофдискспаце**](outofdiskspace.md) имеет значение true, а свойство **аутофнорбдискспаце** — false путем создания пользовательского интерфейса, предоставляющего пользователю возможность отключить откат и продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="7a183-107">A developer of an installation package can handle the situation when the [**OutOfDiskSpace**](outofdiskspace.md) property is True and the **OutOfNoRbDiskSpace** property is False by authoring a user interface that presents the user with an option to disable rollback and continue the installation.</span></span> <span data-ttu-id="7a183-108">Сведения о условном отображении диалогового окна см. в разделе [таблице ControlEvent событие Overview](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7a183-108">For information about conditionally displaying a dialog box, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="7a183-109">Дополнительные сведения об отключении отката см. в разделе [Енаблероллбакк таблице ControlEvent событие](enablerollback-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="7a183-109">For information about disabling rollback, see [EnableRollback ControlEvent](enablerollback-controlevent.md).</span></span>

<span data-ttu-id="7a183-110">Свойство **аутофнорбдискспаце** является допустимым в любой момент после выполнения [действия костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="7a183-110">The **OutOfNoRbDiskSpace** property is valid at any time after the [CostFinalize action](costfinalize-action.md) has been executed.</span></span> <span data-ttu-id="7a183-111">Состояние свойства **аутофнорбдискспаце** динамически обновляется каждый раз, когда общая стоимость установки пересчитывается (например, при каждом изменении состояния установки любой из компонентов с помощью [диалогового окна выбора](selection-dialog.md)).</span><span class="sxs-lookup"><span data-stu-id="7a183-111">The **OutOfNoRbDiskSpace** property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection dialog](selection-dialog.md)).</span></span> <span data-ttu-id="7a183-112">Действия по разрешению выбора используйте это значение для отмены установки и создания диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7a183-112">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a183-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7a183-113">Requirements</span></span>



| <span data-ttu-id="7a183-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7a183-114">Requirement</span></span> | <span data-ttu-id="7a183-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7a183-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a183-116">Версия</span><span class="sxs-lookup"><span data-stu-id="7a183-116">Version</span></span><br/> | <span data-ttu-id="7a183-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7a183-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7a183-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7a183-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7a183-119">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7a183-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7a183-120">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="7a183-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a183-121">См. также</span><span class="sxs-lookup"><span data-stu-id="7a183-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a183-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a183-122">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="7a183-123">Обзор таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="7a183-123">ControlEvent Overview</span></span>](controlevent-overview.md)
</dt> <dt>

[<span data-ttu-id="7a183-124">**Аутофдискспаце, свойство**</span><span class="sxs-lookup"><span data-stu-id="7a183-124">**OutOfDiskSpace property**</span></span>](outofdiskspace.md)
</dt> <dt>

[<span data-ttu-id="7a183-125">Енаблероллбакк таблице ControlEvent событие</span><span class="sxs-lookup"><span data-stu-id="7a183-125">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)
</dt> <dt>

[<span data-ttu-id="7a183-126">Действие Костфинализе</span><span class="sxs-lookup"><span data-stu-id="7a183-126">CostFinalize action</span></span>](costfinalize-action.md)
</dt> <dt>

[<span data-ttu-id="7a183-127">Диалоговое окно выбора</span><span class="sxs-lookup"><span data-stu-id="7a183-127">Selection dialog</span></span>](selection-dialog.md)
</dt> </dl>

 

 




