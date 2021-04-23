---
description: Уведомляет Ишеллвиев о необходимости переупорядочения элементов. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_REARRANGE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081544"
---
# <a name="sfvm_rearrange-message"></a><span data-ttu-id="48cfc-104">СФВМ \_ изменить расположение сообщения</span><span class="sxs-lookup"><span data-stu-id="48cfc-104">SFVM\_REARRANGE message</span></span>

<span data-ttu-id="48cfc-105">Уведомляет [**ишеллвиев**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) о необходимости переупорядочения элементов.</span><span class="sxs-lookup"><span data-stu-id="48cfc-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) to rearrange its items.</span></span> <span data-ttu-id="48cfc-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="48cfc-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a><span data-ttu-id="48cfc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="48cfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48cfc-108">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="48cfc-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48cfc-109">Передается в [**ишеллфолдер:: компареидс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span><span class="sxs-lookup"><span data-stu-id="48cfc-109">Passed to [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span></span> <span data-ttu-id="48cfc-110">Дополнительные сведения об этом параметре см. в разделе [**ишеллфолдер:: компареидс**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) .</span><span class="sxs-lookup"><span data-stu-id="48cfc-110">See [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) for more information on this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48cfc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="48cfc-111">Return value</span></span>

<span data-ttu-id="48cfc-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="48cfc-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="48cfc-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="48cfc-113">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="48cfc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="48cfc-114">Requirements</span></span>



| <span data-ttu-id="48cfc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="48cfc-115">Requirement</span></span> | <span data-ttu-id="48cfc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="48cfc-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="48cfc-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48cfc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="48cfc-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="48cfc-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="48cfc-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48cfc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="48cfc-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="48cfc-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="48cfc-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="48cfc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="48cfc-122"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="48cfc-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




