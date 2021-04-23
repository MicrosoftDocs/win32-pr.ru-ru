---
title: Сообщение CB_SETCUEBANNER (Winuser. h)
description: Задает текст баннера подсказки, отображаемый для элемента управления "поле ввода" поля со списком.
ms.assetid: 4b2b5042-ba64-4e3f-adeb-9aea66773b0e
keywords:
- Элементы управления Windows для CB_SETCUEBANNER сообщений
topic_type:
- apiref
api_name:
- CB_SETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5799b1b1be5e938ce1e234948a1f7d878122f30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071610"
---
# <a name="cb_setcuebanner-message"></a><span data-ttu-id="feb4c-104">\_Сообщение СЕТКУЕБАННЕР CB</span><span class="sxs-lookup"><span data-stu-id="feb4c-104">CB\_SETCUEBANNER message</span></span>

<span data-ttu-id="feb4c-105">Задает текст баннера подсказки, отображаемый для элемента управления "поле ввода" поля со списком.</span><span class="sxs-lookup"><span data-stu-id="feb4c-105">Sets the cue banner text that is displayed for the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="feb4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="feb4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb4c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="feb4c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feb4c-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="feb4c-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="feb4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="feb4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="feb4c-110">Указатель на завершающийся нулем буфер строки в Юникоде, содержащий текст.</span><span class="sxs-lookup"><span data-stu-id="feb4c-110">A pointer to a null-terminated Unicode string buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb4c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="feb4c-111">Return value</span></span>

<span data-ttu-id="feb4c-112">Возвращает 1 в случае успеха или значение ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="feb4c-112">Returns 1 if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb4c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="feb4c-113">Remarks</span></span>

<span data-ttu-id="feb4c-114">Баннер подсказки — это текст, отображаемый в элементе управления "поле со списком" при отсутствии выделения.</span><span class="sxs-lookup"><span data-stu-id="feb4c-114">The cue banner is text that is displayed in the edit control of a combo box when there is no selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb4c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="feb4c-115">Requirements</span></span>



| <span data-ttu-id="feb4c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="feb4c-116">Requirement</span></span> | <span data-ttu-id="feb4c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="feb4c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb4c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="feb4c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="feb4c-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="feb4c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="feb4c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="feb4c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="feb4c-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="feb4c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="feb4c-122">Header</span><span class="sxs-lookup"><span data-stu-id="feb4c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="feb4c-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="feb4c-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb4c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feb4c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb4c-125">Возможности поля со списком</span><span class="sxs-lookup"><span data-stu-id="feb4c-125">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





