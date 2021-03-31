---
title: Сообщение TB_SETBUTTONINFO (Коммктрл. h)
description: Задает сведения для существующей кнопки на панели инструментов.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- Элементы управления Windows для TB_SETBUTTONINFO сообщений
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892614"
---
# <a name="tb_setbuttoninfo-message"></a><span data-ttu-id="9c4bc-104">\_Сообщение СЕТБУТТОНИНФО ТБ</span><span class="sxs-lookup"><span data-stu-id="9c4bc-104">TB\_SETBUTTONINFO message</span></span>

<span data-ttu-id="9c4bc-105">Задает сведения для существующей кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9c4bc-105">Sets the information for an existing button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c4bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c4bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c4bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c4bc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c4bc-108">Идентификатор кнопки.</span><span class="sxs-lookup"><span data-stu-id="9c4bc-108">Button identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9c4bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c4bc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c4bc-110">Указатель на структуру [**тббуттонинфо**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) , содержащую сведения о новых кнопках.</span><span class="sxs-lookup"><span data-stu-id="9c4bc-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that contains the new button information.</span></span> <span data-ttu-id="9c4bc-111">Перед отправкой этого сообщения члены этой структуры должны быть заполнены **кбсизе** и **двмаск** .</span><span class="sxs-lookup"><span data-stu-id="9c4bc-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c4bc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c4bc-112">Return value</span></span>

<span data-ttu-id="9c4bc-113">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9c4bc-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c4bc-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c4bc-114">Remarks</span></span>

<span data-ttu-id="9c4bc-115">Текст обычно назначается кнопкам при их добавлении на панель инструментов путем указания индекса строки в пуле строк панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9c4bc-115">Text is commonly assigned to buttons when they are added to a toolbar by specifying the index of a string in the toolbar's string pool.</span></span> <span data-ttu-id="9c4bc-116">Если для назначения нового текста кнопке используется **\_ сетбуттонинфо ТБ** , она будет окончательно переопределять текст из пула строк.</span><span class="sxs-lookup"><span data-stu-id="9c4bc-116">If you use a **TB\_SETBUTTONINFO** to assign new text to a button, it will permanently override the text from the string pool.</span></span> <span data-ttu-id="9c4bc-117">Вы можете изменить текст, вызвав **\_ сетбуттонинфо ТБ** еще раз, но нельзя переназначить строку из пула строк.</span><span class="sxs-lookup"><span data-stu-id="9c4bc-117">You can change the text by calling **TB\_SETBUTTONINFO** again, but you cannot reassign the string from the string pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c4bc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9c4bc-118">Requirements</span></span>



| <span data-ttu-id="9c4bc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9c4bc-119">Requirement</span></span> | <span data-ttu-id="9c4bc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9c4bc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c4bc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c4bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c4bc-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c4bc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c4bc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c4bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c4bc-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c4bc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c4bc-125">Header</span><span class="sxs-lookup"><span data-stu-id="9c4bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c4bc-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c4bc-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9c4bc-127">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="9c4bc-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9c4bc-128">**ТБ \_ СЕТБУТТОНИНФОВ** (Юникод) и **ТБ \_ сетбуттонинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9c4bc-128">**TB\_SETBUTTONINFOW** (Unicode) and **TB\_SETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="9c4bc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c4bc-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c4bc-130">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9c4bc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c4bc-131">**\_АДДБУТТОНС ТБ**</span><span class="sxs-lookup"><span data-stu-id="9c4bc-131">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="9c4bc-132">**\_ЖЕТБУТТОНИНФО ТБ**</span><span class="sxs-lookup"><span data-stu-id="9c4bc-132">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="9c4bc-133">**\_ЖЕТБУТТОНТЕКСТ ТБ**</span><span class="sxs-lookup"><span data-stu-id="9c4bc-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> <dt>

[<span data-ttu-id="9c4bc-134">**TB (ТБ) \_**</span><span class="sxs-lookup"><span data-stu-id="9c4bc-134">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="9c4bc-135">**\_ИНСЕРТБУТТОН ТБ**</span><span class="sxs-lookup"><span data-stu-id="9c4bc-135">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

 





