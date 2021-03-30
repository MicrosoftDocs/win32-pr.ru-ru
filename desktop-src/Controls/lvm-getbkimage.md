---
title: Сообщение LVM_GETBKIMAGE (Коммктрл. h)
description: Возвращает фоновое изображение в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жетбкимаже ListView.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- Элементы управления Windows для LVM_GETBKIMAGE сообщений
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801120"
---
# <a name="lvm_getbkimage-message"></a><span data-ttu-id="4a1b5-105">\_Сообщение LVM жетбкимаже</span><span class="sxs-lookup"><span data-stu-id="4a1b5-105">LVM\_GETBKIMAGE message</span></span>

<span data-ttu-id="4a1b5-106">Возвращает фоновое изображение в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="4a1b5-106">Gets the background image in a list-view control.</span></span> <span data-ttu-id="4a1b5-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетбкимаже ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .</span><span class="sxs-lookup"><span data-stu-id="4a1b5-107">You can send this message explicitly or by using the [**ListView\_GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a1b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a1b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a1b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a1b5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4a1b5-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4a1b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a1b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1b5-112">Указатель на структуру [**лвбкимаже**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) , которая получит сведения о фоновом изображении.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-112">A pointer to an [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that will receive the background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a1b5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a1b5-113">Return value</span></span>

<span data-ttu-id="4a1b5-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a1b5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4a1b5-115">Requirements</span></span>



| <span data-ttu-id="4a1b5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4a1b5-116">Requirement</span></span> | <span data-ttu-id="4a1b5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4a1b5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1b5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a1b5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a1b5-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a1b5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a1b5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a1b5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a1b5-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a1b5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a1b5-122">Header</span><span class="sxs-lookup"><span data-stu-id="4a1b5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a1b5-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a1b5-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="4a1b5-124">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="4a1b5-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4a1b5-125">**LVM \_ ЖЕТБКИМАЖЕВ** (Юникод) и **LVM \_ жетбкимажеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4a1b5-125">**LVM\_GETBKIMAGEW** (Unicode) and **LVM\_GETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="4a1b5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a1b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1b5-127">**LVM \_ сетбкимаже**</span><span class="sxs-lookup"><span data-stu-id="4a1b5-127">**LVM\_SETBKIMAGE**</span></span>](lvm-setbkimage.md)
</dt> </dl>

 

 





