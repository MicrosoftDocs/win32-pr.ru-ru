---
description: Удаляет объект из представления оболочки. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_REMOVEOBJECT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986104"
---
# <a name="sfvm_removeobject-message"></a><span data-ttu-id="36db1-104">\_Сообщение сфвм ремовеобжект</span><span class="sxs-lookup"><span data-stu-id="36db1-104">SFVM\_REMOVEOBJECT message</span></span>

<span data-ttu-id="36db1-105">Удаляет объект из представления оболочки.</span><span class="sxs-lookup"><span data-stu-id="36db1-105">Removes an object from the shell view.</span></span> <span data-ttu-id="36db1-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="36db1-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="36db1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="36db1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36db1-108">*Пидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="36db1-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="36db1-109">ПИДЛ объекта, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="36db1-109">PIDL of the object to remove.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36db1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36db1-110">Return value</span></span>

<span data-ttu-id="36db1-111">Возвращает индекс элемента, который был удален, если найден элемент, соответствующий указанному ПИДЛ. в противном случае возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="36db1-111">Returns the index of the item that was removed if an item matching the specified PIDL was found; otherwise, returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="36db1-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="36db1-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="36db1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="36db1-113">Requirements</span></span>



| <span data-ttu-id="36db1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="36db1-114">Requirement</span></span> | <span data-ttu-id="36db1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="36db1-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36db1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36db1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36db1-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36db1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="36db1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36db1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36db1-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="36db1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="36db1-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="36db1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="36db1-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="36db1-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




