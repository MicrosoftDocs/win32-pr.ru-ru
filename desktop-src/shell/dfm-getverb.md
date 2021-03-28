---
description: Отправляется реализацией контекстного меню по умолчанию для получения команды для заданного идентификатора команды в контекстном меню.
title: Сообщение DFM_GETVERB (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262909"
---
# <a name="dfm_getverb-message"></a><span data-ttu-id="49b2a-103">DFM, \_ сообщение о команде</span><span class="sxs-lookup"><span data-stu-id="49b2a-103">DFM\_GETVERB message</span></span>

<span data-ttu-id="49b2a-104">Отправляется реализацией контекстного меню по умолчанию для получения команды для заданного идентификатора команды в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="49b2a-104">Sent by the default context menu implementation to get the verb for the given command ID in the context menu.</span></span>


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="49b2a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="49b2a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b2a-106">*идкмд \_ кчмакс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="49b2a-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49b2a-107">Слово с низким приоритетом для этого параметра содержит идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="49b2a-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="49b2a-108">Слово в высоком порядке содержит количество символов в буфере *псзтекст* .</span><span class="sxs-lookup"><span data-stu-id="49b2a-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="49b2a-109">*псзтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="49b2a-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49b2a-110">Указатель на строку, завершающуюся нулем, которая содержит текст команды.</span><span class="sxs-lookup"><span data-stu-id="49b2a-110">A pointer to a null-terminated string that contains the verb text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49b2a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="49b2a-111">Remarks</span></span>

<span data-ttu-id="49b2a-112">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49b2a-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="49b2a-113">Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="49b2a-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="49b2a-114">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="49b2a-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="49b2a-115">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="49b2a-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b2a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="49b2a-116">Requirements</span></span>



| <span data-ttu-id="49b2a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="49b2a-117">Requirement</span></span> | <span data-ttu-id="49b2a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="49b2a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49b2a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49b2a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="49b2a-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49b2a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="49b2a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49b2a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="49b2a-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49b2a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="49b2a-123">Header</span><span class="sxs-lookup"><span data-stu-id="49b2a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="49b2a-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="49b2a-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="49b2a-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="49b2a-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49b2a-126">**DFM \_ ЖЕТВЕРБВ** (Юникод) и **DFM- \_ verb** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="49b2a-126">**DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)</span></span><br/>                 |



 

 




