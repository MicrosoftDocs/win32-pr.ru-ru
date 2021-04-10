---
title: Сообщение LVM_INSERTGROUPSORTED (Коммктрл. h)
description: Вставляет группу в упорядоченный список групп.
ms.assetid: 8ad1660b-8b64-4f02-ac1b-b7edeeea38ab
keywords:
- Элементы управления Windows для LVM_INSERTGROUPSORTED сообщений
topic_type:
- apiref
api_name:
- LVM_INSERTGROUPSORTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 485941f803fd5af565d8b40524a9e15968e387cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892434"
---
# <a name="lvm_insertgroupsorted-message"></a><span data-ttu-id="202d2-104">\_Сообщение LVM инсертграупсортед</span><span class="sxs-lookup"><span data-stu-id="202d2-104">LVM\_INSERTGROUPSORTED message</span></span>

<span data-ttu-id="202d2-105">Вставляет группу в упорядоченный список групп.</span><span class="sxs-lookup"><span data-stu-id="202d2-105">Inserts a group into an ordered list of groups.</span></span>

## <a name="parameters"></a><span data-ttu-id="202d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="202d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="202d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="202d2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="202d2-108">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">лвинсертграупсортед</a> , содержащую вставляемую группу.</span><span class="sxs-lookup"><span data-stu-id="202d2-108">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted">LVINSERTGROUPSORTED</a> structure that contains the group to insert.</span></span></dd> <dt>

<span data-ttu-id="202d2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="202d2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="202d2-110">Должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="202d2-110">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="202d2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="202d2-111">Return value</span></span>

<span data-ttu-id="202d2-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="202d2-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="202d2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="202d2-113">Remarks</span></span>

<span data-ttu-id="202d2-114">Порядок расположения списка основан на ИДЕНТИФИКАТОРе группы.</span><span class="sxs-lookup"><span data-stu-id="202d2-114">The ordering of the list is based on the ID of the group.</span></span> <span data-ttu-id="202d2-115">Порядок определяется определяемой приложением функцией упорядочения [**лвграупкомпаре**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), которая передается в структуру [**лвинсертграупсортед**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) с помощью параметра *wParam* .</span><span class="sxs-lookup"><span data-stu-id="202d2-115">The order is defined by the application-defined ordering function, [**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare), that is passed in the [**LVINSERTGROUPSORTED**](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted) structure by the *wParam* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="202d2-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="202d2-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="202d2-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="202d2-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="202d2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="202d2-118">Requirements</span></span>



| <span data-ttu-id="202d2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="202d2-119">Requirement</span></span> | <span data-ttu-id="202d2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="202d2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="202d2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="202d2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="202d2-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="202d2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="202d2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="202d2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="202d2-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="202d2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="202d2-125">Header</span><span class="sxs-lookup"><span data-stu-id="202d2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="202d2-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="202d2-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202d2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="202d2-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="202d2-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="202d2-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="202d2-129">**лвграупкомпаре**</span><span class="sxs-lookup"><span data-stu-id="202d2-129">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> <dt>

[<span data-ttu-id="202d2-130">**лвинсертграупсортед**</span><span class="sxs-lookup"><span data-stu-id="202d2-130">**LVINSERTGROUPSORTED**</span></span>](/windows/win32/api/commctrl/ns-commctrl-lvinsertgroupsorted)
</dt> </dl>

 

