---
description: Действие Регистертипелибрариес регистрирует библиотеки типов в системе. Это действие применяется к каждому файлу, на который ссылается таблица TypeLib, для которой запланирована установка.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Действие Регистертипелибрариес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673665"
---
# <a name="registertypelibraries-action"></a><span data-ttu-id="1e6dc-104">Действие Регистертипелибрариес</span><span class="sxs-lookup"><span data-stu-id="1e6dc-104">RegisterTypeLibraries Action</span></span>

<span data-ttu-id="1e6dc-105">Действие Регистертипелибрариес регистрирует библиотеки типов в системе.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-105">The RegisterTypeLibraries action registers type libraries with the system.</span></span> <span data-ttu-id="1e6dc-106">Это действие применяется к каждому файлу, на который ссылается [Таблица typelib](typelib-table.md) , для которой запланирована установка.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-106">This action is applied to each file referred to in the [TypeLib table](typelib-table.md) that is scheduled for install.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="1e6dc-107">Ограничения последовательности</span><span class="sxs-lookup"><span data-stu-id="1e6dc-107">Sequence Restrictions</span></span>

<span data-ttu-id="1e6dc-108">Действие Регистертипелибрариес должно следовать после действия [инсталлфилес](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="1e6dc-108">The RegisterTypeLibraries action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="1e6dc-109">Сообщения Актиондата</span><span class="sxs-lookup"><span data-stu-id="1e6dc-109">ActionData Messages</span></span>



| <span data-ttu-id="1e6dc-110">Поле</span><span class="sxs-lookup"><span data-stu-id="1e6dc-110">Field</span></span> | <span data-ttu-id="1e6dc-111">Описание данных действия</span><span class="sxs-lookup"><span data-stu-id="1e6dc-111">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="1e6dc-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="1e6dc-112">\[1\]</span></span> | <span data-ttu-id="1e6dc-113">[Идентификатор GUID](guid.md) зарегистрированной библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-113">[GUID](guid.md) of registered type library.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1e6dc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e6dc-114">Remarks</span></span>

<span data-ttu-id="1e6dc-115">Действие Регистертипелибрариес требует, чтобы язык библиотеки типов был правильно создан в поле Language таблицы TypeLib.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-115">The RegisterTypeLibraries action requires that the type library language be correctly authored in the Language field of the TypeLib table.</span></span> <span data-ttu-id="1e6dc-116">Неправильная разработка поля Language может привести к тому, что установщик не сможет зарегистрировать библиотеку типов, допустимую иным образом.</span><span class="sxs-lookup"><span data-stu-id="1e6dc-116">Incorrect authoring of the Language field can cause the installer to fail to register an otherwise valid type library.</span></span>

 

 



