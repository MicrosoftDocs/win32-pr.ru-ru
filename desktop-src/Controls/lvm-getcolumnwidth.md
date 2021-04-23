---
title: Сообщение LVM_GETCOLUMNWIDTH (Коммктрл. h)
description: Возвращает ширину столбца в представлении отчета или списка. Это сообщение можно отправить явно или с помощью \_ макроса Жетколумнвидс ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Элементы управления Windows для LVM_GETCOLUMNWIDTH сообщений
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135134"
---
# <a name="lvm_getcolumnwidth-message"></a><span data-ttu-id="9b6f4-105">\_Сообщение LVM жетколумнвидс</span><span class="sxs-lookup"><span data-stu-id="9b6f4-105">LVM\_GETCOLUMNWIDTH message</span></span>

<span data-ttu-id="9b6f4-106">Возвращает ширину столбца в представлении отчета или списка.</span><span class="sxs-lookup"><span data-stu-id="9b6f4-106">Gets the width of a column in report or list view.</span></span> <span data-ttu-id="9b6f4-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жетколумнвидс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="9b6f4-107">You can send this message explicitly or by using the [**ListView\_GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9b6f4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b6f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b6f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b6f4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b6f4-110">Индекс столбца.</span><span class="sxs-lookup"><span data-stu-id="9b6f4-110">The index of the column.</span></span> <span data-ttu-id="9b6f4-111">Этот параметр не учитывается в представлении списка.</span><span class="sxs-lookup"><span data-stu-id="9b6f4-111">This parameter is ignored in list view.</span></span>

</dd> <dt>

<span data-ttu-id="9b6f4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b6f4-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9b6f4-113">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9b6f4-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b6f4-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b6f4-114">Return value</span></span>

<span data-ttu-id="9b6f4-115">Возвращает ширину столбца в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9b6f4-115">Returns the column width if successful, or zero otherwise.</span></span> <span data-ttu-id="9b6f4-116">Если это сообщение отправлено в элемент управления "представление списка" с использованием стиля [**\_ отчета LVS**](list-view-window-styles.md) , а указанный столбец не существует, возвращаемое значение не определено.</span><span class="sxs-lookup"><span data-stu-id="9b6f4-116">If this message is sent to a list-view control with the [**LVS\_REPORT**](list-view-window-styles.md) style and the specified column does not exist, the return value is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6f4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9b6f4-117">Requirements</span></span>



| <span data-ttu-id="9b6f4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9b6f4-118">Requirement</span></span> | <span data-ttu-id="9b6f4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9b6f4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6f4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b6f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9b6f4-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b6f4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9b6f4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b6f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9b6f4-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b6f4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b6f4-124">Header</span><span class="sxs-lookup"><span data-stu-id="9b6f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b6f4-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b6f4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





