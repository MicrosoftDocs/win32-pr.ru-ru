---
title: Сообщение TB_SETINSERTMARK (Коммктрл. h)
description: Задает текущую метку вставки для панели инструментов.
ms.assetid: 9a576fca-89cf-4db5-9840-35bfa56af89e
keywords:
- Элементы управления Windows для TB_SETINSERTMARK сообщений
topic_type:
- apiref
api_name:
- TB_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f65ba83d13cbb45f54833725a46de61a5f0444c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135102"
---
# <a name="tb_setinsertmark-message"></a><span data-ttu-id="25eb9-104">\_Сообщение СЕТИНСЕРТМАРК ТБ</span><span class="sxs-lookup"><span data-stu-id="25eb9-104">TB\_SETINSERTMARK message</span></span>

<span data-ttu-id="25eb9-105">Задает текущую метку вставки для панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="25eb9-105">Sets the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="25eb9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25eb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25eb9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25eb9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="25eb9-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="25eb9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="25eb9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25eb9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25eb9-110">Указатель на структуру [**тбинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) , содержащую метку вставки.</span><span class="sxs-lookup"><span data-stu-id="25eb9-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that contains the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25eb9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25eb9-111">Return value</span></span>

<span data-ttu-id="25eb9-112">Возвращаемое значение для этого сообщения не используется.</span><span class="sxs-lookup"><span data-stu-id="25eb9-112">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="25eb9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="25eb9-113">Requirements</span></span>



| <span data-ttu-id="25eb9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="25eb9-114">Requirement</span></span> | <span data-ttu-id="25eb9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="25eb9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25eb9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25eb9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="25eb9-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25eb9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25eb9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25eb9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="25eb9-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25eb9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25eb9-120">Header</span><span class="sxs-lookup"><span data-stu-id="25eb9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="25eb9-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="25eb9-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25eb9-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25eb9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25eb9-123">**\_ЖЕТИНСЕРТМАРК ТБ**</span><span class="sxs-lookup"><span data-stu-id="25eb9-123">**TB\_GETINSERTMARK**</span></span>](tb-getinsertmark.md)
</dt> </dl>

 

 





