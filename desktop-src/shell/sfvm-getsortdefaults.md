---
description: 'Позволяет объекту обратного вызова указывать параметр сортировки по умолчанию. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETSORTDEFAULTS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986101"
---
# <a name="sfvm_getsortdefaults-message"></a><span data-ttu-id="e8ae9-104">\_Сообщение сфвм жетсортдефаултс</span><span class="sxs-lookup"><span data-stu-id="e8ae9-104">SFVM\_GETSORTDEFAULTS message</span></span>

<span data-ttu-id="e8ae9-105">Позволяет объекту обратного вызова указывать параметр сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-105">Allows the callback object to specify a default sorting parameter.</span></span> <span data-ttu-id="e8ae9-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="e8ae9-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="e8ae9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8ae9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8ae9-108">*идиректион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8ae9-108">*iDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ae9-109">Направление сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-109">The default sorting direction.</span></span> <span data-ttu-id="e8ae9-110">Присвойте этому параметру положительное значение для сортировки в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-110">Set this parameter to a positive value to sort in ascending order.</span></span> <span data-ttu-id="e8ae9-111">Присвойте этому параметру нулевое или отрицательное значение для сортировки в убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-111">Set this parameter to zero or a negative value to sort in descending order.</span></span>

</dd> <dt>

<span data-ttu-id="e8ae9-112">*иколумн* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8ae9-112">*iColumn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8ae9-113">Столбец, используемый для сортировки.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-113">The column used for the sort.</span></span> <span data-ttu-id="e8ae9-114">Он будет передан в [**ишеллфолдер:: компареидс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) в младших 16 битах значения *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e8ae9-114">This will be passed to the [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in the lower 16 bits of its *lParam* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8ae9-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8ae9-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e8ae9-116">: **Сфвм \_ жетсортдефаултс** не распознается объектом представления системных папок.</span><span class="sxs-lookup"><span data-stu-id="e8ae9-116">: **SFVM\_GETSORTDEFAULTS** is not recognized by the system folder view object.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8ae9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e8ae9-117">Requirements</span></span>



| <span data-ttu-id="e8ae9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e8ae9-118">Requirement</span></span> | <span data-ttu-id="e8ae9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e8ae9-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ae9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8ae9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ae9-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8ae9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e8ae9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8ae9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ae9-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e8ae9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e8ae9-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e8ae9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8ae9-125"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ae9-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
