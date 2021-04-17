---
description: Действие Мигратефеатурестатес используется во время обновления и при установке нового приложения поверх связанного приложения.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Действие Мигратефеатурестатес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e76edb5fa13506291cc85ebcf8c8824e4ee28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674120"
---
# <a name="migratefeaturestates-action"></a><span data-ttu-id="10be3-103">Действие Мигратефеатурестатес</span><span class="sxs-lookup"><span data-stu-id="10be3-103">MigrateFeatureStates Action</span></span>

<span data-ttu-id="10be3-104">Действие Мигратефеатурестатес используется во время обновления и при установке нового приложения поверх связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="10be3-104">The MigrateFeatureStates action is used during upgrading and when installing a new application over a related application.</span></span> <span data-ttu-id="10be3-105">Мигратефеатурестатес считывает состояния компонентов в существующем приложении, а затем устанавливает эти состояния компонентов в состоянии ожидания установки.</span><span class="sxs-lookup"><span data-stu-id="10be3-105">MigrateFeatureStates reads the feature states in the existing application and then sets these feature states in the pending installation.</span></span> <span data-ttu-id="10be3-106">Метод полезен только в том случае, если новое дерево функций сильно не изменилось с исходного.</span><span class="sxs-lookup"><span data-stu-id="10be3-106">The method is only useful when the new feature tree has not greatly changed from the original.</span></span>

<span data-ttu-id="10be3-107">Действие Мигратефеатурестатес выполняется только при первом установке продукта.</span><span class="sxs-lookup"><span data-stu-id="10be3-107">The MigrateFeatureStates action only runs the first time the product is installed.</span></span> <span data-ttu-id="10be3-108">Действие Мигратефеатурестатес не выполняется во время режима обслуживания или удаления.</span><span class="sxs-lookup"><span data-stu-id="10be3-108">The MigrateFeatureStates action does not run during maintenance mode or uninstallation.</span></span>

<span data-ttu-id="10be3-109">Действие Мигратефеатурестатес выполняется через каждую запись [обновленной таблицы](upgrade-table.md) последовательно и сравнивает код обновления, версию продукта и язык в каждой строке со всеми установленными в системе продуктами.</span><span class="sxs-lookup"><span data-stu-id="10be3-109">MigrateFeatureStates action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to all products installed on the system.</span></span> <span data-ttu-id="10be3-110">Если действие Мигратефеатурестатес обнаруживает корреспонденцию, а флаг Мсидбупградеаттрибутесмигратефеатурес bit задан в столбце Attributes таблицы Upgrade, то установщик запрашивает существующие состояния компонентов для продукта и устанавливает эти состояния для тех же функций в новом приложении.</span><span class="sxs-lookup"><span data-stu-id="10be3-110">If MigrateFeatureStates action detects a correspondence, and if the msidbUpgradeAttributesMigrateFeatures bit flag is set in the Attributes column of the Upgrade table, the installer queries the existing feature states for the product and sets these states for the same features in the new application.</span></span> <span data-ttu-id="10be3-111">Действие переносит только те состояния компонентов, если не задано предварительно [**выбранное**](preselected.md) свойство.</span><span class="sxs-lookup"><span data-stu-id="10be3-111">The action only migrates the feature states if the [**Preselected**](preselected.md) property is not set.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="10be3-112">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="10be3-112">Sequence Restrictions</span></span>

<span data-ttu-id="10be3-113">Действие Мигратефеатурестатес должно следовать сразу после [действия костфинализе](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="10be3-113">The MigrateFeatureStates action should come immediately after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="10be3-114">Мигратефеатурестатес должны быть упорядочены как в [таблице инсталлуисекуенце](installuisequence-table.md) , так и в [таблице инсталлексекутесекуенце](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="10be3-114">MigrateFeatureStates must be sequenced in both the [InstallUISequence table](installuisequence-table.md) and the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="10be3-115">Установщик предотвращает запуск Мигратефеатурестатес в Инсталлексекутесекуенце, если действие уже выполнялось в Инсталлуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="10be3-115">The installer prevents MigrateFeatureStates from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="10be3-116">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="10be3-116">ActionData Messages</span></span>

<span data-ttu-id="10be3-117">Мигратефеатуресеттингс отправляет сообщение данных о действии для каждого продукта.</span><span class="sxs-lookup"><span data-stu-id="10be3-117">MigrateFeatureSettings sends an action data message for each product.</span></span>

## <a name="remarks"></a><span data-ttu-id="10be3-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10be3-118">Remarks</span></span>

<span data-ttu-id="10be3-119">Если несколько установленных продуктов совместно используют одну и ту же функцию, то состояние установки этого компонента может отличаться для разных продуктов.</span><span class="sxs-lookup"><span data-stu-id="10be3-119">If more than one installed product shares a feature, the installation state for that feature may differ between products.</span></span> <span data-ttu-id="10be3-120">Действие Мигратефеатурестате использует следующий порядок приоритета при переносе состояний установки компонентов: Запуск локальной системы, запуск из источника, объявление и удаление.</span><span class="sxs-lookup"><span data-stu-id="10be3-120">MigrateFeatureState action uses the following order of precedence when migrating feature installation states: run local, run from source, advertised, and uninstalled.</span></span> <span data-ttu-id="10be3-121">Например, установленный продукт A может иметь функцию Y как INSTALLSTATE \_ Local и установленный продукт B может иметь функцию y, так как InstallState \_ отсутствует.</span><span class="sxs-lookup"><span data-stu-id="10be3-121">For example, installed product A may have feature Y as INSTALLSTATE\_LOCAL and installed product B may have feature Y as INSTALLSTATE\_ABSENT.</span></span> <span data-ttu-id="10be3-122">Если при обновлении устанавливается продукт C и выполняется миграция состояния установки компонента Y, Мигратефеатурестате устанавливает в качестве состояния установки компонента Y в продукте C значение INSTALLSTATE \_ Local.</span><span class="sxs-lookup"><span data-stu-id="10be3-122">If an upgrade installs product C and migrates the installation state of feature Y, MigrateFeatureState sets the installation state of feature Y in product C to INSTALLSTATE\_LOCAL.</span></span>

<span data-ttu-id="10be3-123">Дополнительные сведения об использовании действия Мигратефеатурестатес для обновления продукта см. в разделе [Подготовка приложения к будущим основным обновлениям](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="10be3-123">For more information about how to use the MigrateFeatureStates action for product upgrades, see [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

 

 



