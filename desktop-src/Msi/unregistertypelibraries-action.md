---
description: Действие Унрегистертипелибрариес отменяет регистрацию библиотек типов в системе. Это действие применяется к каждому файлу, указанному в таблице TypeLib, запускаемой для удаления.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Действие Унрегистертипелибрариес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651186"
---
# <a name="unregistertypelibraries-action"></a><span data-ttu-id="62d99-104">Действие Унрегистертипелибрариес</span><span class="sxs-lookup"><span data-stu-id="62d99-104">UnregisterTypeLibraries Action</span></span>

<span data-ttu-id="62d99-105">Действие Унрегистертипелибрариес отменяет регистрацию библиотек типов в системе.</span><span class="sxs-lookup"><span data-stu-id="62d99-105">The UnregisterTypeLibraries action unregisters type libraries from the system.</span></span> <span data-ttu-id="62d99-106">Это действие применяется к каждому файлу, указанному в таблице [typelib](typelib-table.md) , запускаемой для удаления.</span><span class="sxs-lookup"><span data-stu-id="62d99-106">This action is applied to each file listed in the [TypeLib](typelib-table.md) table that is triggered to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="62d99-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="62d99-107">Sequence Restrictions</span></span>

<span data-ttu-id="62d99-108">Действие Унрегистертипелибрариес должно следовать перед действием [ремовефилес](removefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="62d99-108">The UnregisterTypeLibraries action must come before the [RemoveFiles](removefiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="62d99-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="62d99-109">ActionData Messages</span></span>



| <span data-ttu-id="62d99-110">Поле</span><span class="sxs-lookup"><span data-stu-id="62d99-110">Field</span></span> | <span data-ttu-id="62d99-111">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="62d99-111">Description of action data</span></span>                        |
|-------|---------------------------------------------------|
| <span data-ttu-id="62d99-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="62d99-112">\[1\]</span></span> | <span data-ttu-id="62d99-113">[Идентификатор GUID](guid.md) незарегистрированной библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="62d99-113">[GUID](guid.md) of an unregistered type library.</span></span> |



 

 

 



