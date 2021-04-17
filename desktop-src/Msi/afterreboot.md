---
description: Установщик устанавливает свойство АФТЕРРЕБУТ в значение 1 после перезагрузки, вызванной действием Форцеребут. Установщик добавляет АФТЕРРЕБУТ = 1 в командную строку, выполняемую сразу после перезагрузки.
ms.assetid: d8a71d9a-64bf-4a38-9c3b-073c216de7fa
title: АФТЕРРЕБУТ, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa891c84e2e8f7bdea5bb90311e9706a37e46e31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652136"
---
# <a name="afterreboot-property"></a><span data-ttu-id="cc13e-104">АФТЕРРЕБУТ, свойство</span><span class="sxs-lookup"><span data-stu-id="cc13e-104">AFTERREBOOT property</span></span>

<span data-ttu-id="cc13e-105">Установщик устанавливает свойство **афтерребут** в значение 1 после перезагрузки, вызванной [действием форцеребут](forcereboot-action.md).</span><span class="sxs-lookup"><span data-stu-id="cc13e-105">The installer sets the **AFTERREBOOT** property to 1 after a reboot invoked by the [ForceReboot action](forcereboot-action.md).</span></span> <span data-ttu-id="cc13e-106">Установщик добавляет АФТЕРРЕБУТ = 1 в командную строку, выполняемую сразу после перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="cc13e-106">The installer adds AFTERREBOOT=1 to the command line run immediately after the reboot.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc13e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc13e-107">Remarks</span></span>

<span data-ttu-id="cc13e-108">[Действие форцеребут](forcereboot-action.md) всегда должно использоваться с условным оператором, так что установщик запускает перезагрузку только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="cc13e-108">The [ForceReboot action](forcereboot-action.md) must always be used with a conditional statement such that the installer triggers a reboot only when necessary.</span></span> <span data-ttu-id="cc13e-109">Если определенный файл был заменен или был установлен конкретный компонент, может потребоваться перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="cc13e-109">A reboot might be required if a particular file was replaced or a particular component was installed.</span></span> <span data-ttu-id="cc13e-110">Регистр для каждого продукта различается, и для определения необходимости перезагрузки может потребоваться пользовательское действие.</span><span class="sxs-lookup"><span data-stu-id="cc13e-110">The case is different for each product and a custom action might be needed to determine whether a reboot is needed.</span></span> <span data-ttu-id="cc13e-111">Условие в действии Форцеребут обычно использует свойство **афтерребут** .</span><span class="sxs-lookup"><span data-stu-id="cc13e-111">The condition on the ForceReboot action commonly makes use of the **AFTERREBOOT** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc13e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="cc13e-112">Requirements</span></span>



| <span data-ttu-id="cc13e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="cc13e-113">Requirement</span></span> | <span data-ttu-id="cc13e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cc13e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc13e-115">Версия</span><span class="sxs-lookup"><span data-stu-id="cc13e-115">Version</span></span><br/> | <span data-ttu-id="cc13e-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc13e-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cc13e-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cc13e-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cc13e-118">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc13e-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cc13e-119">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cc13e-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc13e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="cc13e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc13e-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="cc13e-121">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="cc13e-122">Перезагрузка системы</span><span class="sxs-lookup"><span data-stu-id="cc13e-122">System Reboots</span></span>](system-reboots.md)
</dt> </dl>

 

 




