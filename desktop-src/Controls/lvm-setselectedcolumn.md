---
title: Сообщение LVM_SETSELECTEDCOLUMN (Коммктрл. h)
description: Задает индекс выбранного столбца.
ms.assetid: 11b0838e-24a7-4c1c-b67d-0912b5a6442a
keywords:
- Элементы управления Windows для LVM_SETSELECTEDCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_SETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827c41fabaea722bb2372c6bd3f7c3a54bee92f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892838"
---
# <a name="lvm_setselectedcolumn-message"></a><span data-ttu-id="90ff2-104">\_Сообщение LVM сетселектедколумн</span><span class="sxs-lookup"><span data-stu-id="90ff2-104">LVM\_SETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="90ff2-105">Задает индекс выбранного столбца.</span><span class="sxs-lookup"><span data-stu-id="90ff2-105">Sets the index of the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="90ff2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90ff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ff2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90ff2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="90ff2-108">Значение типа **int** , указывающее индекс столбца.</span><span class="sxs-lookup"><span data-stu-id="90ff2-108">Value of type **int** that specifies the column index.</span></span></dd> <dt>

<span data-ttu-id="90ff2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90ff2-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="90ff2-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="90ff2-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ff2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90ff2-111">Return value</span></span>

<span data-ttu-id="90ff2-112">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="90ff2-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ff2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90ff2-113">Remarks</span></span>

<span data-ttu-id="90ff2-114">Индексы столбцов хранятся в массиве **типа int** .</span><span class="sxs-lookup"><span data-stu-id="90ff2-114">The column indices are stored in an **int** array.</span></span> <span data-ttu-id="90ff2-115">См. элемент **пуколумнс** элемента [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span><span class="sxs-lookup"><span data-stu-id="90ff2-115">See the **puColumns** member of [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema).</span></span>

> [!Note]  
> <span data-ttu-id="90ff2-116">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="90ff2-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="90ff2-117">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="90ff2-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90ff2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="90ff2-118">Requirements</span></span>



| <span data-ttu-id="90ff2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="90ff2-119">Requirement</span></span> | <span data-ttu-id="90ff2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="90ff2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90ff2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90ff2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="90ff2-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90ff2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90ff2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90ff2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="90ff2-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90ff2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90ff2-125">Header</span><span class="sxs-lookup"><span data-stu-id="90ff2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="90ff2-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="90ff2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





