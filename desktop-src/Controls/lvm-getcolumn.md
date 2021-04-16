---
title: Сообщение LVM_GETCOLUMN (Коммктрл. h)
description: Возвращает атрибуты столбца элемента управления "представление списка". Это сообщение можно отправить явным образом или с помощью \_ макроса DataColumn в ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Элементы управления Windows для LVM_GETCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489066"
---
# <a name="lvm_getcolumn-message"></a><span data-ttu-id="8d4bc-105">\_Сообщение LVM DataColumn</span><span class="sxs-lookup"><span data-stu-id="8d4bc-105">LVM\_GETCOLUMN message</span></span>

<span data-ttu-id="8d4bc-106">Возвращает атрибуты столбца элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="8d4bc-106">Gets the attributes of a list-view control's column.</span></span> <span data-ttu-id="8d4bc-107">Это сообщение можно отправить явным образом или с помощью макроса [**\_ DataColumn в ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .</span><span class="sxs-lookup"><span data-stu-id="8d4bc-107">You can send this message explicitly or by using the [**ListView\_GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d4bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d4bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d4bc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d4bc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d4bc-110">Индекс столбца.</span><span class="sxs-lookup"><span data-stu-id="8d4bc-110">The index of the column.</span></span>

</dd> <dt>

<span data-ttu-id="8d4bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d4bc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d4bc-112">Указатель на структуру [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) , указывающую сведения для извлечения и получения сведений о столбце.</span><span class="sxs-lookup"><span data-stu-id="8d4bc-112">A pointer to an [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure that specifies the information to retrieve and receives information about the column.</span></span> <span data-ttu-id="8d4bc-113">Элемент **Mask** указывает, какие атрибуты столбца следует извлечь.</span><span class="sxs-lookup"><span data-stu-id="8d4bc-113">The **mask** member specifies which column attributes to retrieve.</span></span> <span data-ttu-id="8d4bc-114">Если элемент **Mask** задает \_ текстовое значение лвкф, то элемент **псзтекст** должен содержать адрес буфера, который получает текст элемента, а элемент **кчтекстмакс** должен задавать размер буфера.</span><span class="sxs-lookup"><span data-stu-id="8d4bc-114">If the **mask** member specifies the LVCF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d4bc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d4bc-115">Return value</span></span>

<span data-ttu-id="8d4bc-116">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8d4bc-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d4bc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8d4bc-117">Requirements</span></span>



| <span data-ttu-id="8d4bc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8d4bc-118">Requirement</span></span> | <span data-ttu-id="8d4bc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8d4bc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4bc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d4bc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8d4bc-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8d4bc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d4bc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d4bc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8d4bc-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8d4bc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d4bc-124">Header</span><span class="sxs-lookup"><span data-stu-id="8d4bc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d4bc-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d4bc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





