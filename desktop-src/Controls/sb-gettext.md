---
title: Сообщение SB_GETTEXT (Коммктрл. h)
description: Извлекает текст из указанной части окна состояния.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- Элементы управления Windows для SB_GETTEXT сообщений
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071861"
---
# <a name="sb_gettext-message"></a><span data-ttu-id="f8ae1-104">\_SMS SB</span><span class="sxs-lookup"><span data-stu-id="f8ae1-104">SB\_GETTEXT message</span></span>

<span data-ttu-id="f8ae1-105">Извлекает текст из указанной части окна состояния.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-105">Retrieves the text from the specified part of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="f8ae1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8ae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ae1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8ae1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ae1-108">Отсчитываемый от нуля индекс части, из которой требуется получить текст.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-108">Zero-based index of the part from which to retrieve text.</span></span>

</dd> <dt>

<span data-ttu-id="f8ae1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8ae1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ae1-110">Указатель на буфер, который получает текст в виде строки, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-110">Pointer to the buffer that receives the text as a null-terminated string.</span></span> <span data-ttu-id="f8ae1-111">Чтобы определить необходимый размер буфера, используйте сообщение [**SB \_ жеттекстленгс**](sb-gettextlength.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ae1-111">Use the [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message to determine the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ae1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8ae1-112">Return value</span></span>

<span data-ttu-id="f8ae1-113">Возвращает 32-разрядное значение, состоящее из 2 16-разрядных значений.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-113">Returns a 32-bit value that consists of two 16-bit values.</span></span> <span data-ttu-id="f8ae1-114">Нижнее слово указывает длину текста в символах.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-114">The low word specifies the length, in characters, of the text.</span></span> <span data-ttu-id="f8ae1-115">В верхнем слове указывается тип операции, используемой для рисования текста.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-115">The high word specifies the type of operation used to draw the text.</span></span> <span data-ttu-id="f8ae1-116">Тип может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-116">The type can be one of the following values.</span></span>



| <span data-ttu-id="f8ae1-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f8ae1-117">Return code</span></span>                                                                                    | <span data-ttu-id="f8ae1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f8ae1-118">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8ae1-119"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ae1-119"><dt>**0**</dt></span></span> </dl>               | <span data-ttu-id="f8ae1-120">Текст отображается с границей, которая отображается ниже плоскости окна.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-120">The text is drawn with a border to appear lower than the plane of the window.</span></span><br/>  |
| <dl> <span data-ttu-id="f8ae1-121"><dt>**SBT \_ НЕграницы**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ae1-121"><dt>**SBT\_NOBORDERS**</dt></span></span> </dl>  | <span data-ttu-id="f8ae1-122">Текст отображается без границ.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-122">The text is drawn without borders.</span></span><br/>                                             |
| <dl> <span data-ttu-id="f8ae1-123"><dt>**SBT \_ POPOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ae1-123"><dt>**SBT\_POPOUT**</dt></span></span> </dl>     | <span data-ttu-id="f8ae1-124">Текст отображается с границей, которая отображается выше плоскости окна.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-124">The text is drawn with a border to appear higher than the plane of the window.</span></span><br/> |
| <dl> <span data-ttu-id="f8ae1-125"><dt>**SBT \_ RTLREADING**</dt></span><span class="sxs-lookup"><span data-stu-id="f8ae1-125"><dt>**SBT\_RTLREADING**</dt></span></span> </dl> | <span data-ttu-id="f8ae1-126">Текст отображается в противоположном направлении текста в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-126">The text displays in the opposite direction of the text in the parent window.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="f8ae1-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8ae1-127">Remarks</span></span>

<span data-ttu-id="f8ae1-128">**Предупреждение системы безопасности:** Неправильное использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-128">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="f8ae1-129">Это сообщение не позволяет получить сведения о размере буфера.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-129">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="f8ae1-130">Если вы используете это сообщение, сначала вызовите [**SB \_ жеттекстленгс**](sb-gettextlength.md) , чтобы получить необходимое количество символов, а затем вызовите сообщение, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-130">If you use this message, first call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="f8ae1-131">Если вы ждете до **вызова \_ SB** GetText, текст может измениться, что сделает недействительной возвращаемое значение **SB \_ жеттекстленгс**.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-131">If you wait before calling **SB\_GETTEXT** the text could change, thereby invalidating the return value of **SB\_GETTEXTLENGTH**.</span></span> <span data-ttu-id="f8ae1-132">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: элементы управления Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ae1-132">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="f8ae1-133">Это сообщение возвращает не более 65 535 символов.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-133">This message returns a maximum of 65,535 characters.</span></span> <span data-ttu-id="f8ae1-134">Если длина текстовой строки превышает это значение, она усекается.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-134">If the text string is longer than that, it is truncated.</span></span>

<span data-ttu-id="f8ae1-135">Если текст имеет \_ Тип рисования SBT овнердрав, то это сообщение возвращает 32-разрядное значение, связанное с текстом, а не тип операции и длину.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-135">If the text has the SBT\_OWNERDRAW drawing type, this message returns the 32-bit value associated with the text instead of the length and operation type.</span></span>

<span data-ttu-id="f8ae1-136">Нормальный отображаемый текст Windows слева направо (LTR).</span><span class="sxs-lookup"><span data-stu-id="f8ae1-136">Normal windows display text left-to-right (LTR).</span></span> <span data-ttu-id="f8ae1-137">Windows может быть *зеркальным* отображением таких языков, как иврит или арабский, которые читаются справа налево.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-137">Windows can be *mirrored* to display languages such as Hebrew or Arabic that read right-to-left (RTL).</span></span> <span data-ttu-id="f8ae1-138">Если \_ задано значение SBT RTLREADING, строка *lParam* считывает в обратном направлении от текста в родительском окне.</span><span class="sxs-lookup"><span data-stu-id="f8ae1-138">If SBT\_RTLREADING is set, the *lParam* string reads in the opposite direction from the text in the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ae1-139">Требования</span><span class="sxs-lookup"><span data-stu-id="f8ae1-139">Requirements</span></span>



| <span data-ttu-id="f8ae1-140">Требование</span><span class="sxs-lookup"><span data-stu-id="f8ae1-140">Requirement</span></span> | <span data-ttu-id="f8ae1-141">Значение</span><span class="sxs-lookup"><span data-stu-id="f8ae1-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ae1-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8ae1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ae1-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8ae1-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8ae1-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8ae1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ae1-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f8ae1-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8ae1-146">Header</span><span class="sxs-lookup"><span data-stu-id="f8ae1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ae1-147"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ae1-147"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f8ae1-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f8ae1-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f8ae1-149">**SB \_ ЖЕТТЕКСТВ** (Юникод) и **SB- \_ Text** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f8ae1-149">**SB\_GETTEXTW** (Unicode) and **SB\_GETTEXTA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="f8ae1-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8ae1-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ae1-151">**SB \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="f8ae1-151">**SB\_SETTEXT**</span></span>](sb-settext.md)
</dt> </dl>

 

 





