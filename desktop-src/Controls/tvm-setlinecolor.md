---
title: Сообщение TVM_SETLINECOLOR (Коммктрл. h)
description: В \_ сообщении TVM сетлинеколор устанавливается текущий цвет линии.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- Элементы управления Windows для TVM_SETLINECOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071735"
---
# <a name="tvm_setlinecolor-message"></a><span data-ttu-id="c7a60-104">\_Сообщение TVM сетлинеколор</span><span class="sxs-lookup"><span data-stu-id="c7a60-104">TVM\_SETLINECOLOR message</span></span>

<span data-ttu-id="c7a60-105">В сообщении **TVM \_ сетлинеколор** устанавливается текущий цвет линии.</span><span class="sxs-lookup"><span data-stu-id="c7a60-105">The **TVM\_SETLINECOLOR** message sets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7a60-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7a60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7a60-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7a60-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c7a60-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="c7a60-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c7a60-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7a60-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7a60-110">Цвет новой линии.</span><span class="sxs-lookup"><span data-stu-id="c7a60-110">New line color.</span></span> <span data-ttu-id="c7a60-111">Используйте \_ значение по умолчанию CLR для восстановления системных цветов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7a60-111">Use the CLR\_DEFAULT value to restore the system default colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7a60-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7a60-112">Return value</span></span>

<span data-ttu-id="c7a60-113">Возвращает цвет предыдущей строки.</span><span class="sxs-lookup"><span data-stu-id="c7a60-113">Returns the previous line color.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a60-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7a60-114">Remarks</span></span>

<span data-ttu-id="c7a60-115">Это сообщение изменяет только цвета линий.</span><span class="sxs-lookup"><span data-stu-id="c7a60-115">This message only changes line colors.</span></span> <span data-ttu-id="c7a60-116">Чтобы изменить цвета "+" и "-" внутри кнопок, используйте сообщение [**TVM \_ сеттекстколор**](tvm-settextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="c7a60-116">To change the colors of the '+' and '-' inside the buttons, use the [**TVM\_SETTEXTCOLOR**](tvm-settextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a60-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c7a60-117">Requirements</span></span>



| <span data-ttu-id="c7a60-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c7a60-118">Requirement</span></span> | <span data-ttu-id="c7a60-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c7a60-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a60-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7a60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a60-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7a60-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7a60-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7a60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a60-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7a60-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7a60-124">Header</span><span class="sxs-lookup"><span data-stu-id="c7a60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7a60-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7a60-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7a60-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7a60-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a60-127">**TVM \_ жетлинеколор**</span><span class="sxs-lookup"><span data-stu-id="c7a60-127">**TVM\_GETLINECOLOR**</span></span>](tvm-getlinecolor.md)
</dt> </dl>

 

 





