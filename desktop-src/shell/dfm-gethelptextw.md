---
description: DFM_GETHELPTEXTW сообщение — позволяет объекту обратного вызова указать строку текста справки.
title: Сообщение DFM_GETHELPTEXTW (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097042"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="8c6c0-103">\_Сообщение DFM жеселптекств</span><span class="sxs-lookup"><span data-stu-id="8c6c0-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="8c6c0-104">Позволяет объекту обратного вызова указать строку текста справки.</span><span class="sxs-lookup"><span data-stu-id="8c6c0-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="8c6c0-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c6c0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c6c0-106">*идкмд \_ кчмакс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="8c6c0-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6c0-107">Слово с низким приоритетом для этого параметра содержит идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="8c6c0-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="8c6c0-108">Слово в высоком порядке содержит количество символов в буфере *псзтекст* .</span><span class="sxs-lookup"><span data-stu-id="8c6c0-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8c6c0-109">*псзтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8c6c0-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c6c0-110">Строка в Юникоде, заканчивающаяся нулем и содержащая текст справки.</span><span class="sxs-lookup"><span data-stu-id="8c6c0-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c6c0-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="8c6c0-111">Remarks</span></span>

<span data-ttu-id="8c6c0-112">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c6c0-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="8c6c0-113">Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="8c6c0-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="8c6c0-114">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="8c6c0-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="8c6c0-115">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="8c6c0-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6c0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8c6c0-116">Requirements</span></span>



| <span data-ttu-id="8c6c0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8c6c0-117">Requirement</span></span> | <span data-ttu-id="8c6c0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8c6c0-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6c0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c6c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8c6c0-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c6c0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8c6c0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c6c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8c6c0-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c6c0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c6c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="8c6c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c6c0-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c6c0-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="8c6c0-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8c6c0-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8c6c0-126">**DFM \_ ЖЕСЕЛПТЕКСТВ** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="8c6c0-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




