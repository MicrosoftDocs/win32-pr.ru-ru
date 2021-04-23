---
title: Сообщение TVM_GETISEARCHSTRING (Коммктрл. h)
description: Извлекает строку добавочного поиска для элемента управления "дерево-представление".
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- Элементы управления Windows для TVM_GETISEARCHSTRING сообщений
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137418"
---
# <a name="tvm_getisearchstring-message"></a><span data-ttu-id="6e296-104">\_Сообщение TVM жетисеарчстринг</span><span class="sxs-lookup"><span data-stu-id="6e296-104">TVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="6e296-105">Извлекает строку добавочного поиска для элемента управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="6e296-105">Retrieves the incremental search string for a tree-view control.</span></span> <span data-ttu-id="6e296-106">Элемент управления "представление дерева" использует строку добавочного поиска для выбора элемента на основе символов, введенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="6e296-106">The tree-view control uses the incremental search string to select an item based on characters typed by the user.</span></span> <span data-ttu-id="6e296-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетисеарчстринг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="6e296-107">You can send this message explicitly or by using the [**TreeView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e296-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e296-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e296-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e296-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6e296-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="6e296-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6e296-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e296-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e296-112">Указатель на буфер, который получает строку добавочного поиска.</span><span class="sxs-lookup"><span data-stu-id="6e296-112">Pointer to the buffer that receives the incremental search string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e296-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e296-113">Return value</span></span>

<span data-ttu-id="6e296-114">Возвращает количество символов в строке добавочного поиска.</span><span class="sxs-lookup"><span data-stu-id="6e296-114">Returns the number of characters in the incremental search string.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e296-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e296-115">Remarks</span></span>

<span data-ttu-id="6e296-116">**Предупреждение системы безопасности:** Неправильное использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="6e296-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="6e296-117">Необходимо выделить достаточно большой буфер для хранения строки.</span><span class="sxs-lookup"><span data-stu-id="6e296-117">You must allocate a large enough buffer to hold the string.</span></span> <span data-ttu-id="6e296-118">Сначала необходимо вызвать сообщение, передав **значение NULL** в *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6e296-118">First call the message passing **NULL** in *lParam*.</span></span> <span data-ttu-id="6e296-119">Это возвращает количество символов, которые являются обязательными **, и исключает их**.</span><span class="sxs-lookup"><span data-stu-id="6e296-119">This returns the number of characters, excluding **NULL**, that are required.</span></span> <span data-ttu-id="6e296-120">Затем вызовите сообщение еще раз, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="6e296-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="6e296-121">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: Microsoft Windows Controls](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="6e296-121">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="6e296-122">Если элемент управления "дерево-представление" не находится в режиме добавочного поиска, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6e296-122">If the tree-view control is not in incremental search mode, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e296-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6e296-123">Requirements</span></span>



| <span data-ttu-id="6e296-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6e296-124">Requirement</span></span> | <span data-ttu-id="6e296-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6e296-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e296-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e296-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6e296-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e296-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e296-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e296-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6e296-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e296-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e296-130">Header</span><span class="sxs-lookup"><span data-stu-id="6e296-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e296-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e296-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6e296-132">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="6e296-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6e296-133">**TVM \_ ЖЕТИСЕАРЧСТРИНГВ** (Юникод) и **TVM \_ жетисеарчстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6e296-133">**TVM\_GETISEARCHSTRINGW** (Unicode) and **TVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





