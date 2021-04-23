---
description: Действие Финдрелатедпродуктс выполняется через каждую запись обновленной таблицы последовательно и сравнивает код обновления, версию продукта и язык в каждой строке с продуктами, установленными в системе.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Действие Финдрелатедпродуктс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347165"
---
# <a name="findrelatedproducts-action"></a><span data-ttu-id="4eee7-103">Действие Финдрелатедпродуктс</span><span class="sxs-lookup"><span data-stu-id="4eee7-103">FindRelatedProducts Action</span></span>

<span data-ttu-id="4eee7-104">Действие Финдрелатедпродуктс выполняется через каждую запись [обновленной таблицы](upgrade-table.md) последовательно и сравнивает код обновления, версию продукта и язык в каждой строке с продуктами, установленными в системе.</span><span class="sxs-lookup"><span data-stu-id="4eee7-104">The FindRelatedProducts action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to products installed on the system.</span></span> <span data-ttu-id="4eee7-105">Когда Финдрелатедпродуктс обнаруживает соответствие между информацией об обновлении и установленным продуктом, он добавляет код продукта к свойству, указанному в столбце Актионпроперти объекта Упградетабле.</span><span class="sxs-lookup"><span data-stu-id="4eee7-105">When FindRelatedProducts detects a correspondence between the upgrade information and an installed product, it appends the product code to the property specified in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="4eee7-106">Действие Финдрелатедпродуктс выполняется только при первом установке продукта.</span><span class="sxs-lookup"><span data-stu-id="4eee7-106">The FindRelatedProducts action only runs the first time the product is installed.</span></span> <span data-ttu-id="4eee7-107">Действие Финдрелатедпродуктс не выполняется во время режима обслуживания или удаления.</span><span class="sxs-lookup"><span data-stu-id="4eee7-107">The FindRelatedProducts action does not run during maintenance mode or uninstallation.</span></span>

## <a name="database-tables-queried"></a><span data-ttu-id="4eee7-108">Запрошенные таблицы базы данных</span><span class="sxs-lookup"><span data-stu-id="4eee7-108">Database Tables Queried</span></span>

<span data-ttu-id="4eee7-109">Это действие запрашивает следующую таблицу:</span><span class="sxs-lookup"><span data-stu-id="4eee7-109">This action queries the following table:</span></span>

[<span data-ttu-id="4eee7-110">Обновление таблицы</span><span class="sxs-lookup"><span data-stu-id="4eee7-110">Upgrade Table</span></span>](upgrade-table.md)

## <a name="properties-used"></a><span data-ttu-id="4eee7-111">Используемые свойства</span><span class="sxs-lookup"><span data-stu-id="4eee7-111">Properties Used</span></span>

<span data-ttu-id="4eee7-112">Действие Финдрелатедпродуктс использует свойство [**UpgradeCode**](upgradecode.md) и сведения о версии и языке, созданные в таблице обновления, для обнаружения установленных продуктов, затрагиваемых ожидающим обновлением.</span><span class="sxs-lookup"><span data-stu-id="4eee7-112">The FindRelatedProducts action uses the [**UpgradeCode**](upgradecode.md) property and the version and language information authored into the Upgrade table to detect installed products affected by the pending upgrade.</span></span> <span data-ttu-id="4eee7-113">Он добавляет код продукта обнаруженных продуктов к свойству в столбце Актионпроперти объекта Упградетабле.</span><span class="sxs-lookup"><span data-stu-id="4eee7-113">It appends the product code of detected products to the property in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="4eee7-114">Финдрелатедпродуктс распознает только существующие продукты, установленные с помощью установщик Windows с файлом MSI, который определяет свойство [**UpgradeCode**](upgradecode.md) , свойство [**ProductVersion**](productversion.md) и значение для свойства [**продуктлангуаже**](productlanguage.md) , которое является одним из языков, перечисленных в свойстве [**сводки шаблона**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="4eee7-114">FindRelatedProducts only recognizes existing products that have been installed using the Windows Installer with an .msi that defines an [**UpgradeCode**](upgradecode.md) property, a [**ProductVersion**](productversion.md) property, and a value for the [**ProductLanguage**](productlanguage.md) property that is one of the languages listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="4eee7-115">Обратите внимание, что Финдрелатедпродуктс использует язык, возвращенный [**мсижетпродуктинфо**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span><span class="sxs-lookup"><span data-stu-id="4eee7-115">Note that FindRelatedProducts uses the language returned by [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span></span> <span data-ttu-id="4eee7-116">Для правильной работы Финдрелатедпродуктс автор пакета должен убедиться, что для свойства [**продуктлангуаже**](productlanguage.md) в [таблице свойств](property-table.md) задан язык, который также указан в свойстве [**сводки шаблона**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="4eee7-116">For FindRelatedProducts to work correctly, the package author must be sure that the [**ProductLanguage**](productlanguage.md) property in the [Property table](property-table.md) is set to a language that is also listed in the [**Template Summary**](template-summary.md) Property.</span></span> <span data-ttu-id="4eee7-117">См. статью [Подготовка приложения к последующим основным обновлениям](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="4eee7-117">See [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4eee7-118">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="4eee7-118">Sequence Restrictions</span></span>

<span data-ttu-id="4eee7-119">Финдрелатедпродуктс должен быть создан в [таблице инсталлуисекуенце](installuisequence-table.md) и таблицах [инсталлексекутесекуенце](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4eee7-119">FindRelatedProducts should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence](installexecutesequence-table.md) tables.</span></span> <span data-ttu-id="4eee7-120">Установщик предотвращает запуск продуктов Финдрелатед в Инсталлексекутесекуенце, если действие уже выполнялось в Инсталлуисекуенце.</span><span class="sxs-lookup"><span data-stu-id="4eee7-120">The installer prevents FindRelated Products from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span> <span data-ttu-id="4eee7-121">Действие Финдрелатедпродуктс должно следовать перед [действием мигратефеатурестатес](migratefeaturestates-action.md) и [действием RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="4eee7-121">The FindRelatedProducts action must come before the [MigrateFeatureStates action](migratefeaturestates-action.md) and the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4eee7-122">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="4eee7-122">ActionData Messages</span></span>

<span data-ttu-id="4eee7-123">Финдрелатедпродуктс отправляет сообщение данных о действии для каждого связанного продукта, который он обнаруживает в системе.</span><span class="sxs-lookup"><span data-stu-id="4eee7-123">FindRelatedProducts sends an action data message for each related product it detects on the system.</span></span>

 

 



