---
description: Чтобы применить основное обновление с помощью установщик Windows, в исходном пакете установки продукта необходимо указать свойство UpgradeCode, как описано в разделе Подготовка приложения к будущим основным обновлениям, а в пакете обновления должна быть обновлена таблица.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Обновление таблицы обновления для обновления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156042"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a><span data-ttu-id="af2fc-103">Обновление таблицы обновления для обновления</span><span class="sxs-lookup"><span data-stu-id="af2fc-103">Updating Upgrade Table for an Upgrade</span></span>

<span data-ttu-id="af2fc-104">Чтобы применить основное обновление с помощью установщик Windows, в исходном пакете установки продукта необходимо указать свойство [**UpgradeCode**](upgradecode.md) , как описано в разделе [Подготовка приложения к будущим основным обновлениям](preparing-an-application-for-future-major-upgrades.md), а в пакете обновления должна быть [обновлена таблица](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="af2fc-104">To apply a major upgrade using Windows Installer, the original product installation package must specify an [**UpgradeCode**](upgradecode.md) Property, described in [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md), and the upgrade package must have an [Upgrade table](upgrade-table.md).</span></span>

<span data-ttu-id="af2fc-105">Дополнительные сведения об основных обновлениях см. в статье [основные обновления](major-upgrades.md) в разделе [Установка исправлений и обновления](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="af2fc-105">For more information about major upgrades, see [Major Upgrades](major-upgrades.md) in [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="af2fc-106">Пакету установки MNP2000.msi было присвоено свойство [**UpgradeCode**](upgradecode.md) , как описано в разделе [Указание свойств](specifying-properties.md).</span><span class="sxs-lookup"><span data-stu-id="af2fc-106">The installation package of MNP2000.msi was assigned an [**UpgradeCode**](upgradecode.md) property, as described in the section [Specifying Properties](specifying-properties.md).</span></span>

<span data-ttu-id="af2fc-107">Установщик Windows применяет обновление, если пользователь уже установил 1,0 в версии 1,4 (включительно) на английском языке MNP2000.</span><span class="sxs-lookup"><span data-stu-id="af2fc-107">Windows Installer applies the upgrade if the user has already installed the 1.0 to 1.4 versions (inclusive) of English language MNP2000.</span></span> <span data-ttu-id="af2fc-108">Установщик Windows переносит все настройки компонентов исходного продукта в обновленный продукт.</span><span class="sxs-lookup"><span data-stu-id="af2fc-108">Windows Installer migrates all of the original product's feature settings to the upgraded product.</span></span> <span data-ttu-id="af2fc-109">Установщик удаляет файлы, относящиеся к исходным продуктам, которые не используются при обновлении продукта.</span><span class="sxs-lookup"><span data-stu-id="af2fc-109">The installer removes the files belonging to the original products not being used by the product's upgrade.</span></span>

<span data-ttu-id="af2fc-110">Если ваша копия MNP2001.msi не содержит [таблицу обновления](upgrade-table.md), используйте Orca или другой редактор таблиц, чтобы импортировать пустую таблицу обновления в базу данных из Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="af2fc-110">If your copy of MNP2001.msi does not include an [Upgrade table](upgrade-table.md), use Orca, or another table editor, to import an empty Upgrade table into the database from Schema.msi.</span></span> <span data-ttu-id="af2fc-111">Пакет SDK предоставляет копию Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="af2fc-111">The SDK provides a copy of Schema.msi.</span></span> <span data-ttu-id="af2fc-112">Используйте редактор базы данных, чтобы открыть MNP2001.msi и ввести следующие данные в пустую таблицу обновления.</span><span class="sxs-lookup"><span data-stu-id="af2fc-112">Use your database editor to open MNP2001.msi and enter the following data into the empty Upgrade table.</span></span>



| <span data-ttu-id="af2fc-113">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="af2fc-113">UpgradeCode</span></span>                            | <span data-ttu-id="af2fc-114">версионмин</span><span class="sxs-lookup"><span data-stu-id="af2fc-114">VersionMin</span></span> | <span data-ttu-id="af2fc-115">версионмакс</span><span class="sxs-lookup"><span data-stu-id="af2fc-115">VersionMax</span></span> | <span data-ttu-id="af2fc-116">Язык</span><span class="sxs-lookup"><span data-stu-id="af2fc-116">Language</span></span> | <span data-ttu-id="af2fc-117">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="af2fc-117">Attributes</span></span> | <span data-ttu-id="af2fc-118">Удалить</span><span class="sxs-lookup"><span data-stu-id="af2fc-118">Remove</span></span> | <span data-ttu-id="af2fc-119">актионпроперти</span><span class="sxs-lookup"><span data-stu-id="af2fc-119">ActionProperty</span></span> |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| <span data-ttu-id="af2fc-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="af2fc-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> | <span data-ttu-id="af2fc-121">01.00.0000</span><span class="sxs-lookup"><span data-stu-id="af2fc-121">01.00.0000</span></span> | <span data-ttu-id="af2fc-122">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="af2fc-122">01.40.0000</span></span> | <span data-ttu-id="af2fc-123">1033</span><span class="sxs-lookup"><span data-stu-id="af2fc-123">1033</span></span>     | <span data-ttu-id="af2fc-124">769</span><span class="sxs-lookup"><span data-stu-id="af2fc-124">769</span></span>        |        | <span data-ttu-id="af2fc-125">олдаппфаунд</span><span class="sxs-lookup"><span data-stu-id="af2fc-125">OLDAPPFOUND</span></span>    |



 

[<span data-ttu-id="af2fc-126">Продолжить</span><span class="sxs-lookup"><span data-stu-id="af2fc-126">Continue</span></span>](updating-properties-for-an-upgrade.md)

 

 



