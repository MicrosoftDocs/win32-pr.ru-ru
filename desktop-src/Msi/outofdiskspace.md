---
description: Установщик задает для свойства Аутофдискспаце значение TRUE, если на любом томе, который является целевым объектом текущей установки, недостаточно места на диске для размещения установки.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Аутофдискспаце, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675432"
---
# <a name="outofdiskspace-property"></a><span data-ttu-id="fc9cc-103">Аутофдискспаце, свойство</span><span class="sxs-lookup"><span data-stu-id="fc9cc-103">OutOfDiskSpace property</span></span>

<span data-ttu-id="fc9cc-104">Установщик задает для свойства **аутофдискспаце** значение true, если на любом томе, который является целевым объектом текущей установки, недостаточно места на диске для размещения установки.</span><span class="sxs-lookup"><span data-stu-id="fc9cc-104">The installer sets the **OutOfDiskSpace** property to TRUE if any volume that is a target of the current installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="fc9cc-105">Если на всех томах достаточно свободного места, значение равно FALSE.</span><span class="sxs-lookup"><span data-stu-id="fc9cc-105">If all volumes have sufficient space, the value is FALSE.</span></span> <span data-ttu-id="fc9cc-106">Действия по разрешению выбора используйте это значение для отмены установки и создания диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="fc9cc-106">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

<span data-ttu-id="fc9cc-107">Это свойство является допустимым в любое время после выполнения [действия костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9cc-107">This property is valid at any time after the [CostFinalize action](costfinalize-action.md) is executed.</span></span> <span data-ttu-id="fc9cc-108">Состояние свойства [**аутофнорбдискспаце**](outofnorbdiskspace.md) динамически обновляется каждый раз, когда общая стоимость установки пересчитывается (например, при каждом изменении состояния установки любой из компонентов с помощью диалогового окна [выбора](selection-dialog.md) ).</span><span class="sxs-lookup"><span data-stu-id="fc9cc-108">The [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection](selection-dialog.md) dialog).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc9cc-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc9cc-109">Remarks</span></span>

<span data-ttu-id="fc9cc-110">Любое диалоговое окно, использующее свойство **аутофдискспаце** для определения, должен ли открыться диалоговое окно, должно установить [бит стиля диалогового окна траккдискспаце](trackdiskspace-dialog-style-bit.md) для диалогового окна, чтобы динамически обновлять пространство на целевых томах.</span><span class="sxs-lookup"><span data-stu-id="fc9cc-110">Any dialog relying on the **OutOfDiskSpace** property to determine whether to bring up a dialog must set the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc9cc-111">Требования</span><span class="sxs-lookup"><span data-stu-id="fc9cc-111">Requirements</span></span>



| <span data-ttu-id="fc9cc-112">Требование</span><span class="sxs-lookup"><span data-stu-id="fc9cc-112">Requirement</span></span> | <span data-ttu-id="fc9cc-113">Значение</span><span class="sxs-lookup"><span data-stu-id="fc9cc-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9cc-114">Версия</span><span class="sxs-lookup"><span data-stu-id="fc9cc-114">Version</span></span><br/> | <span data-ttu-id="fc9cc-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc9cc-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc9cc-116">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc9cc-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc9cc-117">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc9cc-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fc9cc-118">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fc9cc-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc9cc-119">См. также</span><span class="sxs-lookup"><span data-stu-id="fc9cc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc9cc-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc9cc-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




