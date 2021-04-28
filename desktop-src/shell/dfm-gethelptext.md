---
description: DFM_GETHELPTEXT сообщение — позволяет объекту обратного вызова указать строку текста справки.
title: Сообщение DFM_GETHELPTEXT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2428fe6696ff5949a0b25487437c8f3408b95f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097072"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="161e2-103">\_Сообщение DFM жеселптекст</span><span class="sxs-lookup"><span data-stu-id="161e2-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="161e2-104">Позволяет объекту обратного вызова указать строку текста справки.</span><span class="sxs-lookup"><span data-stu-id="161e2-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="161e2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="161e2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="161e2-106">*идкмд \_ кчмакс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="161e2-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="161e2-107">Слово с низким приоритетом для этого параметра содержит идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="161e2-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="161e2-108">Слово в высоком порядке содержит количество символов в буфере *псзтекст* .</span><span class="sxs-lookup"><span data-stu-id="161e2-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="161e2-109">*псзтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="161e2-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="161e2-110">Строка ANSI, заканчивающаяся нулем и содержащая текст справки.</span><span class="sxs-lookup"><span data-stu-id="161e2-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="161e2-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="161e2-111">Remarks</span></span>

<span data-ttu-id="161e2-112">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="161e2-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="161e2-113">Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="161e2-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="161e2-114">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="161e2-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="161e2-115">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="161e2-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="161e2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="161e2-116">Requirements</span></span>



| <span data-ttu-id="161e2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="161e2-117">Requirement</span></span> | <span data-ttu-id="161e2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="161e2-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="161e2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="161e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="161e2-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="161e2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="161e2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="161e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="161e2-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="161e2-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="161e2-123">Header</span><span class="sxs-lookup"><span data-stu-id="161e2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="161e2-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="161e2-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="161e2-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="161e2-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="161e2-126">**DFM \_ ЖЕСЕЛПТЕКСТ** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="161e2-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




