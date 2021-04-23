---
title: Сообщение RB_GETROWHEIGHT (Коммктрл. h)
description: Получает высоту указанной строки в элементе управления "Главная панель".
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- Элементы управления Windows для RB_GETROWHEIGHT сообщений
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ce137eef6168d95abfe493a6f22ab66d58460b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892237"
---
# <a name="rb_getrowheight-message"></a><span data-ttu-id="1199e-104">\_Сообщение ЖЕТРОВХЕИГХТ RB</span><span class="sxs-lookup"><span data-stu-id="1199e-104">RB\_GETROWHEIGHT message</span></span>

<span data-ttu-id="1199e-105">Получает высоту указанной строки в элементе управления "Главная панель".</span><span class="sxs-lookup"><span data-stu-id="1199e-105">Retrieves the height of a specified row in a rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1199e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1199e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1199e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1199e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1199e-108">Отсчитываемый от нуля индекс диапазона.</span><span class="sxs-lookup"><span data-stu-id="1199e-108">Zero-based index of a band.</span></span> <span data-ttu-id="1199e-109">Будет извлечена высота строки, содержащей указанный диапазон.</span><span class="sxs-lookup"><span data-stu-id="1199e-109">The height of the row that contains the specified band will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1199e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1199e-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1199e-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="1199e-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1199e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1199e-112">Return value</span></span>

<span data-ttu-id="1199e-113">Возвращает значение типа **uint** , представляющее высоту строки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1199e-113">Returns a **UINT** value that represents the row height, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="1199e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1199e-114">Remarks</span></span>

<span data-ttu-id="1199e-115">Чтобы получить количество строк в элементе управления "Главная панель", используйте [**сообщение \_ RB**](rb-getrowcount.md) .</span><span class="sxs-lookup"><span data-stu-id="1199e-115">To retrieve the number of rows in a rebar control, use the [**RB\_GETROWCOUNT**](rb-getrowcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1199e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="1199e-116">Requirements</span></span>



| <span data-ttu-id="1199e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="1199e-117">Requirement</span></span> | <span data-ttu-id="1199e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="1199e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1199e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1199e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1199e-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1199e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1199e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1199e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1199e-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1199e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1199e-123">Header</span><span class="sxs-lookup"><span data-stu-id="1199e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1199e-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1199e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





