---
description: Извлекает массив указателей на списки идентификаторов элементов (PIDL) для всех выбранных объектов. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_GETSELECTEDOBJECTS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913315"
---
# <a name="sfvm_getselectedobjects-message"></a><span data-ttu-id="b0227-104">\_Сообщение сфвм жетселектедобжектс</span><span class="sxs-lookup"><span data-stu-id="b0227-104">SFVM\_GETSELECTEDOBJECTS message</span></span>

<span data-ttu-id="b0227-105">Извлекает массив указателей на списки идентификаторов элементов (PIDL) для всех выбранных объектов.</span><span class="sxs-lookup"><span data-stu-id="b0227-105">Retrieves an array of pointers to item identifier lists (PIDLs) for all selected objects.</span></span> <span data-ttu-id="b0227-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="b0227-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="b0227-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0227-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0227-108">*ппидл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b0227-108">*ppidl* \[out\]</span></span>
</dt> <dd><span data-ttu-id="b0227-109">Адрес массива PIDL объектов, выбранных в данный момент.</span><span class="sxs-lookup"><span data-stu-id="b0227-109">The address of an array of PIDLs of currently selected objects.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0227-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0227-110">Return value</span></span>

<span data-ttu-id="b0227-111">Возвращает число элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="b0227-111">Returns the number of items in the array.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0227-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0227-112">Remarks</span></span>

<span data-ttu-id="b0227-113">По завершении необходимо вызвать [**илфри**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) для каждого члена массива, чтобы освободить память.</span><span class="sxs-lookup"><span data-stu-id="b0227-113">When finished, you should call [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) on each member of the array to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0227-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b0227-114">Requirements</span></span>



| <span data-ttu-id="b0227-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b0227-115">Requirement</span></span> | <span data-ttu-id="b0227-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b0227-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0227-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0227-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b0227-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0227-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b0227-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0227-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b0227-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b0227-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b0227-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b0227-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0227-122"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0227-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




