---
description: Получает маркер меню для текущего окна.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Сообщение MN_GETHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264558"
---
# <a name="mn_gethmenu-message"></a><span data-ttu-id="f0e11-103">\_Сообщение ЖЕСМЕНУ MN</span><span class="sxs-lookup"><span data-stu-id="f0e11-103">MN\_GETHMENU message</span></span>

<span data-ttu-id="f0e11-104">Получает маркер меню для текущего окна.</span><span class="sxs-lookup"><span data-stu-id="f0e11-104">Retrieves the menu handle for the current window.</span></span>


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a><span data-ttu-id="f0e11-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0e11-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e11-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0e11-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e11-107">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="f0e11-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f0e11-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0e11-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0e11-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="f0e11-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e11-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0e11-110">Return value</span></span>

<span data-ttu-id="f0e11-111">Тип: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="f0e11-111">Type: **HMENU**</span></span>

<span data-ttu-id="f0e11-112">В случае успеха возвращаемое значение является **HMENU** для текущего окна.</span><span class="sxs-lookup"><span data-stu-id="f0e11-112">If successful, the return value is the **HMENU** for the current window.</span></span> <span data-ttu-id="f0e11-113">В случае сбоя возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="f0e11-113">If it fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e11-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f0e11-114">Requirements</span></span>



| <span data-ttu-id="f0e11-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f0e11-115">Requirement</span></span> | <span data-ttu-id="f0e11-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f0e11-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0e11-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0e11-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0e11-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0e11-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f0e11-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0e11-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0e11-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0e11-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0e11-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f0e11-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0e11-122"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0e11-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 




