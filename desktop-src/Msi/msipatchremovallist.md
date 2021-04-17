---
description: Установщик устанавливает значение свойства MsiPatchRemovalList в список исправлений, удаляемых во время установки.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: MsiPatchRemovalList, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665384"
---
# <a name="msipatchremovallist-property"></a><span data-ttu-id="fc5b7-103">MsiPatchRemovalList, свойство</span><span class="sxs-lookup"><span data-stu-id="fc5b7-103">MsiPatchRemovalList property</span></span>

<span data-ttu-id="fc5b7-104">Установщик устанавливает значение свойства **MsiPatchRemovalList** в список исправлений, удаляемых во время установки.</span><span class="sxs-lookup"><span data-stu-id="fc5b7-104">The installer sets the value of the **MsiPatchRemovalList** property to a list of patches that are being removed during the installation.</span></span> <span data-ttu-id="fc5b7-105">Исправления представлены в списке с помощью идентификаторов GUID кода исправления, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="fc5b7-105">The patches are represented in the list by their patch code GUIDs separated by semicolons.</span></span>

<span data-ttu-id="fc5b7-106">Разработчики могут использовать свойство **MsiPatchRemovalList** для создания пакета установщик Windows или исправления, которое выполняет [пользовательские действия](custom-actions.md) по удалению исправления.</span><span class="sxs-lookup"><span data-stu-id="fc5b7-106">Developers can use the **MsiPatchRemovalList** property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="fc5b7-107">Пользовательское действие может быть создано в исходном пакете установки, уже примененном к пакету или в исправлении, которое не является [удаляемым](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="fc5b7-107">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="fc5b7-108">Настраиваемое действие может быть условным для свойства **MsiPatchRemovalList** в таблицах последовательности.</span><span class="sxs-lookup"><span data-stu-id="fc5b7-108">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="fc5b7-109">Дополнительные сведения о действиях кондитионализинг см. [в разделе Использование свойств в условных инструкциях](using-properties-in-conditional-statements.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5b7-109">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="fc5b7-110">Настраиваемое действие может получать идентификаторы GUID удаляемых исправлений из значения свойства **MsiPatchRemovalList** .</span><span class="sxs-lookup"><span data-stu-id="fc5b7-110">The custom action can obtain the GUIDs of patches being removed from the value of the **MsiPatchRemovalList** property.</span></span> <span data-ttu-id="fc5b7-111">Пользовательское действие может определить, применено ли состояние установки исправления, устарело или заменено путем вызова функции [**мсижетпатчинфоекс**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) или свойства [**патчпроперти**](patch-patchproperty.md) [объекта Patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="fc5b7-111">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) function or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc5b7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc5b7-112">Remarks</span></span>

<span data-ttu-id="fc5b7-113">Дополнительные сведения об удалении исправлений см. в разделе [Удаление исправлений](removing-patches.md).</span><span class="sxs-lookup"><span data-stu-id="fc5b7-113">For more information about removing patches, see [Removing Patches](removing-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc5b7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fc5b7-114">Requirements</span></span>



| <span data-ttu-id="fc5b7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fc5b7-115">Requirement</span></span> | <span data-ttu-id="fc5b7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fc5b7-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc5b7-117">Версия</span><span class="sxs-lookup"><span data-stu-id="fc5b7-117">Version</span></span><br/> | <span data-ttu-id="fc5b7-118">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fc5b7-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fc5b7-119">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fc5b7-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fc5b7-120">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc5b7-120">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fc5b7-121">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fc5b7-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc5b7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fc5b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc5b7-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc5b7-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="fc5b7-124">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="fc5b7-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




