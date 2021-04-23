---
title: Сообщение LVM_GETISEARCHSTRING (Коммктрл. h)
description: Извлекает строку добавочного поиска элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жетисеарчстринг ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- Элементы управления Windows для LVM_GETISEARCHSTRING сообщений
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492417"
---
# <a name="lvm_getisearchstring-message"></a><span data-ttu-id="01fc6-105">\_Сообщение LVM жетисеарчстринг</span><span class="sxs-lookup"><span data-stu-id="01fc6-105">LVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="01fc6-106">Извлекает строку добавочного поиска элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="01fc6-106">Retrieves the incremental search string of a list-view control.</span></span> <span data-ttu-id="01fc6-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетисеарчстринг ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="01fc6-107">You can send this message explicitly or by using the [**ListView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="01fc6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="01fc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01fc6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01fc6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="01fc6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="01fc6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="01fc6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01fc6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01fc6-112">Указатель на буфер, который получает строку добавочного поиска.</span><span class="sxs-lookup"><span data-stu-id="01fc6-112">Pointer to a buffer that receives the incremental search string.</span></span> <span data-ttu-id="01fc6-113">Чтобы просто получить длину строки, присвойте параметру *lParam* **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="01fc6-113">To just retrieve the length of the string, set *lParam* to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01fc6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01fc6-114">Return value</span></span>

<span data-ttu-id="01fc6-115">Возвращает количество символов в строке добавочного поиска, не включая завершающий нуль-символ, или нуль, если элемент управления "представление списка" не находится в режиме добавочного поиска.</span><span class="sxs-lookup"><span data-stu-id="01fc6-115">Returns the number of characters in the incremental search string, not including the terminating NULL character, or zero if the list-view control is not in incremental search mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="01fc6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01fc6-116">Remarks</span></span>

<span data-ttu-id="01fc6-117">**Предупреждение системы безопасности:** Неправильное использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="01fc6-117">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="01fc6-118">Это сообщение не позволяет получить сведения о размере буфера.</span><span class="sxs-lookup"><span data-stu-id="01fc6-118">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="01fc6-119">Если вы используете это сообщение, сначала вызовите сообщение, передав ему **значение NULL** в параметре *lParam*, после чего будет возвращено необходимое число символов, исключая **null** .</span><span class="sxs-lookup"><span data-stu-id="01fc6-119">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="01fc6-120">Затем вызовите сообщение еще раз, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="01fc6-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="01fc6-121">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: элементы управления Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="01fc6-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="01fc6-122">*Строка добавочного поиска* — это последовательность символов, которую пользователь вводит, когда представление списка имеет фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="01fc6-122">The *incremental search string* is the character sequence that the user types while the list view has the input focus.</span></span> <span data-ttu-id="01fc6-123">Каждый раз, когда пользователь вводит символ, система добавляет символ в строку поиска, а затем выполняет поиск соответствующего элемента.</span><span class="sxs-lookup"><span data-stu-id="01fc6-123">Each time the user types a character, the system appends the character to the search string and then searches for a matching item.</span></span> <span data-ttu-id="01fc6-124">Если система находит совпадение, она выбирает элемент и, при необходимости, прокручивает его в представлении.</span><span class="sxs-lookup"><span data-stu-id="01fc6-124">If the system finds a match, it selects the item and, if necessary, scrolls it into view.</span></span>

<span data-ttu-id="01fc6-125">С каждым символом, определяемым пользователем, связан период времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="01fc6-125">A time-out period is associated with each character that the user types.</span></span> <span data-ttu-id="01fc6-126">Если время ожидания истекает до того, как пользователь вводит другой символ, строка добавочного поиска сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="01fc6-126">If the time-out period elapses before the user types another character, the incremental search string is reset.</span></span>

<span data-ttu-id="01fc6-127">Убедитесь, что буфер достаточно велик, чтобы вместить строку и завершающий нуль-символ.</span><span class="sxs-lookup"><span data-stu-id="01fc6-127">Make sure that the buffer is large enough to hold the string and the terminating NULL character.</span></span> <span data-ttu-id="01fc6-128">Если он слишком мал, возникнет немедленная ошибка страницы.</span><span class="sxs-lookup"><span data-stu-id="01fc6-128">If it is too small, an immediate invalid page fault will result.</span></span>

## <a name="requirements"></a><span data-ttu-id="01fc6-129">Требования</span><span class="sxs-lookup"><span data-stu-id="01fc6-129">Requirements</span></span>



| <span data-ttu-id="01fc6-130">Требование</span><span class="sxs-lookup"><span data-stu-id="01fc6-130">Requirement</span></span> | <span data-ttu-id="01fc6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="01fc6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01fc6-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01fc6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="01fc6-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01fc6-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="01fc6-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01fc6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="01fc6-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01fc6-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01fc6-136">Header</span><span class="sxs-lookup"><span data-stu-id="01fc6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="01fc6-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="01fc6-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="01fc6-138">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="01fc6-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="01fc6-139">**LVM \_ ЖЕТИСЕАРЧСТРИНГВ** (Юникод) и **LVM \_ жетисеарчстринга** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="01fc6-139">**LVM\_GETISEARCHSTRINGW** (Unicode) and **LVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





