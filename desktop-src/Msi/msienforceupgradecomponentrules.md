---
description: Задайте для свойства МСИЕНФОРЦЕУПГРАДЕКОМПОНЕНТРУЛЕС значение 1 в командной строке или в таблице свойств, чтобы применить правила обновления компонентов при небольших обновлениях и незначительных обновлениях конкретного продукта.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: МСИЕНФОРЦЕУПГРАДЕКОМПОНЕНТРУЛЕС, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668703"
---
# <a name="msienforceupgradecomponentrules-property"></a><span data-ttu-id="6cff6-103">МСИЕНФОРЦЕУПГРАДЕКОМПОНЕНТРУЛЕС, свойство</span><span class="sxs-lookup"><span data-stu-id="6cff6-103">MSIENFORCEUPGRADECOMPONENTRULES property</span></span>

<span data-ttu-id="6cff6-104">Задайте для свойства **мсиенфорцеупградекомпонентрулес** значение 1 в командной строке или в [таблице свойств](property-table.md) , чтобы применить правила обновления компонентов при [небольших обновлениях](small-updates.md) и [незначительных обновлениях](minor-upgrades.md) конкретного продукта.</span><span class="sxs-lookup"><span data-stu-id="6cff6-104">Set the **MSIENFORCEUPGRADECOMPONENTRULES** property to 1 on the command line or in the [Property table](property-table.md) to apply the upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of a particular product.</span></span> <span data-ttu-id="6cff6-105">Чтобы применить правила при небольших обновлениях и незначительных обновлениях всех продуктов на компьютере, установите для политики [енфорцеупградекомпонентрулес](enforceupgradecomponentrules.md) значение 1.</span><span class="sxs-lookup"><span data-stu-id="6cff6-105">To apply the rules during small updates and minor upgrades of all products on the computer, set the [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) policy to 1.</span></span>

<span data-ttu-id="6cff6-106">Если свойство или политика имеет значение 1, [небольшие обновления](small-updates.md) и [небольшие](minor-upgrades.md) обновления могут завершиться ошибкой, так как обновление пытается выполнить следующие действия, нарушающие правила обновления компонентов:</span><span class="sxs-lookup"><span data-stu-id="6cff6-106">When the property or policy is set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update tries to do the following that violates the upgrade component rules:</span></span>

-   <span data-ttu-id="6cff6-107">Добавление новой функции в начало или середину существующего дерева компонентов.</span><span class="sxs-lookup"><span data-stu-id="6cff6-107">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="6cff6-108">Новую функцию необходимо добавить в качестве новой конечной функции в существующее дерево компонентов.</span><span class="sxs-lookup"><span data-stu-id="6cff6-108">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="6cff6-109">В этом случае [**код**](productcode.md) продукта может быть изменен, а обновление можно считать [основным обновлением](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="6cff6-109">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="6cff6-110">Удаление компонента из компонента.</span><span class="sxs-lookup"><span data-stu-id="6cff6-110">Remove a component from a feature.</span></span>

    <span data-ttu-id="6cff6-111">Это также может произойти при изменении идентификатора GUID компонента.</span><span class="sxs-lookup"><span data-stu-id="6cff6-111">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="6cff6-112">Компонент, идентифицируемый исходным идентификатором GUID, будет удален, а компонент, определенный новым GUID, появится как новый компонент.</span><span class="sxs-lookup"><span data-stu-id="6cff6-112">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="6cff6-113">**Установщик Windows 4,5 и более поздних версий:** Компонент можно правильно удалить с помощью установщик Windows 4,5 и более поздних версий, задав атрибут **мсидбкомпонентаттрибутесунинсталлонсуперседенце** в [таблице Component](component-table.md) или задав свойство [**мсиунинсталлсуперседедкомпонентс**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="6cff6-113">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 and later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component Table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="6cff6-114">Кроме того, можно изменить [**ProductCode**](productcode.md) продукта, и обновление можно считать [основным обновлением](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="6cff6-114">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6cff6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6cff6-115">Requirements</span></span>



| <span data-ttu-id="6cff6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6cff6-116">Requirement</span></span> | <span data-ttu-id="6cff6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6cff6-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cff6-118">Версия</span><span class="sxs-lookup"><span data-stu-id="6cff6-118">Version</span></span><br/> | <span data-ttu-id="6cff6-119">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6cff6-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6cff6-120">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6cff6-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6cff6-121">Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6cff6-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6cff6-122">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6cff6-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6cff6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6cff6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cff6-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="6cff6-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="6cff6-125">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="6cff6-125">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




