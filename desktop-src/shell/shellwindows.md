---
description: Представляет коллекцию открытых окон, принадлежащих оболочке. Методы, связанные с этими объектами, могут управлять и выполнять команды в оболочке и получать другие объекты, связанные с оболочкой.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Объект Шеллвиндовс (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985565"
---
# <a name="shellwindows-object"></a><span data-ttu-id="3bc6f-104">Объект Шеллвиндовс</span><span class="sxs-lookup"><span data-stu-id="3bc6f-104">ShellWindows object</span></span>

<span data-ttu-id="3bc6f-105">Представляет коллекцию открытых окон, принадлежащих оболочке.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-105">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="3bc6f-106">Методы, связанные с этими объектами, могут управлять и выполнять команды в оболочке и получать другие объекты, связанные с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-106">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="3bc6f-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="3bc6f-107">Members</span></span>

<span data-ttu-id="3bc6f-108">Объект **шеллвиндовс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3bc6f-108">The **ShellWindows** object has these types of members:</span></span>

-   [<span data-ttu-id="3bc6f-109">Методы</span><span class="sxs-lookup"><span data-stu-id="3bc6f-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3bc6f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3bc6f-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3bc6f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="3bc6f-111">Methods</span></span>

<span data-ttu-id="3bc6f-112">Объект **шеллвиндовс** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-112">The **ShellWindows** object has these methods.</span></span>



| <span data-ttu-id="3bc6f-113">Метод</span><span class="sxs-lookup"><span data-stu-id="3bc6f-113">Method</span></span>                                                 | <span data-ttu-id="3bc6f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3bc6f-114">Description</span></span>                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3bc6f-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3bc6f-115">**\_NewEnum**</span></span>](shellwindows--newenum-method-7ral.md) | <span data-ttu-id="3bc6f-116">Создает и возвращает новый объект **шеллвиндовс** , являющийся копией этого объекта **шеллвиндовс** .</span><span class="sxs-lookup"><span data-stu-id="3bc6f-116">Creates and returns a new **ShellWindows** object that is a copy of this **ShellWindows** object.</span></span><br/>        |
| [<span data-ttu-id="3bc6f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3bc6f-117">**Item**</span></span>](shellwindows-item.md)                      | <span data-ttu-id="3bc6f-118">Извлекает объект [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) , представляющий окно оболочки.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-118">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3bc6f-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="3bc6f-119">Properties</span></span>

<span data-ttu-id="3bc6f-120">Объект **шеллвиндовс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-120">The **ShellWindows** object has these properties.</span></span>



| <span data-ttu-id="3bc6f-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="3bc6f-121">Property</span></span>                                       | <span data-ttu-id="3bc6f-122">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3bc6f-122">Access type</span></span>          | <span data-ttu-id="3bc6f-123">Описание</span><span class="sxs-lookup"><span data-stu-id="3bc6f-123">Description</span></span>                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="3bc6f-124">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="3bc6f-124">**Count**</span></span>](shellwindows-count.md)<br/> | <span data-ttu-id="3bc6f-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3bc6f-125">Read-only</span></span><br/> | <span data-ttu-id="3bc6f-126">Содержит число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="3bc6f-126">Contains the number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3bc6f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="3bc6f-127">Requirements</span></span>



| <span data-ttu-id="3bc6f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="3bc6f-128">Requirement</span></span> | <span data-ttu-id="3bc6f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="3bc6f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc6f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3bc6f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc6f-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3bc6f-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3bc6f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3bc6f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc6f-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3bc6f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3bc6f-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3bc6f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bc6f-135"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bc6f-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="3bc6f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3bc6f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bc6f-137"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="3bc6f-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
