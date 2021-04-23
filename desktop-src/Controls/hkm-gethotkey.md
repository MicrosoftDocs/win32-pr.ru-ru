---
title: Сообщение HKM_GETHOTKEY (Коммктрл. h)
description: Получает виртуальный код ключа и флаги модификатора для горячего ключа из элемента управления горячего ключа.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Элементы управления Windows для HKM_GETHOTKEY сообщений
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490212"
---
# <a name="hkm_gethotkey-message"></a><span data-ttu-id="a32a9-104">\_Сообщение ХКМ</span><span class="sxs-lookup"><span data-stu-id="a32a9-104">HKM\_GETHOTKEY message</span></span>

<span data-ttu-id="a32a9-105">Получает виртуальный код ключа и флаги модификатора для горячего ключа из элемента управления горячего ключа.</span><span class="sxs-lookup"><span data-stu-id="a32a9-105">Gets the virtual key code and modifier flags of a hot key from a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a32a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a32a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a32a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a32a9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a32a9-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a32a9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a32a9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a32a9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a32a9-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a32a9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a32a9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a32a9-111">Return value</span></span>

<span data-ttu-id="a32a9-112">Возвращает код виртуального ключа и флаги модификатора.</span><span class="sxs-lookup"><span data-stu-id="a32a9-112">Returns the virtual key code and modifier flags.</span></span> <span data-ttu-id="a32a9-113">[**Лобите**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) — это виртуальный код клавиши для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="a32a9-113">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="a32a9-114">[**Хибите**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) **ловорд** — это модификатор ключа, который задает ключи, определяющие сочетание клавиш.</span><span class="sxs-lookup"><span data-stu-id="a32a9-114">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that specifies the keys that define a hot key combination.</span></span> <span data-ttu-id="a32a9-115">Флаги модификатора могут быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a32a9-115">The modifier flags can be a combination of the following values.</span></span>



| <span data-ttu-id="a32a9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a32a9-116">Value</span></span>            | <span data-ttu-id="a32a9-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a32a9-117">Meaning</span></span>      |
|------------------|--------------|
| <span data-ttu-id="a32a9-118">ХОТКЭЙФ \_ ALT</span><span class="sxs-lookup"><span data-stu-id="a32a9-118">HOTKEYF\_ALT</span></span>     | <span data-ttu-id="a32a9-119">ALT - клавиша</span><span class="sxs-lookup"><span data-stu-id="a32a9-119">ALT key</span></span>      |
| <span data-ttu-id="a32a9-120">\_элемент управления хоткэйф</span><span class="sxs-lookup"><span data-stu-id="a32a9-120">HOTKEYF\_CONTROL</span></span> | <span data-ttu-id="a32a9-121">Ключ управления</span><span class="sxs-lookup"><span data-stu-id="a32a9-121">CONTROL key</span></span>  |
| <span data-ttu-id="a32a9-122">ХОТКЭЙФ \_ ext</span><span class="sxs-lookup"><span data-stu-id="a32a9-122">HOTKEYF\_EXT</span></span>     | <span data-ttu-id="a32a9-123">Расширенный ключ</span><span class="sxs-lookup"><span data-stu-id="a32a9-123">Extended key</span></span> |
| <span data-ttu-id="a32a9-124">ХОТКЭЙФ \_ SHIFT</span><span class="sxs-lookup"><span data-stu-id="a32a9-124">HOTKEYF\_SHIFT</span></span>   | <span data-ttu-id="a32a9-125">Клавиша SHIFT</span><span class="sxs-lookup"><span data-stu-id="a32a9-125">SHIFT key</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="a32a9-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a32a9-126">Remarks</span></span>

<span data-ttu-id="a32a9-127">16-разрядное значение, возвращаемое этим сообщением, можно использовать как параметр *wParam* в сообщении [**WM \_ сесоткэй**](/windows/desktop/inputdev/wm-sethotkey) .</span><span class="sxs-lookup"><span data-stu-id="a32a9-127">The 16-bit value returned by this message can be used as the *wParam* parameter in the [**WM\_SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a32a9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a32a9-128">Requirements</span></span>



| <span data-ttu-id="a32a9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a32a9-129">Requirement</span></span> | <span data-ttu-id="a32a9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a32a9-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a32a9-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a32a9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a32a9-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a32a9-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a32a9-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a32a9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a32a9-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a32a9-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a32a9-135">Header</span><span class="sxs-lookup"><span data-stu-id="a32a9-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a32a9-136"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a32a9-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

