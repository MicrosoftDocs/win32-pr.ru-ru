---
title: Сообщение EM_SETCARETINDEX (Коммктрл. h)
description: Задает значение индекса (с отсчетом от нуля) позиции курсора в элементе управления "поле ввода".
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Элементы управления Windows для EM_SETCARETINDEX сообщений
topic_type:
- apiref
api_name:
- EM_SETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: ea0c49ebad91532e82dc7e96facb62f38b2abfa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492471"
---
# <a name="em_setcaretindex-message"></a><span data-ttu-id="9079e-104">\_Сообщение СЕТКАРЕТИНДЕКС EM</span><span class="sxs-lookup"><span data-stu-id="9079e-104">EM\_SETCARETINDEX message</span></span>

<span data-ttu-id="9079e-105">Задает значение индекса (с отсчетом от нуля) позиции курсора в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="9079e-105">Sets the zero-based index value of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9079e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9079e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9079e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9079e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9079e-108">Новое значение индекса (с отсчетом от нуля) позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="9079e-108">The new zero-based index value of the position of the caret.</span></span>

</dd> <dt>

<span data-ttu-id="9079e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9079e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9079e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9079e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9079e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9079e-111">Return value</span></span>

<span data-ttu-id="9079e-112">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9079e-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9079e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9079e-113">Remarks</span></span>

<span data-ttu-id="9079e-114">Если индекс выходит за пределы диапазона текста в элементе управления "поле ввода", индекс будет настроен таким образом, чтобы он поместился внутри диапазона текста.</span><span class="sxs-lookup"><span data-stu-id="9079e-114">If the index is out of the range of the text in an edit control, the index will be adjusted to fit inside the range of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="9079e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9079e-115">Requirements</span></span>



| <span data-ttu-id="9079e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9079e-116">Requirement</span></span> | <span data-ttu-id="9079e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9079e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9079e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9079e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9079e-119">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="9079e-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9079e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9079e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9079e-121">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="9079e-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9079e-122">Header</span><span class="sxs-lookup"><span data-stu-id="9079e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9079e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9079e-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9079e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9079e-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9079e-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9079e-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9079e-126">**EM \_ жеткаретиндекс**</span><span class="sxs-lookup"><span data-stu-id="9079e-126">**EM\_GETCARETINDEX**</span></span>](em-getcaretindex.md)
</dt> </dl>

 

 





