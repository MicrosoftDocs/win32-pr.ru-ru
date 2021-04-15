---
title: Сообщение TB_CUSTOMIZE (Коммктрл. h)
description: Отображает диалоговое окно Настройка панели инструментов.
ms.assetid: 45249467-d585-4ffd-8bbe-e39739059c40
keywords:
- Элементы управления Windows для TB_CUSTOMIZE сообщений
topic_type:
- apiref
api_name:
- TB_CUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dada0ef195e898b7a46487a2d775e46d6af854ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654718"
---
# <a name="tb_customize-message"></a><span data-ttu-id="42020-104">\_Настраиваемое сообщение (ТБ)</span><span class="sxs-lookup"><span data-stu-id="42020-104">TB\_CUSTOMIZE message</span></span>

<span data-ttu-id="42020-105">Отображает диалоговое окно **Настройка панели инструментов** .</span><span class="sxs-lookup"><span data-stu-id="42020-105">Displays the **Customize Toolbar** dialog box.</span></span>

## <a name="parameters"></a><span data-ttu-id="42020-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="42020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42020-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42020-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42020-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="42020-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="42020-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42020-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42020-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="42020-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42020-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42020-111">Return value</span></span>

<span data-ttu-id="42020-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="42020-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42020-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="42020-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42020-114">Панель инструментов должна поддерживать уведомления [ТБН \_ Куеринсерт](tbn-queryinsert.md) и [ТБН \_ куериделете](tbn-querydelete.md) для отображения диалогового окна **Настройка панели инструментов** .</span><span class="sxs-lookup"><span data-stu-id="42020-114">The toolbar must handle the [TBN\_QUERYINSERT](tbn-queryinsert.md) and [TBN\_QUERYDELETE](tbn-querydelete.md) notifications for the **Customize Toolbar** dialog box to appear.</span></span> <span data-ttu-id="42020-115">Если панель инструментов не обрабатывает эти уведомления, **\_ Настройка ТБ** не влияет.</span><span class="sxs-lookup"><span data-stu-id="42020-115">If the toolbar does not handle those notifications, **TB\_CUSTOMIZE** has no effect.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42020-116">Требования</span><span class="sxs-lookup"><span data-stu-id="42020-116">Requirements</span></span>



| <span data-ttu-id="42020-117">Требование</span><span class="sxs-lookup"><span data-stu-id="42020-117">Requirement</span></span> | <span data-ttu-id="42020-118">Значение</span><span class="sxs-lookup"><span data-stu-id="42020-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42020-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42020-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42020-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42020-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42020-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42020-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42020-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42020-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42020-123">Header</span><span class="sxs-lookup"><span data-stu-id="42020-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42020-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="42020-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





