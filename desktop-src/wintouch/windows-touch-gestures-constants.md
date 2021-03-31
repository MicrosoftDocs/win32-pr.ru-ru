---
title: Константы жестов сенсорного ввода Windows (Winuser. h)
description: В этом разделе перечислены константы, используемые для сенсорных жестов Windows.
ms.assetid: C5C3C533-A781-47EF-8209-2D94A94C9097
topic_type:
- apiref
api_name:
- GESTURECONFIGMAXCOUNT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 02/18/2020
ms.openlocfilehash: be1d8fe9354c7160643dcefb2d35938453ad5b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988700"
---
# <a name="windows-touch-gestures-constants"></a><span data-ttu-id="23890-103">Константы жестов сенсорного ввода Windows</span><span class="sxs-lookup"><span data-stu-id="23890-103">Windows Touch Gestures Constants</span></span>

<span data-ttu-id="23890-104">В этом разделе перечислены константы, используемые для сенсорных жестов Windows.</span><span class="sxs-lookup"><span data-stu-id="23890-104">This section lists the constants used for Windows Touch gestures.</span></span>

<dl> <dt>

<span data-ttu-id="23890-105">**жестуреконфигмакскаунт**</span><span class="sxs-lookup"><span data-stu-id="23890-105">**GESTURECONFIGMAXCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="23890-106">256</span><span class="sxs-lookup"><span data-stu-id="23890-106">256</span></span>
</dt> <dt>

<span data-ttu-id="23890-107">Определяет максимальное число конфигураций жестов, которые можно включать в один вызов [**сетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) или [**жетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig).</span><span class="sxs-lookup"><span data-stu-id="23890-107">Defines the maximum number of gesture configurations that can be included in a single call to [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig) or [**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig).</span></span>

</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23890-108">Требования</span><span class="sxs-lookup"><span data-stu-id="23890-108">Requirements</span></span>

| <span data-ttu-id="23890-109">Требование</span><span class="sxs-lookup"><span data-stu-id="23890-109">Requirement</span></span> | <span data-ttu-id="23890-110">Значение</span><span class="sxs-lookup"><span data-stu-id="23890-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23890-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23890-111">Minimum supported client</span></span><br/> | <span data-ttu-id="23890-112">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="23890-112">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="23890-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23890-113">Minimum supported server</span></span><br/> | <span data-ttu-id="23890-114">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="23890-114">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="23890-115">Header</span><span class="sxs-lookup"><span data-stu-id="23890-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="23890-116"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23890-116"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="23890-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23890-117">See also</span></span>

<span data-ttu-id="23890-118">[**Жетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**сетжестуреконфиг**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [жесты касания Windows](multi-touch-gestures.md)</span><span class="sxs-lookup"><span data-stu-id="23890-118">[**GetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-getgestureconfig), [**SetGestureConfig**](/windows/desktop/api/winuser/nf-winuser-setgestureconfig), [Windows Touch Gestures](multi-touch-gestures.md)</span></span>
