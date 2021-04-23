---
title: Сообщение RB_GETBANDBORDERS (Коммктрл. h)
description: Извлекает границы полосы. Результат этого сообщения можно использовать для вычисления области использования в полосе.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- Элементы управления Windows для RB_GETBANDBORDERS сообщений
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521dfecaf5e2573b30f606b7b4d7ecdec9bd896d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988987"
---
# <a name="rb_getbandborders-message"></a><span data-ttu-id="5737c-105">\_Сообщение ЖЕТБАНДБОРДЕРС RB</span><span class="sxs-lookup"><span data-stu-id="5737c-105">RB\_GETBANDBORDERS message</span></span>

<span data-ttu-id="5737c-106">Извлекает границы полосы.</span><span class="sxs-lookup"><span data-stu-id="5737c-106">Retrieves the borders of a band.</span></span> <span data-ttu-id="5737c-107">Результат этого сообщения можно использовать для вычисления области использования в полосе.</span><span class="sxs-lookup"><span data-stu-id="5737c-107">The result of this message can be used to calculate the usable area in a band.</span></span>

## <a name="parameters"></a><span data-ttu-id="5737c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5737c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5737c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5737c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5737c-110">Отсчитываемый от нуля индекс диапазона, для которого будут извлечены границы.</span><span class="sxs-lookup"><span data-stu-id="5737c-110">Zero-based index of the band for which the borders will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5737c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5737c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5737c-112">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать границы полосы.</span><span class="sxs-lookup"><span data-stu-id="5737c-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the band borders.</span></span> <span data-ttu-id="5737c-113">Если элемент управления "Главная панель" имеет стиль [**\_ бандбордерс RBS**](rebar-control-styles.md) , каждый элемент этой структуры будет принимать количество пикселей на соответствующей стороне полосы, составляющую границу.</span><span class="sxs-lookup"><span data-stu-id="5737c-113">If the rebar control has the [**RBS\_BANDBORDERS**](rebar-control-styles.md) style, each member of this structure will receive the number of pixels, on the corresponding side of the band, that constitute the border.</span></span> <span data-ttu-id="5737c-114">Если элемент управления "Главная панель" не имеет стиля **RBS \_ бандбордерс** , только **левый** член этой структуры получает действительную информацию.</span><span class="sxs-lookup"><span data-stu-id="5737c-114">If the rebar control does not have the **RBS\_BANDBORDERS** style, only the **left** member of this structure receives valid information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5737c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5737c-115">Return value</span></span>

<span data-ttu-id="5737c-116">Возвращаемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="5737c-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5737c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5737c-117">Requirements</span></span>



| <span data-ttu-id="5737c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5737c-118">Requirement</span></span> | <span data-ttu-id="5737c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5737c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5737c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5737c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5737c-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5737c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5737c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5737c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5737c-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5737c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5737c-124">Header</span><span class="sxs-lookup"><span data-stu-id="5737c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5737c-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5737c-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

