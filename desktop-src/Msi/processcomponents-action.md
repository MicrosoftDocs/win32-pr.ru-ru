---
description: Действие Процесскомпонентс регистрирует и отменяет регистрацию компонентов, их путей их ключей и клиентов компонентов.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Действие Процесскомпонентс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651056"
---
# <a name="processcomponents-action"></a><span data-ttu-id="ee440-103">Действие Процесскомпонентс</span><span class="sxs-lookup"><span data-stu-id="ee440-103">ProcessComponents Action</span></span>

<span data-ttu-id="ee440-104">Действие Процесскомпонентс регистрирует и отменяет регистрацию компонентов, их путей их ключей и клиентов компонентов.</span><span class="sxs-lookup"><span data-stu-id="ee440-104">The ProcessComponents action registers and unregisters components, their key paths, and the component clients.</span></span> <span data-ttu-id="ee440-105">Действие Процесскомпонентс запрашивает ключевой столбец [таблицы Component](component-table.md) для определения кэйпасс.</span><span class="sxs-lookup"><span data-stu-id="ee440-105">The ProcessComponents action queries the KeyPath column of the [Component table](component-table.md) to determine keypaths.</span></span> <span data-ttu-id="ee440-106">Эта регистрация используется [**мсижеткомпонентпас**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) для возврата пути к компоненту для клиента продукта.</span><span class="sxs-lookup"><span data-stu-id="ee440-106">This registration is used by [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to return the path of a component for a product client.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ee440-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="ee440-107">Sequence Restrictions</span></span>

<span data-ttu-id="ee440-108">Действие Процесскомпонентс должно следовать после действия [инсталлинитиализе](installinitialize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="ee440-108">The ProcessComponents action must come after the [InstallInitialize](installinitialize-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ee440-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="ee440-109">ActionData Messages</span></span>

<span data-ttu-id="ee440-110">Для каждого регистрируемого компонента.</span><span class="sxs-lookup"><span data-stu-id="ee440-110">For each component being registered.</span></span>



| <span data-ttu-id="ee440-111">Поле</span><span class="sxs-lookup"><span data-stu-id="ee440-111">Field</span></span> | <span data-ttu-id="ee440-112">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="ee440-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="ee440-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ee440-113">\[1\]</span></span> | <span data-ttu-id="ee440-114">ProductId</span><span class="sxs-lookup"><span data-stu-id="ee440-114">ProductId</span></span>                       |
| <span data-ttu-id="ee440-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ee440-115">\[2\]</span></span> | <span data-ttu-id="ee440-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="ee440-116">ComponentId</span></span>                     |
| <span data-ttu-id="ee440-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="ee440-117">\[3\]</span></span> | <span data-ttu-id="ee440-118">Путь к ключу для компонента.</span><span class="sxs-lookup"><span data-stu-id="ee440-118">The key path for the component.</span></span> |



 

<span data-ttu-id="ee440-119">Для каждого компонента выполняется отмена регистрации.</span><span class="sxs-lookup"><span data-stu-id="ee440-119">For each component being unregistered.</span></span>



| <span data-ttu-id="ee440-120">Поле</span><span class="sxs-lookup"><span data-stu-id="ee440-120">Field</span></span> | <span data-ttu-id="ee440-121">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="ee440-121">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="ee440-122">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ee440-122">\[1\]</span></span> | <span data-ttu-id="ee440-123">ProductId</span><span class="sxs-lookup"><span data-stu-id="ee440-123">ProductId</span></span>                  |
| <span data-ttu-id="ee440-124">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ee440-124">\[2\]</span></span> | <span data-ttu-id="ee440-125">ComponentId</span><span class="sxs-lookup"><span data-stu-id="ee440-125">ComponentId</span></span>                |



 

 

 



