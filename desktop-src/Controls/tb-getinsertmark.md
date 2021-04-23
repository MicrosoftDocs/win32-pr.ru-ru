---
title: Сообщение TB_GETINSERTMARK (Коммктрл. h)
description: Извлекает текущую метку вставки для панели инструментов.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- Элементы управления Windows для TB_GETINSERTMARK сообщений
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071248"
---
# <a name="tb_getinsertmark-message"></a><span data-ttu-id="000be-104">\_Сообщение ЖЕТИНСЕРТМАРК ТБ</span><span class="sxs-lookup"><span data-stu-id="000be-104">TB\_GETINSERTMARK message</span></span>

<span data-ttu-id="000be-105">Извлекает текущую метку вставки для панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="000be-105">Retrieves the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="000be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="000be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="000be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="000be-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="000be-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="000be-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="000be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="000be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="000be-110">Указатель на структуру [**тбинсертмарк**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) , которая получает метку вставки.</span><span class="sxs-lookup"><span data-stu-id="000be-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="000be-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="000be-111">Return value</span></span>

<span data-ttu-id="000be-112">Всегда возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="000be-112">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="000be-113">Требования</span><span class="sxs-lookup"><span data-stu-id="000be-113">Requirements</span></span>



| <span data-ttu-id="000be-114">Требование</span><span class="sxs-lookup"><span data-stu-id="000be-114">Requirement</span></span> | <span data-ttu-id="000be-115">Значение</span><span class="sxs-lookup"><span data-stu-id="000be-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="000be-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="000be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="000be-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="000be-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="000be-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="000be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="000be-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="000be-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="000be-120">Header</span><span class="sxs-lookup"><span data-stu-id="000be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="000be-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="000be-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="000be-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="000be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="000be-123">**\_СЕТИНСЕРТМАРК ТБ**</span><span class="sxs-lookup"><span data-stu-id="000be-123">**TB\_SETINSERTMARK**</span></span>](tb-setinsertmark.md)
</dt> </dl>

 

 





