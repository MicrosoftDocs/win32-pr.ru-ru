---
title: Сообщение TB_GETSTRING (Коммктрл. h)
description: Извлекает строку из пула строк панели инструментов.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Элементы управления Windows для TB_GETSTRING сообщений
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071381"
---
# <a name="tb_getstring-message"></a><span data-ttu-id="269f9-104">Сообщение о GETSTRING (ТБ) \_</span><span class="sxs-lookup"><span data-stu-id="269f9-104">TB\_GETSTRING message</span></span>

<span data-ttu-id="269f9-105">Извлекает строку из пула строк панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="269f9-105">Retrieves a string from a toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="269f9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="269f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="269f9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="269f9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="269f9-108">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает длину буфера *lParam* в байтах.</span><span class="sxs-lookup"><span data-stu-id="269f9-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the length of the *lParam* buffer, in bytes.</span></span> <span data-ttu-id="269f9-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает индекс строки.</span><span class="sxs-lookup"><span data-stu-id="269f9-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="269f9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="269f9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="269f9-111">Указатель на буфер, используемый для возврата строки.</span><span class="sxs-lookup"><span data-stu-id="269f9-111">Pointer to a buffer used to return the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="269f9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="269f9-112">Return value</span></span>

<span data-ttu-id="269f9-113">Возвращает длину строки в случае успеха или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="269f9-113">Returns the string length if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="269f9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="269f9-114">Remarks</span></span>

<span data-ttu-id="269f9-115">Это сообщение возвращает указанную строку из пула строк панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="269f9-115">This message returns the specified string from the toolbar's string pool.</span></span> <span data-ttu-id="269f9-116">Он не обязательно соответствует текстовой строке, отображаемой в данный момент кнопкой.</span><span class="sxs-lookup"><span data-stu-id="269f9-116">It does not necessarily correspond to the text string currently being displayed by a button.</span></span> <span data-ttu-id="269f9-117">Чтобы получить текущую текстовую строку кнопки, отправьте на панель инструментов сообщение [**\_ Жетбуттонтекст (ТБ**](tb-getbuttontext.md) ).</span><span class="sxs-lookup"><span data-stu-id="269f9-117">To retrieve a button's current text string, send the toolbar a [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="269f9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="269f9-118">Requirements</span></span>



| <span data-ttu-id="269f9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="269f9-119">Requirement</span></span> | <span data-ttu-id="269f9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="269f9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="269f9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="269f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="269f9-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="269f9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="269f9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="269f9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="269f9-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="269f9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="269f9-125">Header</span><span class="sxs-lookup"><span data-stu-id="269f9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="269f9-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="269f9-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="269f9-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="269f9-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="269f9-128">**ТБ \_ ЖЕТСТРИНГВ** (Юникод) и **ТБ- \_ строка** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="269f9-128">**TB\_GETSTRINGW** (Unicode) and **TB\_GETSTRINGA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="269f9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="269f9-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="269f9-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="269f9-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="269f9-131">**\_ADDSTRING ТБ**</span><span class="sxs-lookup"><span data-stu-id="269f9-131">**TB\_ADDSTRING**</span></span>](tb-addstring.md)
</dt> <dt>

[<span data-ttu-id="269f9-132">**\_АДДБУТТОНС ТБ**</span><span class="sxs-lookup"><span data-stu-id="269f9-132">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="269f9-133">**\_ИНСЕРТБУТТОН ТБ**</span><span class="sxs-lookup"><span data-stu-id="269f9-133">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

