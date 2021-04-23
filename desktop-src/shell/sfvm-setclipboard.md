---
description: Уведомляет Ишеллвиев, когда один из его объектов помещается в буфер обмена в результате выполнения команды меню. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_SETCLIPBOARD (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997946"
---
# <a name="sfvm_setclipboard-message"></a><span data-ttu-id="a02b5-104">\_Сообщение сфвм сетклипбоард</span><span class="sxs-lookup"><span data-stu-id="a02b5-104">SFVM\_SETCLIPBOARD message</span></span>

<span data-ttu-id="a02b5-105">Уведомляет [**ишеллвиев**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) , когда один из его объектов помещается в буфер обмена в результате выполнения команды меню.</span><span class="sxs-lookup"><span data-stu-id="a02b5-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) when one of its objects is placed on the Clipboard as a result of a menu command.</span></span> <span data-ttu-id="a02b5-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="a02b5-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a><span data-ttu-id="a02b5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a02b5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a02b5-108">*двеффект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a02b5-108">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02b5-109">Use (WPARAM)-2, если элемент вырезан в буфер обмена или (WPARAM)-3, если элемент копируется в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="a02b5-109">Use (WPARAM)-2 if the item is being cut to the Clipboard or (WPARAM)-3 if the item is being copied to the Clipboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a02b5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a02b5-110">Return value</span></span>

<span data-ttu-id="a02b5-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a02b5-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a02b5-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="a02b5-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a02b5-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a02b5-113">Requirements</span></span>



| <span data-ttu-id="a02b5-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a02b5-114">Requirement</span></span> | <span data-ttu-id="a02b5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a02b5-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a02b5-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a02b5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a02b5-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a02b5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a02b5-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a02b5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a02b5-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a02b5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a02b5-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a02b5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a02b5-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="a02b5-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




