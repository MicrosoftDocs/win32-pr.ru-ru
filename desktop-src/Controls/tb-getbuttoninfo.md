---
title: Сообщение TB_GETBUTTONINFO (Коммктрл. h)
description: Извлекает расширенные сведения для кнопки на панели инструментов.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- Элементы управления Windows для TB_GETBUTTONINFO сообщений
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137846"
---
# <a name="tb_getbuttoninfo-message"></a><span data-ttu-id="8c3ce-104">\_Сообщение ЖЕТБУТТОНИНФО ТБ</span><span class="sxs-lookup"><span data-stu-id="8c3ce-104">TB\_GETBUTTONINFO message</span></span>

<span data-ttu-id="8c3ce-105">Извлекает расширенные сведения для кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="8c3ce-105">Retrieves extended information for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c3ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c3ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c3ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c3ce-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c3ce-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="8c3ce-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="8c3ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c3ce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c3ce-110">Указатель на структуру [**тббуттонинфо**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) , которая получает сведения о кнопке.</span><span class="sxs-lookup"><span data-stu-id="8c3ce-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that receives the button information.</span></span> <span data-ttu-id="8c3ce-111">Перед отправкой этого сообщения члены этой структуры должны быть заполнены **кбсизе** и **двмаск** .</span><span class="sxs-lookup"><span data-stu-id="8c3ce-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c3ce-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c3ce-112">Return value</span></span>

<span data-ttu-id="8c3ce-113">Возвращает отсчитываемый от нуля индекс кнопки или-1, если возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8c3ce-113">Returns the zero-based index of the button, or -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c3ce-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c3ce-114">Remarks</span></span>

<span data-ttu-id="8c3ce-115">Если для размещения кнопок на панели инструментов используется [**ТБ \_ Аддбуттонс**](tb-addbuttons.md) или [**ТБ \_ инсертбуттон**](tb-insertbutton.md) , то текст кнопки обычно задается индексом его пула строк.</span><span class="sxs-lookup"><span data-stu-id="8c3ce-115">When you use [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) to place buttons on the toolbar, the button text is commonly specified by its string pool index.</span></span> <span data-ttu-id="8c3ce-116">**ТБ \_ ЖЕТБУТТОНИНФО** не будет извлекать эту строку.</span><span class="sxs-lookup"><span data-stu-id="8c3ce-116">**TB\_GETBUTTONINFO** will not retrieve this string.</span></span> <span data-ttu-id="8c3ce-117">Чтобы использовать **ТБ \_ жетбуттонинфо** для получения текста кнопки, необходимо сначала задать для текстовой строки значение [**ТБ \_ сетбуттонинфо**](tb-setbuttoninfo.md).</span><span class="sxs-lookup"><span data-stu-id="8c3ce-117">To use **TB\_GETBUTTONINFO** to retrieve button text, you must first set the text string with [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md).</span></span> <span data-ttu-id="8c3ce-118">После того как вы настроили текст кнопки с **\_ сетбуттонинфо ТБ**, вы больше не сможете использовать индекс пула строк.</span><span class="sxs-lookup"><span data-stu-id="8c3ce-118">Once you have set the button text with **TB\_SETBUTTONINFO**, you can no longer use the string pool index.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c3ce-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8c3ce-119">Requirements</span></span>



| <span data-ttu-id="8c3ce-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8c3ce-120">Requirement</span></span> | <span data-ttu-id="8c3ce-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8c3ce-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c3ce-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c3ce-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8c3ce-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c3ce-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c3ce-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c3ce-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8c3ce-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8c3ce-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c3ce-126">Header</span><span class="sxs-lookup"><span data-stu-id="8c3ce-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c3ce-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c3ce-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8c3ce-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8c3ce-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8c3ce-129">**ТБ \_ ЖЕТБУТТОНИНФОВ** (Юникод) и **ТБ \_ жетбуттонинфоа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8c3ce-129">**TB\_GETBUTTONINFOW** (Unicode) and **TB\_GETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="8c3ce-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c3ce-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c3ce-131">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8c3ce-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8c3ce-132">**\_СЕТБУТТОНИНФО ТБ**</span><span class="sxs-lookup"><span data-stu-id="8c3ce-132">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="8c3ce-133">**\_ЖЕТБУТТОНТЕКСТ ТБ**</span><span class="sxs-lookup"><span data-stu-id="8c3ce-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> </dl>

 

 





