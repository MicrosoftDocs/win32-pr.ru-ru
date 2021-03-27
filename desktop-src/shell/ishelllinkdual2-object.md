---
description: Расширяет объект Шелллинкобжект и поддерживает одно дополнительное свойство.
title: Объект IShellLinkDual2 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 8a63552c-6bce-4583-8df8-a7f7731b35eb
ms.openlocfilehash: 0209b57d621d4335a6ef703dadaef3dd5c307c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991313"
---
# <a name="ishelllinkdual2-object"></a><span data-ttu-id="18fcc-103">Объект IShellLinkDual2</span><span class="sxs-lookup"><span data-stu-id="18fcc-103">IShellLinkDual2 object</span></span>

<span data-ttu-id="18fcc-104">Расширяет объект [**шелллинкобжект**](shelllinkobject-object.md) и поддерживает одно дополнительное свойство.</span><span class="sxs-lookup"><span data-stu-id="18fcc-104">Extends the [**ShellLinkObject**](shelllinkobject-object.md) object and supports one additional property.</span></span>

## <a name="members"></a><span data-ttu-id="18fcc-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="18fcc-105">Members</span></span>

<span data-ttu-id="18fcc-106">Объект **IShellLinkDual2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18fcc-106">The **IShellLinkDual2** object has these types of members:</span></span>

-   [<span data-ttu-id="18fcc-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="18fcc-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18fcc-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="18fcc-108">Properties</span></span>

<span data-ttu-id="18fcc-109">Объект **IShellLinkDual2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18fcc-109">The **IShellLinkDual2** object has these properties.</span></span>



| <span data-ttu-id="18fcc-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="18fcc-110">Property</span></span>                                            | <span data-ttu-id="18fcc-111">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="18fcc-111">Access type</span></span>          | <span data-ttu-id="18fcc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="18fcc-112">Description</span></span>                                   |
|:----------------------------------------------------|:---------------------|:----------------------------------------------|
| [<span data-ttu-id="18fcc-113">**Цель**</span><span class="sxs-lookup"><span data-stu-id="18fcc-113">**Target**</span></span>](ishelllinkdual2-target.md)<br/> | <span data-ttu-id="18fcc-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="18fcc-114">Read-only</span></span><br/> | <span data-ttu-id="18fcc-115">Содержит целевой объект объекта Link.</span><span class="sxs-lookup"><span data-stu-id="18fcc-115">Contains the link object's target.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18fcc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="18fcc-116">Requirements</span></span>



| <span data-ttu-id="18fcc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="18fcc-117">Requirement</span></span> | <span data-ttu-id="18fcc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="18fcc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18fcc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18fcc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="18fcc-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="18fcc-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="18fcc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18fcc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="18fcc-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18fcc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="18fcc-123">Header</span><span class="sxs-lookup"><span data-stu-id="18fcc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="18fcc-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="18fcc-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="18fcc-125">IDL</span><span class="sxs-lookup"><span data-stu-id="18fcc-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18fcc-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18fcc-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="18fcc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="18fcc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18fcc-128"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="18fcc-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




