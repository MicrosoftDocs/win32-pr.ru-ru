---
title: Сообщение BM_SETDONTCLICK (Winuser. h)
description: Устанавливает флаг на переключателе, который управляет созданием млрд ДОЛЛных \_ сообщений, когда кнопка получает фокус.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- Элементы управления Windows для BM_SETDONTCLICK сообщений
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654448"
---
# <a name="bm_setdontclick-message"></a><span data-ttu-id="4cfb6-104">\_Сообщение BM сетдонткликк</span><span class="sxs-lookup"><span data-stu-id="4cfb6-104">BM\_SETDONTCLICK message</span></span>

<span data-ttu-id="4cfb6-105">Устанавливает флаг на переключателе, который управляет созданием [млрд доллных сообщений \_ ](bn-clicked.md) , когда кнопка получает фокус.</span><span class="sxs-lookup"><span data-stu-id="4cfb6-105">Sets a flag on a radio button that controls the generation of [BN\_CLICKED](bn-clicked.md) messages when the button receives focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cfb6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cfb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cfb6-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4cfb6-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cfb6-108">**Логическое** значение, указывающее состояние.</span><span class="sxs-lookup"><span data-stu-id="4cfb6-108">A **BOOL** that specifies the state.</span></span> <span data-ttu-id="4cfb6-109">**Значение true** , чтобы установить флаг; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4cfb6-109">**TRUE** to set the flag, otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4cfb6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cfb6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cfb6-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="4cfb6-111">Not used.</span></span> <span data-ttu-id="4cfb6-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4cfb6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cfb6-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cfb6-113">Return value</span></span>

<span data-ttu-id="4cfb6-114">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4cfb6-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfb6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4cfb6-115">Requirements</span></span>



| <span data-ttu-id="4cfb6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4cfb6-116">Requirement</span></span> | <span data-ttu-id="4cfb6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4cfb6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfb6-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cfb6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4cfb6-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cfb6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4cfb6-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cfb6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4cfb6-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cfb6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4cfb6-122">Header</span><span class="sxs-lookup"><span data-stu-id="4cfb6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cfb6-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb6-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





