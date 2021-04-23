---
description: Обновляет объект, передавая указатель на массив двух указателей на списки идентификаторов элементов (PIDL). Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_UPDATEOBJECT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272845"
---
# <a name="sfvm_updateobject-message"></a><span data-ttu-id="c4bba-104">\_Сообщение сфвм UPDATEOBJECT</span><span class="sxs-lookup"><span data-stu-id="c4bba-104">SFVM\_UPDATEOBJECT message</span></span>

<span data-ttu-id="c4bba-105">Обновляет объект, передавая указатель на массив двух указателей на списки идентификаторов элементов (PIDL).</span><span class="sxs-lookup"><span data-stu-id="c4bba-105">Updates an object by passing a pointer to an array of two pointers to item identifier lists (PIDLs).</span></span> <span data-ttu-id="c4bba-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="c4bba-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="c4bba-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4bba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4bba-108">*ппидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4bba-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bba-109">Адрес массива из двух PIDL.</span><span class="sxs-lookup"><span data-stu-id="c4bba-109">The address of an array of two PIDLs.</span></span> <span data-ttu-id="c4bba-110">Первый ПИДЛ является старым ПИДЛ.</span><span class="sxs-lookup"><span data-stu-id="c4bba-110">The first PIDL is the old PIDL.</span></span> <span data-ttu-id="c4bba-111">Второй — копия старого ПИДЛ с обновленной информацией.</span><span class="sxs-lookup"><span data-stu-id="c4bba-111">The second one is a copy of the old PIDL with updated information.</span></span> <span data-ttu-id="c4bba-112">Управление временем существования копии принадлежит к представлению после успешного завершения этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c4bba-112">Control over the copy's lifetime belongs to the view after successful completion of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4bba-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4bba-113">Return value</span></span>

<span data-ttu-id="c4bba-114">Возвращает идентификатор ListView обновленного объекта, если обновление прошло успешно. в противном случае возвращается значение-1.</span><span class="sxs-lookup"><span data-stu-id="c4bba-114">Returns the listview ID of the updated object if the update was successful; otherwise, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4bba-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4bba-115">Remarks</span></span>

<span data-ttu-id="c4bba-116">Если обновление завершилось неудачно, вызывающий объект должен освободить память.</span><span class="sxs-lookup"><span data-stu-id="c4bba-116">If the update was unsuccessful, the caller must free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4bba-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c4bba-117">Requirements</span></span>



| <span data-ttu-id="c4bba-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c4bba-118">Requirement</span></span> | <span data-ttu-id="c4bba-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c4bba-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bba-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4bba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c4bba-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4bba-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c4bba-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4bba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c4bba-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c4bba-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c4bba-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c4bba-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4bba-125"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4bba-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




