---
title: Сообщение LVM_GETHEADER (Коммктрл. h)
description: Возвращает маркер элемента управления "заголовок", используемый элементом управления "представление списка". Это сообщение можно отправить явным образом или воспользоваться \_ макросом ListView.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- Элементы управления Windows для LVM_GETHEADER сообщений
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071192"
---
# <a name="lvm_getheader-message"></a><span data-ttu-id="51ad4-105">\_Сообщение LVM</span><span class="sxs-lookup"><span data-stu-id="51ad4-105">LVM\_GETHEADER message</span></span>

<span data-ttu-id="51ad4-106">Возвращает маркер элемента управления "заголовок", используемый элементом управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="51ad4-106">Gets the handle to the header control used by the list-view control.</span></span> <span data-ttu-id="51ad4-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) .</span><span class="sxs-lookup"><span data-stu-id="51ad4-107">You can send this message explicitly or use the [**ListView\_GetHeader**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="51ad4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="51ad4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ad4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51ad4-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="51ad4-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="51ad4-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="51ad4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51ad4-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="51ad4-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="51ad4-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ad4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51ad4-113">Return value</span></span>

<span data-ttu-id="51ad4-114">Возвращает маркер элемента управления заголовка.</span><span class="sxs-lookup"><span data-stu-id="51ad4-114">Returns the handle to the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ad4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="51ad4-115">Requirements</span></span>



| <span data-ttu-id="51ad4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="51ad4-116">Requirement</span></span> | <span data-ttu-id="51ad4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="51ad4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51ad4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51ad4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51ad4-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51ad4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51ad4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51ad4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51ad4-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51ad4-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51ad4-122">Header</span><span class="sxs-lookup"><span data-stu-id="51ad4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="51ad4-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="51ad4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





