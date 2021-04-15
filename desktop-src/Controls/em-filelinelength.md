---
title: Сообщение EM_FILELINELENGTH (Коммктрл. h)
description: Извлекает длину строки в символах в элементе управления "поле ввода" независимо от того, как линии отображаются на экране.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Элементы управления Windows для EM_FILELINELENGTH сообщений
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa50f4d9b49253a558095be78e0e781d7d4c7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534370"
---
# <a name="em_filelinelength-message"></a><span data-ttu-id="ee07b-104">\_Сообщение ФИЛЕЛИНЕЛЕНГС EM</span><span class="sxs-lookup"><span data-stu-id="ee07b-104">EM\_FILELINELENGTH message</span></span>

<span data-ttu-id="ee07b-105">Извлекает длину строки в символах в элементе управления "поле ввода" независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="ee07b-105">Retrieves the length, in characters, of a line in an edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="ee07b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee07b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee07b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ee07b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee07b-108">Индекс символа в строке, длина которого должна быть получена.</span><span class="sxs-lookup"><span data-stu-id="ee07b-108">The character index of a character in the line whose length is to be retrieved.</span></span> <span data-ttu-id="ee07b-109">Если этот параметр больше числа символов в элементе управления, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ee07b-109">If this parameter is greater than the number of characters in the control, the return value is zero.</span></span>

<span data-ttu-id="ee07b-110">Этот параметр может быть равен-1.</span><span class="sxs-lookup"><span data-stu-id="ee07b-110">This parameter can be -1.</span></span> <span data-ttu-id="ee07b-111">В этом случае сообщение возвращает число невыбранных символов в строках, содержащих выбранные символы.</span><span class="sxs-lookup"><span data-stu-id="ee07b-111">In this case, the message returns the number of unselected characters on lines containing selected characters.</span></span> <span data-ttu-id="ee07b-112">Например, если выделение, расширенное от четвертого символа одной строки до восьмого символа от конца следующей строки, возвращаемое значение будет равно 10 (три символа в первой строке и семь на следующем).</span><span class="sxs-lookup"><span data-stu-id="ee07b-112">For example, if the selection extended from the fourth character of one line through the eighth character from the end of the next line, the return value would be 10 (three characters on the first line and seven on the next).</span></span>

</dd> <dt>

<span data-ttu-id="ee07b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ee07b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ee07b-114">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="ee07b-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee07b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee07b-115">Return value</span></span>

<span data-ttu-id="ee07b-116">Для элементов управления многострочного редактирования возвращаемое значение является длиной в **TCHAR** s строки, заданной параметром *wParam* , независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="ee07b-116">For multiline edit controls, the return value is the length, in **TCHAR** s, of the line specified by the *wParam* parameter, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="ee07b-117">Он не включает символ возврата каретки или перевода строки в конце линии.</span><span class="sxs-lookup"><span data-stu-id="ee07b-117">It does not include the carriage-return or linefeed character at the end of the line.</span></span>

<span data-ttu-id="ee07b-118">Для однострочных элементов управления редактирования возвращаемое значение является длиной в **TCHAR** s текста в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="ee07b-118">For single-line edit controls, the return value is the length, in **TCHAR** s, of the text in the edit control.</span></span>

<span data-ttu-id="ee07b-119">Если параметр *wParam* больше числа символов в элементе управления, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="ee07b-119">If *wParam* is greater than the number of characters in the control, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee07b-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee07b-120">Remarks</span></span>

<span data-ttu-id="ee07b-121">Используйте сообщение [**EM \_ филелинеиндекс**](em-lineindex.md) , чтобы получить индекс символа для заданного номера строки в многострочном элементе управления Edit, независимо от того, как линии отображаются на экране.</span><span class="sxs-lookup"><span data-stu-id="ee07b-121">Use the [**EM\_FILELINEINDEX**](em-lineindex.md) message to retrieve a character index for a given line number within a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee07b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ee07b-122">Requirements</span></span>



| <span data-ttu-id="ee07b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ee07b-123">Requirement</span></span> | <span data-ttu-id="ee07b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ee07b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee07b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee07b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ee07b-126">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="ee07b-126">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ee07b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee07b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ee07b-128">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="ee07b-128">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ee07b-129">Header</span><span class="sxs-lookup"><span data-stu-id="ee07b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee07b-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee07b-130"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee07b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee07b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee07b-132">**EM \_ филелинеиндекс**</span><span class="sxs-lookup"><span data-stu-id="ee07b-132">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





