---
description: Пакеты обновления установщик Windows могут быть созданы, чтобы обновления не устанавливались, если у пользователя уже установлена более новая версия.
ms.assetid: f46e82bd-70b3-46a2-8246-a1eadfdc589d
title: Предотвращать установку старого пакета более новой версией
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320ab062c4ffbc740d85c59ece3d3baaa63f4209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650692"
---
# <a name="preventing-an-old-package-from-installing-over-a-newer-version"></a><span data-ttu-id="5eef0-103">Предотвращение установки старого пакета более новой версией</span><span class="sxs-lookup"><span data-stu-id="5eef0-103">Preventing an Old Package from Installing Over a Newer Version</span></span>

<span data-ttu-id="5eef0-104">Пакеты обновления установщик Windows могут быть созданы, чтобы обновления не устанавливались, если у пользователя уже установлена более новая версия.</span><span class="sxs-lookup"><span data-stu-id="5eef0-104">Windows Installer upgrade packages can be authored to have major upgrades not install if a user already has a newer version installed.</span></span> <span data-ttu-id="5eef0-105">Процедура в этом разделе может только препятствовать переходу на более раннюю версию, которая может быть вызвана запуском основного пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="5eef0-105">The procedure in this topic can only prevent downgrades that might be caused by running a major upgrade package.</span></span> <span data-ttu-id="5eef0-106">Эта процедура зависит от [действия финдрелатедпродуктс](findrelatedproducts-action.md), которое выполняется только при первой установке и не выполняется в режиме обслуживания (переустановка).</span><span class="sxs-lookup"><span data-stu-id="5eef0-106">This procedure relies on the [FindRelatedProducts Action](findrelatedproducts-action.md), which only runs during a first-time installation and does not run in maintenance mode (reinstallation).</span></span> <span data-ttu-id="5eef0-107">Так как небольшие обновления выполняются с помощью повторной установки, эту процедуру нельзя использовать, чтобы определить, пытается ли понизить версию приложения с незначительным обновлением.</span><span class="sxs-lookup"><span data-stu-id="5eef0-107">Because minor upgrades are performed using reinstallation, this procedure cannot be used to determine whether a minor upgrade package is attempting to downgrade an application.</span></span> <span data-ttu-id="5eef0-108">Дополнительные сведения см. в разделе [Подготовка приложения к будущим основным обновлениям](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-108">For more information, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

<span data-ttu-id="5eef0-109">**Предотвращение установки старого пакета более новой версией**</span><span class="sxs-lookup"><span data-stu-id="5eef0-109">**To prevent an old package from installing over a newer version**</span></span>

1.  <span data-ttu-id="5eef0-110">Введите свойство [**UpgradeCode**](upgradecode.md) для группы связанных продуктов, которые могут получать это обновление, в столбец UpgradeCode [таблицы обновления](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-110">Enter the [**UpgradeCode**](upgradecode.md) Property for the group of related products that may be eligible to receive this upgrade into the UpgradeCode column of the [Upgrade Table](upgrade-table.md).</span></span>
2.  <span data-ttu-id="5eef0-111">Введите флаг **мсидбупградеаттрибутесонлидетект** bit в столбце Attributes [таблицы Upgrade](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-111">Enter the **msidbUpgradeAttributesOnlyDetect** bit flag in the Attributes column of the [Upgrade Table](upgrade-table.md).</span></span>
3.  <span data-ttu-id="5eef0-112">Введите версию обновления, предоставленную этим пакетом, в столбец Версионмин [таблицы Upgrade](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-112">Enter the version of the upgrade provided by this package into the VersionMin column of the [Upgrade Table](upgrade-table.md).</span></span> <span data-ttu-id="5eef0-113">Оставьте столбец Версионмакс пустым.</span><span class="sxs-lookup"><span data-stu-id="5eef0-113">Leave the VersionMax column blank.</span></span>
4.  <span data-ttu-id="5eef0-114">Введите имя свойства, которое должно быть задано [действием финдрелатедпродуктс](findrelatedproducts-action.md) , в столбец Актионпроперти [таблицы Upgrade](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-114">Enter the name of the property that is to be set by the [FindRelatedProducts Action](findrelatedproducts-action.md) into the ActionProperty column of the [Upgrade Table](upgrade-table.md).</span></span>
5.  <span data-ttu-id="5eef0-115">Добавьте свойство [**секурекустомпропертиес**](securecustomproperties.md) и свойство с именем в столбец Актионпроперти [таблицы Upgrade](upgrade-table.md) в [таблицу свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-115">Add the [**SecureCustomProperties**](securecustomproperties.md) property and the property named in the ActionProperty column of the [Upgrade Table](upgrade-table.md) to the [Property Table](property-table.md).</span></span>
6.  <span data-ttu-id="5eef0-116">Добавьте [тип настраиваемого действия 19](custom-action-type-19.md) после действия Финдрелатедпродуктс в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-116">Add a [Custom Action Type 19](custom-action-type-19.md) after the FindRelatedProducts action in the [InstallExecuteSequence Table](installexecutesequence-table.md).</span></span> <span data-ttu-id="5eef0-117">Включите запись в [таблицу CustomAction](customaction-table.md) для этого действия и введите текст, который будет отображаться в целевом столбце.</span><span class="sxs-lookup"><span data-stu-id="5eef0-117">Include a record in the [CustomAction Table](customaction-table.md) for this action and enter the text to be displayed in the Target column.</span></span> <span data-ttu-id="5eef0-118">Настраиваемое действие типа 19 встроено в установщик, поэтому код для записи отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5eef0-118">The type 19 custom action is built into the installer, so there is no code to write.</span></span>
7.  <span data-ttu-id="5eef0-119">Введите имя Актионпроперти в столбец Условие записи в [таблице инсталлексекутесекуенце](installexecutesequence-table.md) , которая содержит [тип настраиваемого действия 19](custom-action-type-19.md).</span><span class="sxs-lookup"><span data-stu-id="5eef0-119">Enter the name of the ActionProperty into the Condition column of the record in [InstallExecuteSequence Table](installexecutesequence-table.md) that contains the [Custom Action Type 19](custom-action-type-19.md).</span></span> <span data-ttu-id="5eef0-120">Это условие позволяет выполнить пользовательское действие только в том случае, если в [таблице обновления](upgrade-table.md) обнаруживается, что уже установлена более новая версия.</span><span class="sxs-lookup"><span data-stu-id="5eef0-120">This conditions the custom action to only be executed when the [Upgrade Table](upgrade-table.md) detects that a newer version is already installed.</span></span>

    <span data-ttu-id="5eef0-121">Например, пакет установщик Windows, который обновляет группу связанных продуктов до версии 3,0, может включать в себя следующие записи в своих таблицах [обновления](upgrade-table.md), [CustomAction](customaction-table.md), [инсталлексекутесекуенце](installexecutesequence-table.md)и [свойств](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5eef0-121">For example, a Windows Installer package that upgrades a group of related products to version 3.0 may include the following records in its [Upgrade](upgrade-table.md), [CustomAction](customaction-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [Property](property-table.md) tables.</span></span> <span data-ttu-id="5eef0-122">Все связанные продукты в группе имеют одно и то же значение UpgradeCode, но установщик не устанавливает этот пакет обновления, если на компьютере уже установлена более поздняя версия, чем 3,0.</span><span class="sxs-lookup"><span data-stu-id="5eef0-122">All the related products in the group have the same UpgradeCode, but the installer does not install this upgrade package if a version later than 3.0 is already installed on the computer.</span></span> <span data-ttu-id="5eef0-123">В этом случае установщик выводит сообщение об ошибке, и установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="5eef0-123">In this case, the Installer presents an error message and the installation fails.</span></span> <span data-ttu-id="5eef0-124">Пакет обновления версии 3,0 устанавливает более ранние версии, чем 1,0 и 2,0.</span><span class="sxs-lookup"><span data-stu-id="5eef0-124">The version 3.0 upgrade package installs over versions 1.0 and 2.0.</span></span>

    [<span data-ttu-id="5eef0-125">Обновление таблицы</span><span class="sxs-lookup"><span data-stu-id="5eef0-125">Upgrade Table</span></span>](upgrade-table.md)

    

    | <span data-ttu-id="5eef0-126">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="5eef0-126">UpgradeCode</span></span>                            | <span data-ttu-id="5eef0-127">версионмин</span><span class="sxs-lookup"><span data-stu-id="5eef0-127">VersionMin</span></span> | <span data-ttu-id="5eef0-128">версионмакс</span><span class="sxs-lookup"><span data-stu-id="5eef0-128">VersionMax</span></span> | <span data-ttu-id="5eef0-129">Язык</span><span class="sxs-lookup"><span data-stu-id="5eef0-129">Language</span></span> | <span data-ttu-id="5eef0-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5eef0-130">Attributes</span></span>                                | <span data-ttu-id="5eef0-131">Удалить</span><span class="sxs-lookup"><span data-stu-id="5eef0-131">Remove</span></span> | <span data-ttu-id="5eef0-132">актионпроперти</span><span class="sxs-lookup"><span data-stu-id="5eef0-132">ActionProperty</span></span>  |
    |----------------------------------------|------------|------------|----------|-------------------------------------------|--------|-----------------|
    | <span data-ttu-id="5eef0-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="5eef0-133">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="5eef0-134">3.0</span><span class="sxs-lookup"><span data-stu-id="5eef0-134">3.0</span></span>        |            |          | <span data-ttu-id="5eef0-135">мсидбупградеаттрибутесонлидетект</span><span class="sxs-lookup"><span data-stu-id="5eef0-135">msidbUpgradeAttributesOnlyDetect</span></span>          |        | <span data-ttu-id="5eef0-136">невпродуктфаунд</span><span class="sxs-lookup"><span data-stu-id="5eef0-136">NEWPRODUCTFOUND</span></span> |
    | <span data-ttu-id="5eef0-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span><span class="sxs-lookup"><span data-stu-id="5eef0-137">{E7BE6D45-49FF-4701-A17E-BDCC98CE180D}</span></span> | <span data-ttu-id="5eef0-138">1.0</span><span class="sxs-lookup"><span data-stu-id="5eef0-138">1.0</span></span>        | <span data-ttu-id="5eef0-139">3.0</span><span class="sxs-lookup"><span data-stu-id="5eef0-139">3.0</span></span>        |          | <span data-ttu-id="5eef0-140">мсидбупградеаттрибутесверсионмининклусиве</span><span class="sxs-lookup"><span data-stu-id="5eef0-140">msidbUpgradeAttributesVersionMinInclusive</span></span> |        | <span data-ttu-id="5eef0-141">упградефаунд</span><span class="sxs-lookup"><span data-stu-id="5eef0-141">UPGRADEFOUND</span></span>    |

    

     

    [<span data-ttu-id="5eef0-142">Таблица CustomAction</span><span class="sxs-lookup"><span data-stu-id="5eef0-142">CustomAction Table</span></span>](customaction-table.md)

    

    | <span data-ttu-id="5eef0-143">Действие</span><span class="sxs-lookup"><span data-stu-id="5eef0-143">Action</span></span> | <span data-ttu-id="5eef0-144">Тип</span><span class="sxs-lookup"><span data-stu-id="5eef0-144">Type</span></span> | <span data-ttu-id="5eef0-145">Источник</span><span class="sxs-lookup"><span data-stu-id="5eef0-145">Source</span></span> | <span data-ttu-id="5eef0-146">Назначение</span><span class="sxs-lookup"><span data-stu-id="5eef0-146">Target</span></span>                                 |
    |--------|------|--------|----------------------------------------|
    | <span data-ttu-id="5eef0-147">CA1</span><span class="sxs-lookup"><span data-stu-id="5eef0-147">CA1</span></span>    | <span data-ttu-id="5eef0-148">19</span><span class="sxs-lookup"><span data-stu-id="5eef0-148">19</span></span>   |        | <span data-ttu-id="5eef0-149">Уже установлено более высокое обновление.</span><span class="sxs-lookup"><span data-stu-id="5eef0-149">A higher upgrade is already installed.</span></span> |

    

     

    [<span data-ttu-id="5eef0-150">Таблица Инсталлексекутесекуенце</span><span class="sxs-lookup"><span data-stu-id="5eef0-150">InstallExecuteSequence Table</span></span>](installexecutesequence-table.md)

    

    | <span data-ttu-id="5eef0-151">Действие</span><span class="sxs-lookup"><span data-stu-id="5eef0-151">Action</span></span>              | <span data-ttu-id="5eef0-152">Условие</span><span class="sxs-lookup"><span data-stu-id="5eef0-152">Condition</span></span>       | <span data-ttu-id="5eef0-153">Последовательность</span><span class="sxs-lookup"><span data-stu-id="5eef0-153">Sequence</span></span> |
    |---------------------|-----------------|----------|
    | <span data-ttu-id="5eef0-154">финдрелатедпродуктс</span><span class="sxs-lookup"><span data-stu-id="5eef0-154">FindRelatedProducts</span></span> |                 | <span data-ttu-id="5eef0-155">200</span><span class="sxs-lookup"><span data-stu-id="5eef0-155">200</span></span>      |
    | <span data-ttu-id="5eef0-156">CA1</span><span class="sxs-lookup"><span data-stu-id="5eef0-156">CA1</span></span>                 | <span data-ttu-id="5eef0-157">невпродуктфаунд</span><span class="sxs-lookup"><span data-stu-id="5eef0-157">NEWPRODUCTFOUND</span></span> | <span data-ttu-id="5eef0-158">201</span><span class="sxs-lookup"><span data-stu-id="5eef0-158">201</span></span>      |

    

     

    [<span data-ttu-id="5eef0-159">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="5eef0-159">Property Table</span></span>](property-table.md)

    

    | <span data-ttu-id="5eef0-160">Свойство</span><span class="sxs-lookup"><span data-stu-id="5eef0-160">Property</span></span>                                                 | <span data-ttu-id="5eef0-161">Значение</span><span class="sxs-lookup"><span data-stu-id="5eef0-161">Value</span></span>                        |
    |----------------------------------------------------------|------------------------------|
    | [<span data-ttu-id="5eef0-162">**секурекустомпропертиес**</span><span class="sxs-lookup"><span data-stu-id="5eef0-162">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="5eef0-163">НЕВПРОДУКТФАУНД; упградефаунд</span><span class="sxs-lookup"><span data-stu-id="5eef0-163">NEWPRODUCTFOUND;UPGRADEFOUND</span></span> |

    

     

 

 



