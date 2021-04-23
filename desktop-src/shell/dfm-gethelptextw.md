---
description: Позволяет объекту обратного вызова указать строку текста справки.
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
ms.openlocfilehash: 7ac1e41046b2d757df96e9acf5722710ae832bf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984308"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="44bff-103">\_Сообщение DFM жеселптекств</span><span class="sxs-lookup"><span data-stu-id="44bff-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="44bff-104">Позволяет объекту обратного вызова указать строку текста справки.</span><span class="sxs-lookup"><span data-stu-id="44bff-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="44bff-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="44bff-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44bff-106">*идкмд \_ кчмакс* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="44bff-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44bff-107">Слово с низким приоритетом для этого параметра содержит идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="44bff-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="44bff-108">Слово в высоком порядке содержит количество символов в буфере *псзтекст* .</span><span class="sxs-lookup"><span data-stu-id="44bff-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="44bff-109">*псзтекст* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44bff-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44bff-110">Строка в Юникоде, заканчивающаяся нулем и содержащая текст справки.</span><span class="sxs-lookup"><span data-stu-id="44bff-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44bff-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="44bff-111">Remarks</span></span>

<span data-ttu-id="44bff-112">Это сообщение отправляется либо в функцию обратного вызова, либо в объект обратного вызова в зависимости от того, как создается объект контекстного меню по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="44bff-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="44bff-113">Существует два API для своей конструкции, [**кдеффолдермену \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**шкреатедефаултконтекстмену**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="44bff-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="44bff-114">[**DFM \_ ИНВОКЕКОММАНДЕКС**](dfm-invokecommandex.md) — это расширенная версия этого сообщения, которая предоставляет дополнительные сведения для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="44bff-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="44bff-115">Используйте **DFM \_ инвокекоммандекс** , если в реализации требуется дополнительная информация, предоставляемая этим интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="44bff-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="44bff-116">Требования</span><span class="sxs-lookup"><span data-stu-id="44bff-116">Requirements</span></span>



| <span data-ttu-id="44bff-117">Требование</span><span class="sxs-lookup"><span data-stu-id="44bff-117">Requirement</span></span> | <span data-ttu-id="44bff-118">Значение</span><span class="sxs-lookup"><span data-stu-id="44bff-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="44bff-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44bff-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44bff-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44bff-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="44bff-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44bff-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44bff-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44bff-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="44bff-123">Header</span><span class="sxs-lookup"><span data-stu-id="44bff-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44bff-124"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="44bff-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="44bff-125">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="44bff-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="44bff-126">**DFM \_ ЖЕСЕЛПТЕКСТВ** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="44bff-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




