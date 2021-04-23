---
title: Сообщение LVM_GETSELECTEDCOLUMN (Коммктрл. h)
description: Извлекает целое число, указывающее выбранный столбец.
ms.assetid: 5aba5d96-50fd-439b-9782-fd5d8684b17f
keywords:
- Элементы управления Windows для LVM_GETSELECTEDCOLUMN сообщений
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ffae9a9c7812f025241f5b46f3b1ea61bb88bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341000"
---
# <a name="lvm_getselectedcolumn-message"></a><span data-ttu-id="2bab6-104">\_Сообщение LVM жетселектедколумн</span><span class="sxs-lookup"><span data-stu-id="2bab6-104">LVM\_GETSELECTEDCOLUMN message</span></span>

<span data-ttu-id="2bab6-105">Извлекает целое число, указывающее выбранный столбец.</span><span class="sxs-lookup"><span data-stu-id="2bab6-105">Retrieves an integer that specifies the selected column.</span></span>

## <a name="parameters"></a><span data-ttu-id="2bab6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2bab6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bab6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2bab6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2bab6-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2bab6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2bab6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2bab6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2bab6-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="2bab6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bab6-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2bab6-111">Return value</span></span>

<span data-ttu-id="2bab6-112">Возвращает значение типа **uint** , указывающее выбранный столбец.</span><span class="sxs-lookup"><span data-stu-id="2bab6-112">Returns an **UINT** that specifies the selected column.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bab6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2bab6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2bab6-114">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="2bab6-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="2bab6-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2bab6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2bab6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2bab6-116">Requirements</span></span>



| <span data-ttu-id="2bab6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2bab6-117">Requirement</span></span> | <span data-ttu-id="2bab6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2bab6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bab6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2bab6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bab6-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2bab6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2bab6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2bab6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bab6-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2bab6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2bab6-123">Header</span><span class="sxs-lookup"><span data-stu-id="2bab6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bab6-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bab6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





