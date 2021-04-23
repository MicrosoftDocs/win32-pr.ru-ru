---
title: Сообщение LB_GETTEXT (Winuser. h)
description: Возвращает строку из списка.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- Элементы управления Windows для LB_GETTEXT сообщений
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492150"
---
# <a name="lb_gettext-message"></a><span data-ttu-id="d382f-104">Сообщение балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="d382f-104">LB\_GETTEXT message</span></span>

<span data-ttu-id="d382f-105">Возвращает строку из списка.</span><span class="sxs-lookup"><span data-stu-id="d382f-105">Gets a string from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d382f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d382f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d382f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d382f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d382f-108">Отсчитываемый от нуля индекс извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="d382f-108">The zero-based index of the string to retrieve.</span></span>

<span data-ttu-id="d382f-109">Windows 95, Windows 98/Windows Millennium Edition (Windows Me): параметр *wParam* ограничен 16-разрядными значениями.</span><span class="sxs-lookup"><span data-stu-id="d382f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="d382f-110">Это означает, что списки не могут содержать более 32 767 элементов.</span><span class="sxs-lookup"><span data-stu-id="d382f-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="d382f-111">Хотя количество элементов ограничено, общий размер элементов в списке в байтах ограничен только доступной памятью.</span><span class="sxs-lookup"><span data-stu-id="d382f-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="d382f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d382f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d382f-113">Указатель на буфер, который получит строку; Это тип **LPTSTR** , который впоследствии приводится к **lParam**.</span><span class="sxs-lookup"><span data-stu-id="d382f-113">A pointer to the buffer that will receive the string; it is type **LPTSTR** which is subsequently cast to an **LPARAM**.</span></span> <span data-ttu-id="d382f-114">Буфер должен содержать достаточно места для строки и завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="d382f-114">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="d382f-115">Сообщение [**\_ жеттекстлен балансировки нагрузки**](lb-gettextlen.md) может быть отправлено перед тем, как сообщение **балансировки нагрузки \_** получает длину строки в **TCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="d382f-115">An [**LB\_GETTEXTLEN**](lb-gettextlen.md) message can be sent before the **LB\_GETTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d382f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d382f-116">Return value</span></span>

<span data-ttu-id="d382f-117">Возвращаемое значение — это длина строки в **файле TCHAR** s, исключая завершающего нуль-символа.</span><span class="sxs-lookup"><span data-stu-id="d382f-117">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="d382f-118">Если параметр *wParam* не указывает допустимый индекс, возвращается значение фунтов \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d382f-118">If *wParam* does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d382f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d382f-119">Remarks</span></span>

<span data-ttu-id="d382f-120">Если список имеет стиль, рисуемый владельцем, но не хасстрингс в [**стиле \_ фунта**](list-box-styles.md) , то буфер, на который указывает параметр *lParam* , получает значение, связанное с элементом (данные элемента).</span><span class="sxs-lookup"><span data-stu-id="d382f-120">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the buffer pointed to by the *lParam* parameter receives the value associated with the item (the item data).</span></span>

## <a name="requirements"></a><span data-ttu-id="d382f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d382f-121">Requirements</span></span>



| <span data-ttu-id="d382f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d382f-122">Requirement</span></span> | <span data-ttu-id="d382f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d382f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d382f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d382f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d382f-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d382f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d382f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d382f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d382f-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d382f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d382f-128">Header</span><span class="sxs-lookup"><span data-stu-id="d382f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d382f-129"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d382f-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d382f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d382f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d382f-131">**жеттекстлен балансировки нагрузки \_**</span><span class="sxs-lookup"><span data-stu-id="d382f-131">**LB\_GETTEXTLEN**</span></span>](lb-gettextlen.md)
</dt> </dl>

 

 





