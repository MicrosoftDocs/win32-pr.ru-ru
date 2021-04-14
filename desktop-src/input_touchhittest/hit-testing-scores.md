---
title: Оценки проверки попадания касания
description: Следующие константы указывают на возможные результаты проверки попадания для объекта относительно других объектов, пересекающих зону касания.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534004"
---
# <a name="touch-hit-testing-scores"></a><span data-ttu-id="a7c53-103">Оценки проверки попадания касания</span><span class="sxs-lookup"><span data-stu-id="a7c53-103">Touch Hit Testing Scores</span></span>

<span data-ttu-id="a7c53-104">Следующие константы указывают на возможные результаты проверки попадания для объекта относительно других объектов, пересекающих зону касания.</span><span class="sxs-lookup"><span data-stu-id="a7c53-104">The following constants identify the possible hit test scores for an object, relative to other objects that intersect the touch contact area.</span></span>

| <span data-ttu-id="a7c53-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="a7c53-105">Constant/value</span></span> | <span data-ttu-id="a7c53-106">Описание</span><span class="sxs-lookup"><span data-stu-id="a7c53-106">Description</span></span> |
|---|---|
| <span data-ttu-id="a7c53-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span><span class="sxs-lookup"><span data-stu-id="a7c53-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span></span>      | <span data-ttu-id="a7c53-108">Объект является наиболее вероятной целью.</span><span class="sxs-lookup"><span data-stu-id="a7c53-108">The object is the most probable target.</span></span><br/>  |
| <span data-ttu-id="a7c53-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xfff</span><span class="sxs-lookup"><span data-stu-id="a7c53-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span></span> | <span data-ttu-id="a7c53-110">Объект является наименее вероятной целью.</span><span class="sxs-lookup"><span data-stu-id="a7c53-110">The object is the least probable target.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="a7c53-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a7c53-111">Requirements</span></span>

| <span data-ttu-id="a7c53-112">Требование</span><span class="sxs-lookup"><span data-stu-id="a7c53-112">Requirement</span></span> | <span data-ttu-id="a7c53-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a7c53-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c53-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7c53-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a7c53-115">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a7c53-115">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a7c53-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7c53-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a7c53-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a7c53-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="a7c53-118">Header</span><span class="sxs-lookup"><span data-stu-id="a7c53-118">Header</span></span><br/>                   | <span data-ttu-id="a7c53-119">Winuser. h</span><span class="sxs-lookup"><span data-stu-id="a7c53-119">Winuser.h</span></span> |
