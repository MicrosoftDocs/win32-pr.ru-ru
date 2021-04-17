---
description: Каждая установщик Windowsная функция использует один или несколько установщик Windows компонентов, а компоненты могут совместно использовать компоненты.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Указание отношений Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673338"
---
# <a name="specifying-feature-component-relationships"></a><span data-ttu-id="30d1c-103">Указание отношений Feature-Component</span><span class="sxs-lookup"><span data-stu-id="30d1c-103">Specifying Feature-Component Relationships</span></span>

<span data-ttu-id="30d1c-104">Каждая [установщик Windowsная функция](windows-installer-features.md) использует один или несколько [установщик Windows компонентов](windows-installer-components.md), а компоненты могут совместно использовать компоненты.</span><span class="sxs-lookup"><span data-stu-id="30d1c-104">Each [Windows Installer Feature](windows-installer-features.md) uses one or more [Windows Installer Components](windows-installer-components.md), and features may share components.</span></span> <span data-ttu-id="30d1c-105">В [таблице феатурекомпонентс](featurecomponents-table.md) определяется связь между компонентами и компонентами.</span><span class="sxs-lookup"><span data-stu-id="30d1c-105">The [FeatureComponents table](featurecomponents-table.md) defines the relationship between features and components.</span></span> <span data-ttu-id="30d1c-106">См. раздел [основные таблицы](core-tables-group.md) и [компоненты и](components-and-features.md) компоненты в обзоре установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="30d1c-106">See the [Core Tables Group](core-tables-group.md) and [Components and Features](components-and-features.md) in the Windows Installer overview.</span></span> <span data-ttu-id="30d1c-107">В этом разделе вы добавите сведения в таблицу Феатурекомпонентс образца Notepad.</span><span class="sxs-lookup"><span data-stu-id="30d1c-107">In this section you add information to the FeatureComponents table of the Notepad sample.</span></span>

<span data-ttu-id="30d1c-108">Используйте редактор базы данных, чтобы открыть MNP2000.msi и ввести следующие данные в пустую таблицу Феатурекомпонентс.</span><span class="sxs-lookup"><span data-stu-id="30d1c-108">Use your database editor to open MNP2000.msi and enter the following data into the empty FeatureComponents table.</span></span>

[<span data-ttu-id="30d1c-109">Таблица Феатурекомпонентс</span><span class="sxs-lookup"><span data-stu-id="30d1c-109">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="30d1c-110">Функция\_</span><span class="sxs-lookup"><span data-stu-id="30d1c-110">Feature\_</span></span> | <span data-ttu-id="30d1c-111">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="30d1c-111">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="30d1c-112">Команды</span><span class="sxs-lookup"><span data-stu-id="30d1c-112">Baseball</span></span>  | <span data-ttu-id="30d1c-113">Команды</span><span class="sxs-lookup"><span data-stu-id="30d1c-113">Baseball</span></span>    |
| <span data-ttu-id="30d1c-114">Концерт</span><span class="sxs-lookup"><span data-stu-id="30d1c-114">Concert</span></span>   | <span data-ttu-id="30d1c-115">Концерт</span><span class="sxs-lookup"><span data-stu-id="30d1c-115">Concert</span></span>     |
| <span data-ttu-id="30d1c-116">Dance</span><span class="sxs-lookup"><span data-stu-id="30d1c-116">Dance</span></span>     | <span data-ttu-id="30d1c-117">Dance</span><span class="sxs-lookup"><span data-stu-id="30d1c-117">Dance</span></span>       |
| <span data-ttu-id="30d1c-118">Футбол</span><span class="sxs-lookup"><span data-stu-id="30d1c-118">Football</span></span>  | <span data-ttu-id="30d1c-119">Футбол</span><span class="sxs-lookup"><span data-stu-id="30d1c-119">Football</span></span>    |
| <span data-ttu-id="30d1c-120">Справка</span><span class="sxs-lookup"><span data-stu-id="30d1c-120">Help</span></span>      | <span data-ttu-id="30d1c-121">Справка</span><span class="sxs-lookup"><span data-stu-id="30d1c-121">Help</span></span>        |
| <span data-ttu-id="30d1c-122">Январь</span><span class="sxs-lookup"><span data-stu-id="30d1c-122">January</span></span>   | <span data-ttu-id="30d1c-123">Январь</span><span class="sxs-lookup"><span data-stu-id="30d1c-123">January</span></span>     |
| <span data-ttu-id="30d1c-124">невеарс</span><span class="sxs-lookup"><span data-stu-id="30d1c-124">NewYears</span></span>  | <span data-ttu-id="30d1c-125">невеарс</span><span class="sxs-lookup"><span data-stu-id="30d1c-125">NewYears</span></span>    |
| <span data-ttu-id="30d1c-126">Блокнот</span><span class="sxs-lookup"><span data-stu-id="30d1c-126">Notepad</span></span>   | <span data-ttu-id="30d1c-127">Блокнот</span><span class="sxs-lookup"><span data-stu-id="30d1c-127">Notepad</span></span>     |
| <span data-ttu-id="30d1c-128">Readme</span><span class="sxs-lookup"><span data-stu-id="30d1c-128">Readme</span></span>    | <span data-ttu-id="30d1c-129">Блокнот</span><span class="sxs-lookup"><span data-stu-id="30d1c-129">Notepad</span></span>     |



 

[<span data-ttu-id="30d1c-130">Продолжить</span><span class="sxs-lookup"><span data-stu-id="30d1c-130">Continue</span></span>](adding-registry-information.md)

 

 



