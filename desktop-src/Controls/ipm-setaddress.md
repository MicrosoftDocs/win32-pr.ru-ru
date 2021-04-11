---
title: Сообщение IPM_SETADDRESS (Коммктрл. h)
description: Задает значения адреса для всех четырех полей в элементе управления "IP-адрес".
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- Элементы управления Windows для IPM_SETADDRESS сообщений
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136422"
---
# <a name="ipm_setaddress-message"></a><span data-ttu-id="e88be-104">\_Сообщение IPM сетаддресс</span><span class="sxs-lookup"><span data-stu-id="e88be-104">IPM\_SETADDRESS message</span></span>

<span data-ttu-id="e88be-105">Задает значения адреса для всех четырех полей в элементе управления "IP-адрес".</span><span class="sxs-lookup"><span data-stu-id="e88be-105">Sets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e88be-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e88be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e88be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e88be-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e88be-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e88be-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e88be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e88be-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e88be-110">Значение **типа DWORD** , содержащее новый адрес.</span><span class="sxs-lookup"><span data-stu-id="e88be-110">A **DWORD** value that contains the new address.</span></span> <span data-ttu-id="e88be-111">Значение поля 3 содержится в битах от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="e88be-111">The field 3 value is contained in bits 0 through 7.</span></span> <span data-ttu-id="e88be-112">Значение поля 2 содержится в битах от 8 до 15.</span><span class="sxs-lookup"><span data-stu-id="e88be-112">The field 2 value is contained in bits 8 through 15.</span></span> <span data-ttu-id="e88be-113">Значение поля 1 содержится в битах от 16 до 23.</span><span class="sxs-lookup"><span data-stu-id="e88be-113">The field 1 value is contained in bits 16 through 23.</span></span> <span data-ttu-id="e88be-114">Значение поля 0 содержится в битах с 24 по 31.</span><span class="sxs-lookup"><span data-stu-id="e88be-114">The field 0 value is contained in bits 24 through 31.</span></span> <span data-ttu-id="e88be-115">Для создания сведений об адресе также можно использовать макрос [**макеипаддресс**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) .</span><span class="sxs-lookup"><span data-stu-id="e88be-115">The [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) macro can also be used to create the address information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e88be-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e88be-116">Return value</span></span>

<span data-ttu-id="e88be-117">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="e88be-117">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="e88be-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e88be-118">Remarks</span></span>

<span data-ttu-id="e88be-119">Это сообщение не создает уведомление [**ИПН \_ фиелдчанжед**](ipn-fieldchanged.md) .</span><span class="sxs-lookup"><span data-stu-id="e88be-119">This message does not generate an [**IPN\_FIELDCHANGED**](ipn-fieldchanged.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="e88be-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e88be-120">Requirements</span></span>



| <span data-ttu-id="e88be-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e88be-121">Requirement</span></span> | <span data-ttu-id="e88be-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e88be-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e88be-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e88be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e88be-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e88be-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e88be-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e88be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e88be-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e88be-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e88be-127">Header</span><span class="sxs-lookup"><span data-stu-id="e88be-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e88be-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e88be-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





