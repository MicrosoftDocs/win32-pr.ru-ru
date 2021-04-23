---
title: Сообщение ACM_ISPLAYING (Коммктрл. h)
description: Проверяет, воспроизводится ли ролик с чередованием Audio-Video (AVI). Это сообщение можно отправить явно или использовать \_ макрос анимации.
ms.assetid: ebb0c92a-99d2-49c1-9de1-8bdbd032be3a
keywords:
- Элементы управления Windows для ACM_ISPLAYING сообщений
topic_type:
- apiref
api_name:
- ACM_ISPLAYING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f663872ce02b9520e3e033cb5bc5a3da12bb3c3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071333"
---
# <a name="acm_isplaying-message"></a><span data-ttu-id="ca36c-105">ACM \_ воспроизведение сообщения</span><span class="sxs-lookup"><span data-stu-id="ca36c-105">ACM\_ISPLAYING message</span></span>

<span data-ttu-id="ca36c-106">Проверяет, воспроизводится ли ролик с чередованием Audio-Video (AVI).</span><span class="sxs-lookup"><span data-stu-id="ca36c-106">Checks whether an Audio-Video Interleaved (AVI) clip is playing.</span></span> <span data-ttu-id="ca36c-107">Это сообщение можно отправить явно или использовать макрос [**анимации. \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying)</span><span class="sxs-lookup"><span data-stu-id="ca36c-107">You can send this message explicitly or use the [**Animate\_IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca36c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca36c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca36c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca36c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca36c-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ca36c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ca36c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca36c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca36c-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ca36c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca36c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca36c-113">Return value</span></span>

<span data-ttu-id="ca36c-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ca36c-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca36c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ca36c-115">Requirements</span></span>



| <span data-ttu-id="ca36c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ca36c-116">Requirement</span></span> | <span data-ttu-id="ca36c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ca36c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca36c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca36c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ca36c-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca36c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca36c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca36c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ca36c-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca36c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca36c-122">Header</span><span class="sxs-lookup"><span data-stu-id="ca36c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca36c-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca36c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





