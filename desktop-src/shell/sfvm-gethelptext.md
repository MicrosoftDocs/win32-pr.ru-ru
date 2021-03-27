---
description: 'Позволяет объекту обратного вызова указать текст справки для пунктов меню или кнопок панели инструментов. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETHELPTEXT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815480"
---
# <a name="sfvm_gethelptext-message"></a><span data-ttu-id="f0555-104">\_Сообщение сфвм жеселптекст</span><span class="sxs-lookup"><span data-stu-id="f0555-104">SFVM\_GETHELPTEXT message</span></span>

<span data-ttu-id="f0555-105">Позволяет объекту обратного вызова указать текст справки для пунктов меню или кнопок панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="f0555-105">Allows the callback object to specify a help text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="f0555-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="f0555-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="f0555-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0555-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0555-108">*идкмд \_ кчмакс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f0555-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0555-109">Слово с низким приоритетом для этого параметра содержит идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="f0555-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="f0555-110">Слово в высоком порядке содержит количество символов в буфере *псзтекст* .</span><span class="sxs-lookup"><span data-stu-id="f0555-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f0555-111">*псзтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f0555-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0555-112">Строка, заканчивающаяся нулем и содержащая текст справки.</span><span class="sxs-lookup"><span data-stu-id="f0555-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0555-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f0555-113">Requirements</span></span>



| <span data-ttu-id="f0555-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f0555-114">Requirement</span></span> | <span data-ttu-id="f0555-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f0555-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0555-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0555-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f0555-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0555-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f0555-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0555-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f0555-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f0555-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f0555-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f0555-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0555-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0555-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
