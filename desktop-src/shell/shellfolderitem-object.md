---
description: Расширяет объект FolderItem. В дополнение к свойствам и методам, поддерживаемым FolderItem, Шеллфолдеритем имеет два дополнительных метода.
title: Объект Шеллфолдеритем (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: 84e230e295a956f3f83833a577b47be1e46873a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985877"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="8d054-104">Объект Шеллфолдеритем</span><span class="sxs-lookup"><span data-stu-id="8d054-104">ShellFolderItem object</span></span>

<span data-ttu-id="8d054-105">Расширяет объект [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8d054-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="8d054-106">В дополнение к свойствам и методам, поддерживаемым **FolderItem**, **шеллфолдеритем** имеет два дополнительных метода.</span><span class="sxs-lookup"><span data-stu-id="8d054-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="8d054-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="8d054-107">Members</span></span>

<span data-ttu-id="8d054-108">Объект **шеллфолдеритем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8d054-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="8d054-109">Методы</span><span class="sxs-lookup"><span data-stu-id="8d054-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8d054-110">Методы</span><span class="sxs-lookup"><span data-stu-id="8d054-110">Methods</span></span>

<span data-ttu-id="8d054-111">Объект **шеллфолдеритем** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="8d054-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="8d054-112">Метод</span><span class="sxs-lookup"><span data-stu-id="8d054-112">Method</span></span>                                                       | <span data-ttu-id="8d054-113">Описание</span><span class="sxs-lookup"><span data-stu-id="8d054-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8d054-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="8d054-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="8d054-115">Возвращает значение свойства из набора свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="8d054-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="8d054-116">Свойство может быть задано либо по имени, либо идентификатором формата набора свойств (FMTID) и идентификатором свойства (PID).</span><span class="sxs-lookup"><span data-stu-id="8d054-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="8d054-117">**инвокевербекс**</span><span class="sxs-lookup"><span data-stu-id="8d054-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="8d054-118">Выполняет команду для элемента оболочки.</span><span class="sxs-lookup"><span data-stu-id="8d054-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8d054-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8d054-119">Requirements</span></span>



| <span data-ttu-id="8d054-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8d054-120">Requirement</span></span> | <span data-ttu-id="8d054-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8d054-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d054-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d054-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d054-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d054-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8d054-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d054-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d054-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d054-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8d054-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8d054-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d054-127"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d054-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8d054-128">IDL</span><span class="sxs-lookup"><span data-stu-id="8d054-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d054-129"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d054-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8d054-130">DLL</span><span class="sxs-lookup"><span data-stu-id="8d054-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d054-131"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="8d054-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




