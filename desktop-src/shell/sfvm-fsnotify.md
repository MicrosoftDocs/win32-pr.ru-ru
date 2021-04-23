---
description: 'Уведомляет объект обратного вызова о том, что произошло событие, которое влияет на один из его элементов. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_FSNOTIFY (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2021
ms.locfileid: "104997978"
---
# <a name="sfvm_fsnotify-message"></a><span data-ttu-id="1f820-104">\_Сообщение сфвм фснотифи</span><span class="sxs-lookup"><span data-stu-id="1f820-104">SFVM\_FSNOTIFY message</span></span>

<span data-ttu-id="1f820-105">Уведомляет объект обратного вызова о том, что произошло событие, которое влияет на один из его элементов.</span><span class="sxs-lookup"><span data-stu-id="1f820-105">Notifies the callback object that an event has taken place that affects one of its items.</span></span> <span data-ttu-id="1f820-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="1f820-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a><span data-ttu-id="1f820-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f820-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f820-108">*ппидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f820-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f820-109">Указатель ПИДЛ затронутого элемента.</span><span class="sxs-lookup"><span data-stu-id="1f820-109">The pointer of PIDL of the affected item.</span></span>

</dd> <dt>

<span data-ttu-id="1f820-110">*Левент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1f820-110">*lEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f820-111">Значение ШКНЕ, указывающее, какое событие произошло.</span><span class="sxs-lookup"><span data-stu-id="1f820-111">A SHCNE value that indicates which event occurred.</span></span> <span data-ttu-id="1f820-112">Список возможных значений см. в разделе [**шчанженотифи**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span><span class="sxs-lookup"><span data-stu-id="1f820-112">For a list of possible values, see [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f820-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1f820-113">Requirements</span></span>



| <span data-ttu-id="1f820-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1f820-114">Requirement</span></span> | <span data-ttu-id="1f820-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1f820-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1f820-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f820-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1f820-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f820-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1f820-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f820-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1f820-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1f820-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1f820-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1f820-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f820-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f820-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
