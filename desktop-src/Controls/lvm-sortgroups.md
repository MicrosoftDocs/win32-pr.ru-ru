---
title: Сообщение LVM_SORTGROUPS (Коммктрл. h)
description: Использует определяемую приложением функцию сравнения для сортировки групп по ИДЕНТИФИКАТОРу в элементе управления "представление списка".
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- Элементы управления Windows для LVM_SORTGROUPS сообщений
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c70fd0f343c9efe0215c87f430e5ed1c89a3aed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137086"
---
# <a name="lvm_sortgroups-message"></a><span data-ttu-id="07392-104">\_Сообщение LVM сортграупс</span><span class="sxs-lookup"><span data-stu-id="07392-104">LVM\_SORTGROUPS message</span></span>

<span data-ttu-id="07392-105">Использует определяемую приложением функцию сравнения для сортировки групп по ИДЕНТИФИКАТОРу в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="07392-105">Uses an application-defined comparison function to sort groups by ID within a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="07392-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07392-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="07392-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="07392-108">Указатель на определяемую приложением функцию сравнения <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">лвграупкомпаре</a>.</span><span class="sxs-lookup"><span data-stu-id="07392-108">Pointer to an application-defined comparison function, <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>.</span></span></dd> <dt>

<span data-ttu-id="07392-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07392-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="07392-110">Указатель void на сведения, определяемые приложением.</span><span class="sxs-lookup"><span data-stu-id="07392-110">Void pointer to the application-defined information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07392-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07392-111">Return value</span></span>

<span data-ttu-id="07392-112">Возвращает 1, если успешно, или 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="07392-112">Returns 1 if successful, or 0 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="07392-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07392-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="07392-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="07392-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="07392-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="07392-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="07392-116">Требования</span><span class="sxs-lookup"><span data-stu-id="07392-116">Requirements</span></span>



| <span data-ttu-id="07392-117">Требование</span><span class="sxs-lookup"><span data-stu-id="07392-117">Requirement</span></span> | <span data-ttu-id="07392-118">Значение</span><span class="sxs-lookup"><span data-stu-id="07392-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07392-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07392-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07392-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07392-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07392-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07392-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07392-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07392-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07392-123">Header</span><span class="sxs-lookup"><span data-stu-id="07392-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="07392-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="07392-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07392-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07392-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07392-126">**лвграупкомпаре**</span><span class="sxs-lookup"><span data-stu-id="07392-126">**LVGroupCompare**</span></span>](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>

