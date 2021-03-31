---
title: Сообщение STM_SETICON (Winuser. h)
description: Приложение отправляет \_ сообщение STM сетикон, чтобы связать значок с элементом управления "значок".
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Элементы управления Windows для STM_SETICON сообщений
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071176"
---
# <a name="stm_seticon-message"></a><span data-ttu-id="b1d45-104">\_Сообщение СЕТИКОН STM</span><span class="sxs-lookup"><span data-stu-id="b1d45-104">STM\_SETICON message</span></span>

<span data-ttu-id="b1d45-105">Приложение отправляет сообщение **STM \_ сетикон** , чтобы связать значок с элементом управления "значок".</span><span class="sxs-lookup"><span data-stu-id="b1d45-105">An application sends the **STM\_SETICON** message to associate an icon with an icon control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1d45-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1d45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1d45-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1d45-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1d45-108">Обработчик значка, связываемый с элементом управления "значок".</span><span class="sxs-lookup"><span data-stu-id="b1d45-108">Handle to the icon to associate with the icon control.</span></span>

</dd> <dt>

<span data-ttu-id="b1d45-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1d45-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1d45-110">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b1d45-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1d45-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1d45-111">Return value</span></span>

<span data-ttu-id="b1d45-112">Возвращаемое значение является обработчиком значка, ранее связанного с элементом управления "значок", или нулем в случае возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1d45-112">The return value is a handle to the icon previously associated with the icon control, or zero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d45-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b1d45-113">Requirements</span></span>



| <span data-ttu-id="b1d45-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b1d45-114">Requirement</span></span> | <span data-ttu-id="b1d45-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b1d45-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d45-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1d45-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1d45-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1d45-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b1d45-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1d45-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1d45-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1d45-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1d45-120">Header</span><span class="sxs-lookup"><span data-stu-id="b1d45-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1d45-121"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1d45-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1d45-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1d45-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1d45-123">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b1d45-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1d45-124">**\_значок STM**</span><span class="sxs-lookup"><span data-stu-id="b1d45-124">**STM\_GETICON**</span></span>](stm-geticon.md)
</dt> <dt>

<span data-ttu-id="b1d45-125">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="b1d45-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b1d45-126">**лоадикон**</span><span class="sxs-lookup"><span data-stu-id="b1d45-126">**LoadIcon**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

