---
description: Чтобы указать, что установщик запускает настраиваемое действие только при удалении исправления, можно использовать параметр Удаление исправления настраиваемого действия.
ms.assetid: c741aa40-ba4c-459e-936a-19c002620c30
title: Настраиваемые действия при удалении исправлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90cfffbdb37f1f2fab046b794010a790e9a5212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662369"
---
# <a name="patch-uninstall-custom-actions"></a><span data-ttu-id="23503-103">Настраиваемые действия при удалении исправлений</span><span class="sxs-lookup"><span data-stu-id="23503-103">Patch Uninstall Custom Actions</span></span>

<span data-ttu-id="23503-104">Чтобы указать, что установщик запускает настраиваемое действие только при удалении исправления, можно использовать [параметр Удаление исправления настраиваемого действия](custom-action-patch-uninstall-option.md) .</span><span class="sxs-lookup"><span data-stu-id="23503-104">You can use the [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) to specify that the installer run the custom action only when a patch is uninstalled.</span></span>

<span data-ttu-id="23503-105">**Установщик Windows 4,5 и более поздних версий:** Чтобы указать, что установщик будет запускать настраиваемое действие только при удалении исправления, можно использовать [параметр удалить с помощью настраиваемого действия удаление исправления](custom-action-patch-uninstall-option.md) .</span><span class="sxs-lookup"><span data-stu-id="23503-105">**Windows Installer 4.5 and later:** You can use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) to specify that the installer only run the custom action when a patch is uninstalled.</span></span>

<span data-ttu-id="23503-106">\*\*[Установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md): \* \*</span><span class="sxs-lookup"><span data-stu-id="23503-106">\*\*[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):  \*\*</span></span>

<span data-ttu-id="23503-107">[Параметр Удаление исправления настраиваемого действия](custom-action-patch-uninstall-option.md) недоступен.</span><span class="sxs-lookup"><span data-stu-id="23503-107">The [Custom Action Patch Uninstall option](custom-action-patch-uninstall-option.md) is not available.</span></span> <span data-ttu-id="23503-108">Не существует метода пометки [настраиваемого действия](custom-actions.md) в пакете исправлений для запуска при удалении исправления, так как установщик не применяет удаляемые пакеты исправлений.</span><span class="sxs-lookup"><span data-stu-id="23503-108">There is no method for marking a [custom action](custom-actions.md) within a patch package to be run when the patch is uninstalled because the installer does not apply the patch packages being uninstalled.</span></span>

<span data-ttu-id="23503-109">Чтобы [пользовательское действие](custom-actions.md) выполнялось при удалении определенного исправления, пользовательское действие должно присутствовать в исходном приложении или быть исправлением для продукта, который всегда применяется.</span><span class="sxs-lookup"><span data-stu-id="23503-109">To have a [custom action](custom-actions.md) run when a particular patch is uninstalled, the custom action must either be present in the original application or be in a patch for the product that is always applied.</span></span>

<span data-ttu-id="23503-110">Разработчики могут использовать свойство [**MsiPatchRemovalList**](msipatchremovallist.md) для создания пакета установщик Windows или исправления, которое выполняет [пользовательские действия](custom-actions.md) по удалению исправления.</span><span class="sxs-lookup"><span data-stu-id="23503-110">Developers can use the [**MsiPatchRemovalList**](msipatchremovallist.md) property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="23503-111">Пользовательское действие может быть создано в исходном пакете установки, уже примененном к пакету или в исправлении, которое не является [удаляемым](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="23503-111">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="23503-112">Настраиваемое действие может быть условным для свойства **MsiPatchRemovalList** в таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="23503-112">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="23503-113">Дополнительные сведения о действиях кондитионализинг см. [в разделе Использование свойств в условных инструкциях](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="23503-113">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="23503-114">Настраиваемое действие может получать идентификаторы GUID удаляемых исправлений из значения свойства [**MsiPatchRemovalList**](msipatchremovallist.md) .</span><span class="sxs-lookup"><span data-stu-id="23503-114">The custom action can obtain the GUIDs of patches being removed from the value of the [**MsiPatchRemovalList**](msipatchremovallist.md) property.</span></span> <span data-ttu-id="23503-115">Пользовательское действие может определить, применено ли состояние установки исправления, устарело или заменено путем вызова свойства [**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) или [**патчпроперти**](patch-patchproperty.md) [объекта Patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="23503-115">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

<span data-ttu-id="23503-116">Если для настраиваемого действия требуются специальные метаданные из исправления, то исправление должно содержать пользовательское действие, записывающее метаданные в реестр или расположение файла при применении исправления.</span><span class="sxs-lookup"><span data-stu-id="23503-116">If the custom action requires special metadata from the patch, the patch should contain a custom action that writes the metadata to a registry or file location when the patch is applied.</span></span> <span data-ttu-id="23503-117">Пользовательское действие в исходном приложении или исправление, которое всегда применяется, может получить сведения, необходимые для удаления изменений исправления.</span><span class="sxs-lookup"><span data-stu-id="23503-117">The custom action in the original application or a patch that is always applied can obtain the information needed to remove the patch's changes.</span></span>

<span data-ttu-id="23503-118">Исправления, выполняющие изменения, которые трудно отменить правильно, не должны помечаться как [неустанавливаемые исправления](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="23503-118">Patches making changes that are difficult to undo correctly should not be marked as [uninstallable patches](uninstallable-patches.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23503-119">См. также</span><span class="sxs-lookup"><span data-stu-id="23503-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23503-120">Последовательность исправлений</span><span class="sxs-lookup"><span data-stu-id="23503-120">Patch Sequencing</span></span>](sequencing-patches.md)
</dt> <dt>

[<span data-ttu-id="23503-121">Удаление исправлений</span><span class="sxs-lookup"><span data-stu-id="23503-121">Removing Patches</span></span>](removing-patches.md)
</dt> <dt>

[<span data-ttu-id="23503-122">Неустанавливаемые исправления</span><span class="sxs-lookup"><span data-stu-id="23503-122">Uninstallable Patches</span></span>](uninstallable-patches.md)
</dt> <dt>

[<span data-ttu-id="23503-123">Удаление исправлений</span><span class="sxs-lookup"><span data-stu-id="23503-123">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="23503-124">**мсипатчремове**</span><span class="sxs-lookup"><span data-stu-id="23503-124">**MSIPATCHREMOVE**</span></span>](msipatchremove.md)
</dt> <dt>

[<span data-ttu-id="23503-125">**мсиенумаппликатионсекс**</span><span class="sxs-lookup"><span data-stu-id="23503-125">**MsiEnumapplicationsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[<span data-ttu-id="23503-126">**мсижетпатчинфоекс**</span><span class="sxs-lookup"><span data-stu-id="23503-126">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="23503-127">**мсиремовепатчес**</span><span class="sxs-lookup"><span data-stu-id="23503-127">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> </dl>

 

 



