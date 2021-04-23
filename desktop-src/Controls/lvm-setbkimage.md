---
title: Сообщение LVM_SETBKIMAGE (Коммктрл. h)
description: Задает фоновое изображение в элементе управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Сетбкимаже ListView.
ms.assetid: 8fdd363c-ac12-498b-80b7-aaa5741cfd76
keywords:
- Элементы управления Windows для LVM_SETBKIMAGE сообщений
topic_type:
- apiref
api_name:
- LVM_SETBKIMAGE
- LVM_SETBKIMAGEA
- LVM_SETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e22bebdcb36faff56dfabab721731acb55fdec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491457"
---
# <a name="lvm_setbkimage-message"></a><span data-ttu-id="1082a-105">\_Сообщение LVM сетбкимаже</span><span class="sxs-lookup"><span data-stu-id="1082a-105">LVM\_SETBKIMAGE message</span></span>

<span data-ttu-id="1082a-106">Задает фоновое изображение в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="1082a-106">Sets the background image in a list-view control.</span></span> <span data-ttu-id="1082a-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетбкимаже ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) .</span><span class="sxs-lookup"><span data-stu-id="1082a-107">You can send this message explicitly or by using the [**ListView\_SetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1082a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1082a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1082a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1082a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1082a-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1082a-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1082a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1082a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1082a-112">Указатель на структуру [**лвбкимаже**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) , содержащую новые сведения о фоновом изображении.</span><span class="sxs-lookup"><span data-stu-id="1082a-112">Pointer to a [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure that contains the new background image information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1082a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1082a-113">Return value</span></span>

<span data-ttu-id="1082a-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1082a-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="1082a-115">Возвращает нуль, если элемент **улфлагс** структуры [**Лвбкимаже**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) имеет значение **лвбкиф \_ source \_ None**.</span><span class="sxs-lookup"><span data-stu-id="1082a-115">Returns zero if the **ulFlags** member of the [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) structure is **LVBKIF\_SOURCE\_NONE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1082a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1082a-116">Remarks</span></span>

<span data-ttu-id="1082a-117">Так как элемент управления "представление списка" использует OLE COM для работы с фоновыми изображениями, вызывающее приложение должно вызвать [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**олеинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) перед отправкой этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="1082a-117">Because the list-view control uses OLE COM to manipulate the background images, the calling application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before sending this message.</span></span> <span data-ttu-id="1082a-118">Рекомендуется вызывать одну из этих функций при инициализации приложения и вызывать [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) или [**олеунинитиализе**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) при завершении работы приложения.</span><span class="sxs-lookup"><span data-stu-id="1082a-118">It is best to call one of these functions when the application is initialized and call either [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) or [**OleUninitialize**](/windows/desktop/api/ole2/nf-ole2-oleuninitialize) when the application is terminating.</span></span>

## <a name="requirements"></a><span data-ttu-id="1082a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1082a-119">Requirements</span></span>



| <span data-ttu-id="1082a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1082a-120">Requirement</span></span> | <span data-ttu-id="1082a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1082a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1082a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1082a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1082a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1082a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1082a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1082a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1082a-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1082a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1082a-126">Header</span><span class="sxs-lookup"><span data-stu-id="1082a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1082a-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1082a-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="1082a-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="1082a-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1082a-129">**LVM \_ СЕТБКИМАЖЕВ** (Юникод) и **LVM \_ сетбкимажеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1082a-129">**LVM\_SETBKIMAGEW** (Unicode) and **LVM\_SETBKIMAGEA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1082a-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1082a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1082a-131">**LVM \_ жетбкимаже**</span><span class="sxs-lookup"><span data-stu-id="1082a-131">**LVM\_GETBKIMAGE**</span></span>](lvm-getbkimage.md)
</dt> </dl>

 

