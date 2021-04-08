---
title: Сообщение IPM_GETADDRESS (Коммктрл. h)
description: Возвращает значения адреса для всех четырех полей в элементе управления IP-адреса.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- Элементы управления Windows для IPM_GETADDRESS сообщений
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988911"
---
# <a name="ipm_getaddress-message"></a><span data-ttu-id="57ef9-104">Сообщение IPM. \_ Address</span><span class="sxs-lookup"><span data-stu-id="57ef9-104">IPM\_GETADDRESS message</span></span>

<span data-ttu-id="57ef9-105">Возвращает значения адреса для всех четырех полей в элементе управления IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="57ef9-105">Gets the address values for all four fields in the IP address control.</span></span>

## <a name="parameters"></a><span data-ttu-id="57ef9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57ef9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ef9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57ef9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="57ef9-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="57ef9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="57ef9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57ef9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57ef9-110">Указатель на значение **DWORD** , получающее адрес.</span><span class="sxs-lookup"><span data-stu-id="57ef9-110">A pointer to a **DWORD** value that receives the address.</span></span> <span data-ttu-id="57ef9-111">Значение поля 3 будет содержаться в битах от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="57ef9-111">The field 3 value will be contained in bits 0 through 7.</span></span> <span data-ttu-id="57ef9-112">Значение поля 2 будет содержаться в битах 8 – 15.</span><span class="sxs-lookup"><span data-stu-id="57ef9-112">The field 2 value will be contained in bits 8 through 15.</span></span> <span data-ttu-id="57ef9-113">Значение поля 1 будет содержаться в битах от 16 до 23.</span><span class="sxs-lookup"><span data-stu-id="57ef9-113">The field 1 value will be contained in bits 16 through 23.</span></span> <span data-ttu-id="57ef9-114">Значение поля 0 будет содержаться в битах с 24 по 31.</span><span class="sxs-lookup"><span data-stu-id="57ef9-114">The field 0 value will be contained in bits 24 through 31.</span></span> <span data-ttu-id="57ef9-115">Для извлечения сведений об адресе также можно использовать [**первый \_ IP**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)-адрес, [**второй \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**третий \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)и [**четвертый \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) .</span><span class="sxs-lookup"><span data-stu-id="57ef9-115">The [**FIRST\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress), and [**FOURTH\_IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) macros can also be used to extract the address information.</span></span> <span data-ttu-id="57ef9-116">Ноль будет возвращен в качестве адреса для любых пустых полей.</span><span class="sxs-lookup"><span data-stu-id="57ef9-116">Zero will be returned as the address for any blank fields.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ef9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57ef9-117">Return value</span></span>

<span data-ttu-id="57ef9-118">Возвращает количество непустых полей.</span><span class="sxs-lookup"><span data-stu-id="57ef9-118">Returns the number of nonblank fields.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ef9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="57ef9-119">Requirements</span></span>



| <span data-ttu-id="57ef9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="57ef9-120">Requirement</span></span> | <span data-ttu-id="57ef9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="57ef9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57ef9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57ef9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57ef9-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57ef9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57ef9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57ef9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57ef9-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57ef9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57ef9-126">Header</span><span class="sxs-lookup"><span data-stu-id="57ef9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ef9-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ef9-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





