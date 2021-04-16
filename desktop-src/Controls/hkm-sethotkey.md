---
title: Сообщение HKM_SETHOTKEY (Коммктрл. h)
description: Задает сочетание горячих клавиш для элемента управления "горячий ключ".
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Элементы управления Windows для HKM_SETHOTKEY сообщений
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534037"
---
# <a name="hkm_sethotkey-message"></a><span data-ttu-id="78e29-104">\_Сообщение ХКМ сесоткэй</span><span class="sxs-lookup"><span data-stu-id="78e29-104">HKM\_SETHOTKEY message</span></span>

<span data-ttu-id="78e29-105">Задает сочетание горячих клавиш для элемента управления "горячий ключ".</span><span class="sxs-lookup"><span data-stu-id="78e29-105">Sets the hot key combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="78e29-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="78e29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78e29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="78e29-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78e29-108">[**Лобите**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это виртуальный код клавиши для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="78e29-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="78e29-109">[**Хибите**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) **ловорд** — это модификатор ключа, который указывает ключи, определяющие сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="78e29-109">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that indicates the keys that define a hot key combination.</span></span> <span data-ttu-id="78e29-110">Список значений флагов модификаторов см. в описании сообщения ХКМ- [**\_ горячих клавиш**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="78e29-110">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="78e29-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78e29-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78e29-112">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="78e29-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78e29-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78e29-113">Return value</span></span>

<span data-ttu-id="78e29-114">Всегда возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="78e29-114">Always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="78e29-115">Требования</span><span class="sxs-lookup"><span data-stu-id="78e29-115">Requirements</span></span>



| <span data-ttu-id="78e29-116">Требование</span><span class="sxs-lookup"><span data-stu-id="78e29-116">Requirement</span></span> | <span data-ttu-id="78e29-117">Значение</span><span class="sxs-lookup"><span data-stu-id="78e29-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78e29-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78e29-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78e29-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78e29-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78e29-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78e29-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78e29-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="78e29-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78e29-122">Header</span><span class="sxs-lookup"><span data-stu-id="78e29-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78e29-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="78e29-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

