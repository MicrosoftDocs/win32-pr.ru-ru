---
description: Установщик задает свойство Роллбаккдисаблед, когда откат был отключен.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Роллбаккдисаблед, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651741"
---
# <a name="rollbackdisabled-property"></a><span data-ttu-id="aed41-103">Роллбаккдисаблед, свойство</span><span class="sxs-lookup"><span data-stu-id="aed41-103">RollbackDisabled property</span></span>

<span data-ttu-id="aed41-104">Установщик задает свойство **роллбаккдисаблед** , когда откат был отключен.</span><span class="sxs-lookup"><span data-stu-id="aed41-104">The installer sets the **RollbackDisabled** property when rollback has been disabled.</span></span> <span data-ttu-id="aed41-105">**Роллбаккдисаблед** используется авторами пакетов, которым необходимо убедиться, что в установщике не отключен откат.</span><span class="sxs-lookup"><span data-stu-id="aed41-105">**RollbackDisabled** is used by package authors who need to ensure that the installer has not disabled rollback.</span></span> <span data-ttu-id="aed41-106">Свойство **роллбаккдисаблед** может использоваться в условном выражении, которое фактически отказывается продолжать установку, если задано свойство **роллбаккдисаблед** .</span><span class="sxs-lookup"><span data-stu-id="aed41-106">The **RollbackDisabled** property can be used in a conditional expression that effectively refuses to continue with the installation if **RollbackDisabled** property is set.</span></span>

## <a name="default-value"></a><span data-ttu-id="aed41-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="aed41-107">Default Value</span></span>

<span data-ttu-id="aed41-108">По умолчанию откат включен.</span><span class="sxs-lookup"><span data-stu-id="aed41-108">By default, rollback is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="aed41-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aed41-109">Remarks</span></span>

<span data-ttu-id="aed41-110">Поскольку [откат](rollback-custom-actions.md) и [фиксация](commit-custom-actions.md) не выполняются при отключенном откате, установщик не может правильно установить пакет, использующий эти типы настраиваемых действий в транзакции во время установки.</span><span class="sxs-lookup"><span data-stu-id="aed41-110">Because [rollback](rollback-custom-actions.md) and [commit](commit-custom-actions.md) do not run while rollback is disabled, the installer cannot properly install a package that uses these types of custom actions in a transaction during the installation.</span></span> <span data-ttu-id="aed41-111">В этом случае автор пакета должен включить условие с помощью Дисаблероллбакк, которое предотвращает продолжение установки, если откат отключен.</span><span class="sxs-lookup"><span data-stu-id="aed41-111">In this case, the author of the package should include a condition using DisableRollback that prevents the installation from continuing if rollback is disabled.</span></span>

<span data-ttu-id="aed41-112">Значение политики Дисаблероллбакк может быть задано администратором в рамках назначения системной политики.</span><span class="sxs-lookup"><span data-stu-id="aed41-112">The DisableRollback policy value can be set by an administrator as a part of assigning system policy.</span></span> <span data-ttu-id="aed41-113">Администраторам рекомендуется не отключать откат, если это не требуется.</span><span class="sxs-lookup"><span data-stu-id="aed41-113">Administrators are advised to not disable rollback unless necessary.</span></span> <span data-ttu-id="aed41-114">Дополнительные сведения о значении политики Дисаблероллбакк см. в разделе [Системная политика](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="aed41-114">For more information about DisableRollback policy value, see [System Policy](system-policy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aed41-115">Требования</span><span class="sxs-lookup"><span data-stu-id="aed41-115">Requirements</span></span>



| <span data-ttu-id="aed41-116">Требование</span><span class="sxs-lookup"><span data-stu-id="aed41-116">Requirement</span></span> | <span data-ttu-id="aed41-117">Значение</span><span class="sxs-lookup"><span data-stu-id="aed41-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aed41-118">Версия</span><span class="sxs-lookup"><span data-stu-id="aed41-118">Version</span></span><br/> | <span data-ttu-id="aed41-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aed41-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="aed41-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aed41-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="aed41-121">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="aed41-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="aed41-122">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="aed41-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aed41-123">См. также</span><span class="sxs-lookup"><span data-stu-id="aed41-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aed41-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="aed41-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="aed41-125">Откат установки</span><span class="sxs-lookup"><span data-stu-id="aed41-125">Rollback Installation</span></span>](rollback-installation.md)
</dt> <dt>

[<span data-ttu-id="aed41-126">Системная политика</span><span class="sxs-lookup"><span data-stu-id="aed41-126">System Policy</span></span>](system-policy.md)
</dt> <dt>

[<span data-ttu-id="aed41-127">откат настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="aed41-127">rollback custom actions</span></span>](rollback-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="aed41-128">зафиксировать настраиваемые действия</span><span class="sxs-lookup"><span data-stu-id="aed41-128">commit custom actions</span></span>](commit-custom-actions.md)
</dt> </dl>

 

 




