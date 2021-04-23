---
description: Предоставляет методы, используемые для инициализации списка недавно использовавшихся (MRU) для объекта автозавершения.
title: Интерфейс Иаклкустоммру
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997679"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="8b75e-103">Интерфейс Иаклкустоммру</span><span class="sxs-lookup"><span data-stu-id="8b75e-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="8b75e-104">Предоставляет методы, используемые для инициализации списка недавно использовавшихся (MRU) для объекта автозавершения.</span><span class="sxs-lookup"><span data-stu-id="8b75e-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="8b75e-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="8b75e-105">Members</span></span>

<span data-ttu-id="8b75e-106">Интерфейс **иаклкустоммру** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b75e-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b75e-107">**Иаклкустоммру** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8b75e-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="8b75e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="8b75e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b75e-109">Методы</span><span class="sxs-lookup"><span data-stu-id="8b75e-109">Methods</span></span>

<span data-ttu-id="8b75e-110">Интерфейс **иаклкустоммру** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8b75e-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="8b75e-111">Метод</span><span class="sxs-lookup"><span data-stu-id="8b75e-111">Method</span></span>                                             | <span data-ttu-id="8b75e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8b75e-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="8b75e-113">**аддмрустринг**</span><span class="sxs-lookup"><span data-stu-id="8b75e-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="8b75e-114">Добавляет запись в список MRU.</span><span class="sxs-lookup"><span data-stu-id="8b75e-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="8b75e-115">**Инициализация**</span><span class="sxs-lookup"><span data-stu-id="8b75e-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="8b75e-116">Загружает список строк из реестра в список MRU.</span><span class="sxs-lookup"><span data-stu-id="8b75e-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8b75e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8b75e-117">Requirements</span></span>



| <span data-ttu-id="8b75e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8b75e-118">Requirement</span></span> | <span data-ttu-id="8b75e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8b75e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8b75e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b75e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8b75e-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8b75e-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8b75e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b75e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8b75e-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b75e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
