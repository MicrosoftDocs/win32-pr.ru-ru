---
description: Это системная политика для каждого компьютера, которую можно использовать для применения правил обновления компонентов при небольших обновлениях и незначительных обновлениях.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: енфорцеупградекомпонентрулес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998691"
---
# <a name="enforceupgradecomponentrules"></a><span data-ttu-id="72128-103">енфорцеупградекомпонентрулес</span><span class="sxs-lookup"><span data-stu-id="72128-103">EnforceUpgradeComponentRules</span></span>

<span data-ttu-id="72128-104">Это [Системная политика](system-policy.md) для каждого компьютера, которую можно использовать для применения правил обновления компонентов при [небольших обновлениях](small-updates.md) и [незначительных обновлениях](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="72128-104">This is a per-machine [system policy](system-policy.md) that can be used to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md).</span></span>

<span data-ttu-id="72128-105">Задайте для политики Енфорцеупградекомпонентрулес значение 1, чтобы применить правила обновления компонентов при [небольших обновлениях](small-updates.md) и [незначительных обновлениях](minor-upgrades.md) всех продуктов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="72128-105">Set the EnforceUpgradeComponentRules policy to 1 to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of all products on the computer.</span></span> <span data-ttu-id="72128-106">Чтобы применить правила при небольших обновлениях и незначительных обновлениях конкретного продукта, присвойте свойству [**мсиенфорцеупградекомпонентрулес**](msienforceupgradecomponentrules.md) значение 1 в командной строке или в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="72128-106">To apply the rules during small updates and minor upgrades of a particular product, set the [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) property to 1 on the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="72128-107">Если свойство или политика установлено в 1, [небольшие обновления](small-updates.md) и [небольшие](minor-upgrades.md) обновления могут завершиться ошибкой, так как обновление пытается выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="72128-107">When the property or policy has been set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update attempts to do the following:</span></span>

-   <span data-ttu-id="72128-108">Добавление новой функции в начало или середину существующего дерева компонентов.</span><span class="sxs-lookup"><span data-stu-id="72128-108">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="72128-109">Новую функцию необходимо добавить в качестве новой конечной функции в существующее дерево компонентов.</span><span class="sxs-lookup"><span data-stu-id="72128-109">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="72128-110">В этом случае [**код**](productcode.md) продукта может быть изменен, а обновления могут рассматриваться как [основные обновления](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="72128-110">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="72128-111">Удаление компонента из компонента.</span><span class="sxs-lookup"><span data-stu-id="72128-111">Remove a component from a feature.</span></span>

    <span data-ttu-id="72128-112">Это также может произойти при изменении идентификатора GUID компонента.</span><span class="sxs-lookup"><span data-stu-id="72128-112">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="72128-113">Компонент, идентифицируемый исходным идентификатором GUID, будет удален, а компонент, определенный новым GUID, появится как новый компонент.</span><span class="sxs-lookup"><span data-stu-id="72128-113">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="72128-114">**Установщик Windows 4,5 и более поздних версий:** Компонент можно правильно удалить с помощью установщик Windows 4,5 или более поздней версии, задав атрибут **мсидбкомпонентаттрибутесунинсталлонсуперседенце** в [таблице Component](component-table.md) или задав свойство [**мсиунинсталлсуперседедкомпонентс**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="72128-114">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 or later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="72128-115">Кроме того, [**код**](productcode.md) продукта может быть изменен, и обновления могут рассматриваться как [основные обновления](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="72128-115">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="72128-116">Ключ реестра</span><span class="sxs-lookup"><span data-stu-id="72128-116">Registry Key</span></span>

<span data-ttu-id="72128-117">**HKey \_ \_** \\ **Политики программного обеспечения** локального компьютера \\  \\  \\  \\ **установщик** Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="72128-117">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="72128-118">Тип данных</span><span class="sxs-lookup"><span data-stu-id="72128-118">Data Type</span></span>

<span data-ttu-id="72128-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="72128-119">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="72128-120">См. также</span><span class="sxs-lookup"><span data-stu-id="72128-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72128-121">Не поддерживается в установщик Windows 2,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="72128-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



