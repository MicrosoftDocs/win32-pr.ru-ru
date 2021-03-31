---
title: Сообщение CB_GETLBTEXT (Winuser. h)
description: Возвращает строку из списка поля со списком.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- Элементы управления Windows для CB_GETLBTEXT сообщений
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071617"
---
# <a name="cb_getlbtext-message"></a><span data-ttu-id="42cfe-104">\_Сообщение ЖЕТЛБТЕКСТ CB</span><span class="sxs-lookup"><span data-stu-id="42cfe-104">CB\_GETLBTEXT message</span></span>

<span data-ttu-id="42cfe-105">Возвращает строку из списка поля со списком.</span><span class="sxs-lookup"><span data-stu-id="42cfe-105">Gets a string from the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="42cfe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42cfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42cfe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42cfe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42cfe-108">Отсчитываемый от нуля индекс извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="42cfe-108">The zero-based index of the string to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="42cfe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42cfe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42cfe-110">Указатель на буфер, который получает строку.</span><span class="sxs-lookup"><span data-stu-id="42cfe-110">A pointer to the buffer that receives the string.</span></span> <span data-ttu-id="42cfe-111">Буфер должен содержать достаточно места для строки и завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="42cfe-111">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="42cfe-112">Вы можете отправить сообщение [**\_ жетлбтекстлен CB**](cb-getlbtextlen.md) перед сообщением **\_ жетлбтекст CB** , чтобы получить длину строки в **файле TCHAR**.</span><span class="sxs-lookup"><span data-stu-id="42cfe-112">You can send a [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) message prior to the **CB\_GETLBTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span> <span data-ttu-id="42cfe-113">Если это строка ANSI, то это число байтов, но если это строка в Юникоде, то это число символов.</span><span class="sxs-lookup"><span data-stu-id="42cfe-113">If it is an ANSI string this is the number of bytes, but if it is a Unicode string this is the number of characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42cfe-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42cfe-114">Return value</span></span>

<span data-ttu-id="42cfe-115">Возвращаемое значение — это длина строки в **файле TCHAR** s, исключая завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="42cfe-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="42cfe-116">Если параметр *wParam* не указывает допустимый индекс, возвращается значение CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="42cfe-116">If *wParam* does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="42cfe-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42cfe-117">Remarks</span></span>

<span data-ttu-id="42cfe-118">**Предупреждение системы безопасности:** Неправильное использование этого сообщения может нарушить безопасность программы.</span><span class="sxs-lookup"><span data-stu-id="42cfe-118">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="42cfe-119">Это сообщение не позволяет получить сведения о размере буфера.</span><span class="sxs-lookup"><span data-stu-id="42cfe-119">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="42cfe-120">Если вы используете это сообщение, сначала вызовите [**CB \_ жетлбтекстлен**](cb-getlbtextlen.md) , чтобы получить необходимое количество символов, а затем вызовите сообщение, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="42cfe-120">If you use this message, first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="42cfe-121">Прежде чем продолжить, ознакомьтесь с [вопросами безопасности: элементы управления Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="42cfe-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="42cfe-122">Если создать поле со списком, используя стиль, рисуемый владельцем, но без [**стиля \_ хасстрингс CBS**](combo-box-styles.md) , то буфер, на который указывает *lParam* , получает данные, связанные с этим элементом.</span><span class="sxs-lookup"><span data-stu-id="42cfe-122">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the buffer pointed to by *lParam* receives the data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="42cfe-123">Требования</span><span class="sxs-lookup"><span data-stu-id="42cfe-123">Requirements</span></span>



| <span data-ttu-id="42cfe-124">Требование</span><span class="sxs-lookup"><span data-stu-id="42cfe-124">Requirement</span></span> | <span data-ttu-id="42cfe-125">Значение</span><span class="sxs-lookup"><span data-stu-id="42cfe-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42cfe-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42cfe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="42cfe-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42cfe-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42cfe-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42cfe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="42cfe-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42cfe-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42cfe-130">Header</span><span class="sxs-lookup"><span data-stu-id="42cfe-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="42cfe-131"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42cfe-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42cfe-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42cfe-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cfe-133">**\_ЖЕТЛБТЕКСТЛЕН CB**</span><span class="sxs-lookup"><span data-stu-id="42cfe-133">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
</dt> </dl>

 

 





