---
description: 'Позволяет объекту обратного вызова указать текст подсказки для элементов меню или кнопок панели инструментов. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Сообщение SFVM_GETTOOLTIPTEXT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999527"
---
# <a name="sfvm_gettooltiptext-message"></a><span data-ttu-id="8269c-104">\_Сообщение сфвм жеттултиптекст</span><span class="sxs-lookup"><span data-stu-id="8269c-104">SFVM\_GETTOOLTIPTEXT message</span></span>

<span data-ttu-id="8269c-105">Позволяет объекту обратного вызова указать текст подсказки для элементов меню или кнопок панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="8269c-105">Allows the callback object to specify a tooltip text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="8269c-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="8269c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="8269c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8269c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8269c-108">*идкмд \_ кчмакс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8269c-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8269c-109">Слово с низким приоритетом для этого параметра содержит идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="8269c-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="8269c-110">Слово в высоком порядке содержит количество символов в буфере *псзтекст* .</span><span class="sxs-lookup"><span data-stu-id="8269c-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8269c-111">*псзтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8269c-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8269c-112">Строка, заканчивающаяся нулем и содержащая текст справки.</span><span class="sxs-lookup"><span data-stu-id="8269c-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8269c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8269c-113">Requirements</span></span>



| <span data-ttu-id="8269c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8269c-114">Requirement</span></span> | <span data-ttu-id="8269c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8269c-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8269c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8269c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8269c-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8269c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8269c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8269c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8269c-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8269c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8269c-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8269c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8269c-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="8269c-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
