---
title: Сообщение TVM_GETLINECOLOR (Коммктрл. h)
description: Сообщение TVM \_ жетлинеколор получает текущий цвет линии.
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- Элементы управления Windows для TVM_GETLINECOLOR сообщений
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071773"
---
# <a name="tvm_getlinecolor-message"></a><span data-ttu-id="486bc-104">\_Сообщение TVM жетлинеколор</span><span class="sxs-lookup"><span data-stu-id="486bc-104">TVM\_GETLINECOLOR message</span></span>

<span data-ttu-id="486bc-105">Сообщение **TVM \_ жетлинеколор** получает текущий цвет линии.</span><span class="sxs-lookup"><span data-stu-id="486bc-105">The **TVM\_GETLINECOLOR** message gets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="486bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="486bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="486bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="486bc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="486bc-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="486bc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="486bc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="486bc-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="486bc-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="486bc-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="486bc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="486bc-111">Return value</span></span>

<span data-ttu-id="486bc-112">Возвращает текущий цвет строки или \_ значение CLR по умолчанию, если ничего не указано.</span><span class="sxs-lookup"><span data-stu-id="486bc-112">Returns the current line color, or the CLR\_DEFAULT value if none has been specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="486bc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="486bc-113">Remarks</span></span>

<span data-ttu-id="486bc-114">Это сообщение получает только цвета линий.</span><span class="sxs-lookup"><span data-stu-id="486bc-114">This message only retrieves line colors.</span></span> <span data-ttu-id="486bc-115">Чтобы получить цвета "+" и "-" внутри кнопок, используйте сообщение [**TVM \_ жеттекстколор**](tvm-gettextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="486bc-115">To retrieve the colors of the '+' and '-' inside the buttons, use the [**TVM\_GETTEXTCOLOR**](tvm-gettextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="486bc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="486bc-116">Requirements</span></span>



| <span data-ttu-id="486bc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="486bc-117">Requirement</span></span> | <span data-ttu-id="486bc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="486bc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="486bc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="486bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="486bc-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="486bc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="486bc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="486bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="486bc-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="486bc-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="486bc-123">Header</span><span class="sxs-lookup"><span data-stu-id="486bc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="486bc-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="486bc-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="486bc-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="486bc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="486bc-126">**TVM \_ сетлинеколор**</span><span class="sxs-lookup"><span data-stu-id="486bc-126">**TVM\_SETLINECOLOR**</span></span>](tvm-setlinecolor.md)
</dt> </dl>

 

 





