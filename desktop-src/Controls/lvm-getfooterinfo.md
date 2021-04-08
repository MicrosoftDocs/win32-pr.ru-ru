---
title: Сообщение LVM_GETFOOTERINFO (Коммктрл. h)
description: Возвращает сведения о нижнем колонтитуле элемента управления "представление списка". Отправьте это сообщение явным образом или с помощью \_ макроса Жетфутеринфо ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- Элементы управления Windows для LVM_GETFOOTERINFO сообщений
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988202"
---
# <a name="lvm_getfooterinfo-message"></a><span data-ttu-id="68b5b-105">\_Сообщение LVM жетфутеринфо</span><span class="sxs-lookup"><span data-stu-id="68b5b-105">LVM\_GETFOOTERINFO message</span></span>

<span data-ttu-id="68b5b-106">Возвращает сведения о нижнем колонтитуле элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="68b5b-106">Gets information about the footer of a list-view control.</span></span> <span data-ttu-id="68b5b-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ жетфутеринфо ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .</span><span class="sxs-lookup"><span data-stu-id="68b5b-107">Send this message explicitly or by using the [**ListView\_GetFooterInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="68b5b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68b5b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68b5b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68b5b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68b5b-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="68b5b-110">Not used.</span></span> <span data-ttu-id="68b5b-111">Должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="68b5b-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="68b5b-112">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="68b5b-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="68b5b-113">Указатель на структуру [**лвфутеринфо**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) для получения сведений в зависимости от значения элемента **маски** .</span><span class="sxs-lookup"><span data-stu-id="68b5b-113">A pointer to a [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) structure to receive information depending on the value of the **mask** member.</span></span> <span data-ttu-id="68b5b-114">Вызывающий процесс отвечает за выделение этой структуры и задание элемента **маски** .</span><span class="sxs-lookup"><span data-stu-id="68b5b-114">The calling process is responsible for allocating this structure and setting the **mask** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68b5b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68b5b-115">Return value</span></span>

<span data-ttu-id="68b5b-116">Возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="68b5b-116">Returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b5b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="68b5b-117">Requirements</span></span>



| <span data-ttu-id="68b5b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="68b5b-118">Requirement</span></span> | <span data-ttu-id="68b5b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="68b5b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68b5b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68b5b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="68b5b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68b5b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68b5b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68b5b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="68b5b-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68b5b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68b5b-124">Header</span><span class="sxs-lookup"><span data-stu-id="68b5b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b5b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b5b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





