---
title: Сообщение EM_GETCARETINDEX (Коммктрл. h)
description: Возвращает отсчитываемый от нуля индекс позиции курсора в элементе управления "поле ввода".
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- Элементы управления Windows для EM_GETCARETINDEX сообщений
topic_type:
- apiref
api_name:
- EM_GETCARETINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6653e2ae0e2126941e3d8977a593300b86051800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988769"
---
# <a name="em_getcaretindex-message"></a><span data-ttu-id="24cf6-104">\_Сообщение ЖЕТКАРЕТИНДЕКС EM</span><span class="sxs-lookup"><span data-stu-id="24cf6-104">EM\_GETCARETINDEX message</span></span>

<span data-ttu-id="24cf6-105">Возвращает отсчитываемый от нуля индекс позиции курсора в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="24cf6-105">Gets the zero-based index of the position of the caret in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="24cf6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="24cf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24cf6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24cf6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="24cf6-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="24cf6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="24cf6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24cf6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="24cf6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="24cf6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24cf6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24cf6-111">Return value</span></span>

<span data-ttu-id="24cf6-112">Возвращаемое значение — это отсчитываемое от нуля значение индекса позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="24cf6-112">The return value is a zero-based index value of the position of the caret.</span></span>

## <a name="requirements"></a><span data-ttu-id="24cf6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="24cf6-113">Requirements</span></span>



| <span data-ttu-id="24cf6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="24cf6-114">Requirement</span></span> | <span data-ttu-id="24cf6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="24cf6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24cf6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24cf6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24cf6-117">Windows 10, \[ только классические приложения 1809\]</span><span class="sxs-lookup"><span data-stu-id="24cf6-117">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="24cf6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24cf6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24cf6-119">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="24cf6-119">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24cf6-120">Header</span><span class="sxs-lookup"><span data-stu-id="24cf6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="24cf6-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="24cf6-121"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24cf6-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24cf6-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="24cf6-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="24cf6-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24cf6-124">**EM \_ сеткаретиндекс**</span><span class="sxs-lookup"><span data-stu-id="24cf6-124">**EM\_SETCARETINDEX**</span></span>](em-setcaretindex.md)
</dt> </dl>

 

 





