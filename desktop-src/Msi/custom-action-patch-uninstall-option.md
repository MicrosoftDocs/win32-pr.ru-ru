---
description: Используйте следующий флаг параметра, чтобы указать, что установщик запускает настраиваемое действие только при удалении исправления. Чтобы задать параметр, добавьте значение в этой таблице в значение поля ExtendedType таблицы CustomAction.
ms.assetid: aa4d9e21-5316-42b5-a22e-c7a5becd3cae
title: Параметр удаления исправления настраиваемого действия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108365876393733f7cc520ae565bb2c5ea7ff3df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651176"
---
# <a name="custom-action-patch-uninstall-option"></a><span data-ttu-id="d72b9-104">Параметр удаления исправления настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="d72b9-104">Custom Action Patch Uninstall Option</span></span>

<span data-ttu-id="d72b9-105">Используйте следующий флаг параметра, чтобы указать, что установщик запускает настраиваемое действие только при удалении исправления.</span><span class="sxs-lookup"><span data-stu-id="d72b9-105">Use the following option flag to specify that the installer run the custom action only when a patch is being uninstalled.</span></span> <span data-ttu-id="d72b9-106">Чтобы задать параметр, добавьте значение в этой таблице в значение поля ExtendedType [таблицы CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="d72b9-106">To set the option, add the value in this table to the value in the ExtendedType field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="d72b9-107">**[Установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d72b9-107">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="d72b9-108">Этот параметр доступен, начиная с установщик Windows 4,5.</span><span class="sxs-lookup"><span data-stu-id="d72b9-108">This option is available beginning with Windows Installer 4.5.</span></span>



| <span data-ttu-id="d72b9-109">Константа</span><span class="sxs-lookup"><span data-stu-id="d72b9-109">Constant</span></span>                                | <span data-ttu-id="d72b9-110">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="d72b9-110">Hexadecimal</span></span> | <span data-ttu-id="d72b9-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="d72b9-111">Decimal</span></span> | <span data-ttu-id="d72b9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d72b9-112">Description</span></span>                                                    |
|-----------------------------------------|-------------|---------|----------------------------------------------------------------|
| <span data-ttu-id="d72b9-113">**мсидбкустомактионтипепатчунинсталл**</span><span class="sxs-lookup"><span data-stu-id="d72b9-113">**msidbCustomActionTypePatchUninstall**</span></span> | <span data-ttu-id="d72b9-114">0x8000</span><span class="sxs-lookup"><span data-stu-id="d72b9-114">0x8000</span></span>      | <span data-ttu-id="d72b9-115">32768</span><span class="sxs-lookup"><span data-stu-id="d72b9-115">32768</span></span>   | <span data-ttu-id="d72b9-116">Настраиваемое действие выполняется только при удалении исправления.</span><span class="sxs-lookup"><span data-stu-id="d72b9-116">The custom action runs only when a patch is being uninstalled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d72b9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d72b9-117">Remarks</span></span>

<span data-ttu-id="d72b9-118">Этот атрибут можно добавить в настраиваемое действие путем его создания в установщик Windowsном пакете (MSI-файле).</span><span class="sxs-lookup"><span data-stu-id="d72b9-118">This attribute can be added to a custom action by authoring it in the Windows Installer package (.msi file).</span></span> <span data-ttu-id="d72b9-119">С помощью исправления можно добавить новое настраиваемое действие с этим атрибутом.</span><span class="sxs-lookup"><span data-stu-id="d72b9-119">A new custom action with this attribute can be added by a patch.</span></span> <span data-ttu-id="d72b9-120">Пользовательское действие, имеющее этот атрибут, может обновляться с помощью исправления.</span><span class="sxs-lookup"><span data-stu-id="d72b9-120">A custom action having this attribute can be updated by a patch.</span></span> <span data-ttu-id="d72b9-121">Этот атрибут нельзя добавить или удалить с помощью исправления для существующего настраиваемого действия.</span><span class="sxs-lookup"><span data-stu-id="d72b9-121">This attribute cannot be added or removed by a patch to an existing custom action.</span></span>

<span data-ttu-id="d72b9-122">Если исправление добавляет или обновляет настраиваемое действие с этим атрибутом, установщик Windows запускает новое или обновленное настраиваемое действие при удалении исправления.</span><span class="sxs-lookup"><span data-stu-id="d72b9-122">If a patch adds or updates a custom action with this attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="d72b9-123">Установщик Windows делает обновления из удаляемого исправления доступными для настраиваемого действия удаления исправления.</span><span class="sxs-lookup"><span data-stu-id="d72b9-123">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="d72b9-124">Исправление должно включать таблицу [мситрансформвиев *<PatchGUID>*](msitransformview.md) , чтобы предоставить эти сведения установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d72b9-124">The patch must include a [MsiTransformView *<PatchGUID>*](msitransformview.md) table to provide this information to Windows Installer.</span></span>

<span data-ttu-id="d72b9-125">Если пакет, содержащий настраиваемое действие с атрибутом **мсидбкустомактионтипепатчунинсталл** , устанавливается с помощью установщика версии более ранней, чем установщик Windows 4,0, установщик не вызывает настраиваемое действие при удалении исправления.</span><span class="sxs-lookup"><span data-stu-id="d72b9-125">When a package that contains a custom action with the **msidbCustomActionTypePatchUninstall** attribute is installed using an installer version earlier than Windows Installer 4.0, the installer does not call the custom action when the patch is uninstalled.</span></span> <span data-ttu-id="d72b9-126">Установка может выполнить настраиваемое действие во время установки, восстановления или обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="d72b9-126">The install can run the custom action during the installation, repair, or update of the package.</span></span>

<span data-ttu-id="d72b9-127">Пользовательские действия с атрибутом **мсидбкустомактионтипепатчунинсталл** должны быть условы с помощью свойства [**мсипатчремове**](msipatchremove.md) , чтобы предотвратить выполнение настраиваемого действия при установке, восстановлении или обновлении с помощью системы с установщик Windows 4,0 или более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="d72b9-127">Custom actions with the **msidbCustomActionTypePatchUninstall** attribute should be conditioned using the [**MSIPATCHREMOVE**](msipatchremove.md) property to prevent the custom action from running when installing, repairing, or updating using a system with Windows Installer 4.0 or earlier.</span></span> <span data-ttu-id="d72b9-128">При установке установщик Windows 4,5 и более поздних версий все исправления в системе с пользовательскими действиями, помеченными атрибутом **мсидбкустомактионтипепатчунинсталл** , запускают настраиваемое действие во время удаления исправления.</span><span class="sxs-lookup"><span data-stu-id="d72b9-128">When Windows Installer 4.5 and later is installed, all the patches on the system having custom actions marked with the **msidbCustomActionTypePatchUninstall** attribute run the custom action during patch uninstallation.</span></span> <span data-ttu-id="d72b9-129">Если в системе удаляется установщик Windows 4,5 или более поздней версии, то исправления теряют функцию удаления исправлений для настраиваемых действий.</span><span class="sxs-lookup"><span data-stu-id="d72b9-129">If Windows Installer 4.5 or later is removed from the system, patches lose the custom action patch uninstall functionality.</span></span>

<span data-ttu-id="d72b9-130">Сведения о выполнении настраиваемого действия во время удаления исправления с использованием более ранней версии, чем установщик Windows 4,5, см. в разделе [Удаление исправлений настраиваемые действия](patch-uninstall-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="d72b9-130">For information about running a custom action during the uninstallation of a patch using a version earlier than Windows Installer 4.5, see [Patch Uninstall Custom Actions](patch-uninstall-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d72b9-131">См. также</span><span class="sxs-lookup"><span data-stu-id="d72b9-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d72b9-132">Параметры выполнения In-Script настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="d72b9-132">Custom Action In-Script Execution Options</span></span>](custom-action-in-script-execution-options.md)
</dt> <dt>

[<span data-ttu-id="d72b9-133">Ссылка на настраиваемое действие</span><span class="sxs-lookup"><span data-stu-id="d72b9-133">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="d72b9-134">Сведения о настраиваемых действиях</span><span class="sxs-lookup"><span data-stu-id="d72b9-134">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="d72b9-135">Использование настраиваемых действий</span><span class="sxs-lookup"><span data-stu-id="d72b9-135">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="d72b9-136">мситрансформвиев *<PatchGUID>*</span><span class="sxs-lookup"><span data-stu-id="d72b9-136">MsiTransformView *<PatchGUID>*</span></span>](msitransformview.md)
</dt> </dl>

 

 



