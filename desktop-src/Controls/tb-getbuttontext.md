---
title: Сообщение TB_GETBUTTONTEXT (Коммктрл. h)
description: Получает отображаемый текст кнопки на панели инструментов.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- Элементы управления Windows для TB_GETBUTTONTEXT сообщений
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136234"
---
# <a name="tb_getbuttontext-message"></a><span data-ttu-id="fa2be-104">\_Сообщение ЖЕТБУТТОНТЕКСТ ТБ</span><span class="sxs-lookup"><span data-stu-id="fa2be-104">TB\_GETBUTTONTEXT message</span></span>

<span data-ttu-id="fa2be-105">Получает отображаемый текст кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="fa2be-105">Retrieves the display text of a button on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fa2be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa2be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa2be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fa2be-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa2be-108">Идентификатор команды для кнопки, текст которой необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="fa2be-108">Command identifier of the button whose text is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="fa2be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fa2be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fa2be-110">Указатель на буфер, который получает текст кнопки.</span><span class="sxs-lookup"><span data-stu-id="fa2be-110">Pointer to a buffer that receives the button text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa2be-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa2be-111">Return value</span></span>

<span data-ttu-id="fa2be-112">Возвращает длину строки в символах, на которую указывает *lParam*.</span><span class="sxs-lookup"><span data-stu-id="fa2be-112">Returns the length, in characters, of the string pointed to by *lParam*.</span></span> <span data-ttu-id="fa2be-113">Длина не включает завершающего нуль символа.</span><span class="sxs-lookup"><span data-stu-id="fa2be-113">The length does not include the terminating null character.</span></span> <span data-ttu-id="fa2be-114">В случае неудачи возвращаемое значение равно-1.</span><span class="sxs-lookup"><span data-stu-id="fa2be-114">If unsuccessful, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa2be-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa2be-115">Remarks</span></span>

<span data-ttu-id="fa2be-116">**Предупреждение системы безопасности:** Неправильное использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="fa2be-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="fa2be-117">Это сообщение не позволяет получить сведения о размере буфера.</span><span class="sxs-lookup"><span data-stu-id="fa2be-117">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="fa2be-118">Если вы используете это сообщение, сначала вызовите сообщение, передав ему **значение NULL** в параметре *lParam*, после чего будет возвращено необходимое число символов, исключая **null** .</span><span class="sxs-lookup"><span data-stu-id="fa2be-118">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="fa2be-119">Затем вызовите сообщение еще раз, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="fa2be-119">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="fa2be-120">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: элементы управления Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="fa2be-120">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="fa2be-121">Возвращаемая строка соответствует тексту, который в данный момент отображается кнопкой.</span><span class="sxs-lookup"><span data-stu-id="fa2be-121">The returned string corresponds to the text that is currently displayed by the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa2be-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fa2be-122">Requirements</span></span>



| <span data-ttu-id="fa2be-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fa2be-123">Requirement</span></span> | <span data-ttu-id="fa2be-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fa2be-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa2be-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa2be-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa2be-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa2be-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fa2be-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa2be-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa2be-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa2be-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa2be-129">Header</span><span class="sxs-lookup"><span data-stu-id="fa2be-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa2be-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa2be-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="fa2be-131">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="fa2be-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="fa2be-132">**ТБ \_ ЖЕТБУТТОНТЕКСТВ** (Юникод) и **ТБ \_ жетбуттонтекста** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="fa2be-132">**TB\_GETBUTTONTEXTW** (Unicode) and **TB\_GETBUTTONTEXTA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="fa2be-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa2be-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="fa2be-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fa2be-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fa2be-135">**\_ЖЕТБУТТОНИНФО ТБ**</span><span class="sxs-lookup"><span data-stu-id="fa2be-135">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="fa2be-136">**TB (ТБ) \_**</span><span class="sxs-lookup"><span data-stu-id="fa2be-136">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="fa2be-137">**\_СЕТБУТТОНИНФО ТБ**</span><span class="sxs-lookup"><span data-stu-id="fa2be-137">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> </dl>

 

 





