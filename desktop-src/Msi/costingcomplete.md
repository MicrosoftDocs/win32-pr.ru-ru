---
description: Свойство Костингкомплете указывает, завершила ли программа установки затраты места на диске.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Костингкомплете, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651778"
---
# <a name="costingcomplete-property"></a><span data-ttu-id="dc211-103">Костингкомплете, свойство</span><span class="sxs-lookup"><span data-stu-id="dc211-103">CostingComplete property</span></span>

<span data-ttu-id="dc211-104">Свойство **костингкомплете** указывает, завершила ли программа установки затраты места на диске.</span><span class="sxs-lookup"><span data-stu-id="dc211-104">The **CostingComplete** property indicates whether the installer has completed disk space costing.</span></span> <span data-ttu-id="dc211-105">Это свойство можно использовать для создания диалогового окна, запускаемого, если не было завершено расчет стоимости.</span><span class="sxs-lookup"><span data-stu-id="dc211-105">This property can be used to author a dialog box triggered if costing has not been completed.</span></span> <span data-ttu-id="dc211-106">Свойство задается динамически во время учета места на диске и устанавливается равным 1 сразу после завершения расчета стоимости.</span><span class="sxs-lookup"><span data-stu-id="dc211-106">The property is set dynamically during disk space costing and is set to 1 as soon as the costing is complete.</span></span> <span data-ttu-id="dc211-107">Это свойство инициализируется значением 0 с помощью [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="dc211-107">This property is initialized to 0 by the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc211-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc211-108">Remarks</span></span>

<span data-ttu-id="dc211-109">Пример создания "Подождите.</span><span class="sxs-lookup"><span data-stu-id="dc211-109">For an example of how to author a "Please wait .</span></span> <span data-ttu-id="dc211-110">.</span><span class="sxs-lookup"><span data-stu-id="dc211-110">.</span></span> <span data-ttu-id="dc211-111">.</span><span class="sxs-lookup"><span data-stu-id="dc211-111">.</span></span> <span data-ttu-id="dc211-112">"диалоговое окно, которое появляется во время учета затрат места на диске, см. в разделе [создание условного выражения" Подождите... ". Окно сообщения](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="dc211-112">" dialog box that pops up during disk space costing, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc211-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dc211-113">Requirements</span></span>



| <span data-ttu-id="dc211-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dc211-114">Requirement</span></span> | <span data-ttu-id="dc211-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dc211-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc211-116">Версия</span><span class="sxs-lookup"><span data-stu-id="dc211-116">Version</span></span><br/> | <span data-ttu-id="dc211-117">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dc211-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dc211-118">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dc211-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dc211-119">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc211-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="dc211-120">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="dc211-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc211-121">См. также</span><span class="sxs-lookup"><span data-stu-id="dc211-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc211-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc211-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




