---
title: Сообщение CB_GETCOMBOBOXINFO (Winuser. h)
description: Возвращает сведения об указанном поле со списком.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- Элементы управления Windows для CB_GETCOMBOBOXINFO сообщений
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd7052ef4feca8a8704258c7c34d6516c7cd6cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489300"
---
# <a name="cb_getcomboboxinfo-message"></a><span data-ttu-id="b9a7d-104">\_Сообщение ЖЕТКОМБОБОКСИНФО CB</span><span class="sxs-lookup"><span data-stu-id="b9a7d-104">CB\_GETCOMBOBOXINFO message</span></span>

<span data-ttu-id="b9a7d-105">Возвращает сведения об указанном поле со списком.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-105">Gets information about the specified combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9a7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9a7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9a7d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b9a7d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b9a7d-108">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b9a7d-109">*lParam* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b9a7d-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9a7d-110">Указатель на структуру [**комбобоксинфо**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) , которая получает сведения.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-110">A pointer to a [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9a7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9a7d-111">Return value</span></span>

<span data-ttu-id="b9a7d-112">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-112">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="b9a7d-113">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b9a7d-113">If the function fails, the return value is zero.</span></span> <span data-ttu-id="b9a7d-114">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b9a7d-114">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9a7d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9a7d-115">Remarks</span></span>

<span data-ttu-id="b9a7d-116">Это сообщение эквивалентно [**жеткомбобоксинфо**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span><span class="sxs-lookup"><span data-stu-id="b9a7d-116">This message is equivalent to [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9a7d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b9a7d-117">Requirements</span></span>



| <span data-ttu-id="b9a7d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b9a7d-118">Requirement</span></span> | <span data-ttu-id="b9a7d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b9a7d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a7d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9a7d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b9a7d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9a7d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b9a7d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9a7d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b9a7d-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b9a7d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b9a7d-124">Header</span><span class="sxs-lookup"><span data-stu-id="b9a7d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9a7d-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b9a7d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9a7d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9a7d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b9a7d-127">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b9a7d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b9a7d-128">**комбобоксинфо**</span><span class="sxs-lookup"><span data-stu-id="b9a7d-128">**COMBOBOXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[<span data-ttu-id="b9a7d-129">**жеткомбобоксинфо**</span><span class="sxs-lookup"><span data-stu-id="b9a7d-129">**GetComboBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

