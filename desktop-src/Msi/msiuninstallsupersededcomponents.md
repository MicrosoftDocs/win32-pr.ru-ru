---
description: Присвойте свойству МСИУНИНСТАЛЛСУПЕРСЕДЕДКОМПОНЕНТС значение 1 в таблице свойств или в командной строке.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: МСИУНИНСТАЛЛСУПЕРСЕДЕДКОМПОНЕНТС, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679606"
---
# <a name="msiuninstallsupersededcomponents-property"></a><span data-ttu-id="17657-103">МСИУНИНСТАЛЛСУПЕРСЕДЕДКОМПОНЕНТС, свойство</span><span class="sxs-lookup"><span data-stu-id="17657-103">MSIUNINSTALLSUPERSEDEDCOMPONENTS property</span></span>

<span data-ttu-id="17657-104">Присвойте свойству **мсиунинсталлсуперседедкомпонентс** значение 1 в [таблице свойств](property-table.md) или в командной строке.</span><span class="sxs-lookup"><span data-stu-id="17657-104">Set the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** property to 1 in the [Property table](property-table.md) or on a command line.</span></span> <span data-ttu-id="17657-105">Если этому свойству присвоено значение 1, установщик определяет, избыточны ли компоненты в любых заменяемых исправлениях.</span><span class="sxs-lookup"><span data-stu-id="17657-105">When this property has been set to 1, the installer determines whether the components in any superseded patches are becoming redundant.</span></span> <span data-ttu-id="17657-106">Установщик может отменить регистрацию и удаление избыточных компонентов, чтобы предотвратить появление устаревших компонентов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="17657-106">The installer can unregister and uninstall redundant components to prevent leaving behind orphan components on the computer.</span></span>

<span data-ttu-id="17657-107">Установка этого свойства влияет на компоненты во всех заменяемых исправлениях.</span><span class="sxs-lookup"><span data-stu-id="17657-107">Setting this property affects the components in all patches being superseded.</span></span> <span data-ttu-id="17657-108">Чтобы включить эту функцию для отдельных компонентов, используйте атрибут **мсидбкомпонентаттрибутесунинсталлонсуперседенце** в [таблице Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="17657-108">To enable this functionality for single components, use the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md).</span></span>

<span data-ttu-id="17657-109">**[Установщик Windows 4,0 и более ранних версий](not-supported-in-windows-installer-4-0.md):** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="17657-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="17657-110">Версии, предшествующие установщик Windows 4,5, игнорируют свойство **мсиунинсталлсуперседедкомпонентс** .</span><span class="sxs-lookup"><span data-stu-id="17657-110">Versions earlier than Windows Installer 4.5 ignore the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** Property.</span></span>

## <a name="requirements"></a><span data-ttu-id="17657-111">Требования</span><span class="sxs-lookup"><span data-stu-id="17657-111">Requirements</span></span>



| <span data-ttu-id="17657-112">Требование</span><span class="sxs-lookup"><span data-stu-id="17657-112">Requirement</span></span> | <span data-ttu-id="17657-113">Значение</span><span class="sxs-lookup"><span data-stu-id="17657-113">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17657-114">Версия</span><span class="sxs-lookup"><span data-stu-id="17657-114">Version</span></span><br/> | <span data-ttu-id="17657-115">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="17657-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="17657-116">Установщик Windows 4,5 или установщик Windows 4,5 в Windows Vista, Windows XP, Windows Server 2003 и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="17657-116">Windows Installer 4.5 or Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="17657-117">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="17657-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17657-118">См. также</span><span class="sxs-lookup"><span data-stu-id="17657-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17657-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="17657-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




