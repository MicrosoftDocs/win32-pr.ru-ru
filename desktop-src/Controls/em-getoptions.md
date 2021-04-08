---
title: Сообщение EM_GETOPTIONS (RichEdit. h)
description: Возвращает широкие параметры элемента управления редактированием.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- Элементы управления Windows для EM_GETOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989008"
---
# <a name="em_getoptions-message"></a><span data-ttu-id="bd12f-104">\_Сообщение о параметре EM</span><span class="sxs-lookup"><span data-stu-id="bd12f-104">EM\_GETOPTIONS message</span></span>

<span data-ttu-id="bd12f-105">Возвращает широкие параметры элемента управления редактированием.</span><span class="sxs-lookup"><span data-stu-id="bd12f-105">Retrieves rich edit control options.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd12f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd12f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd12f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd12f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd12f-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bd12f-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bd12f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd12f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd12f-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="bd12f-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd12f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd12f-111">Return value</span></span>

<span data-ttu-id="bd12f-112">Это сообщение Возвращает сочетание текущих значений флагов параметров, описанных в сообщении [**EM \_ сетоптионс**](em-setoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="bd12f-112">This message returns a combination of the current option flag values described in the [**EM\_SETOPTIONS**](em-setoptions.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd12f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bd12f-113">Requirements</span></span>



| <span data-ttu-id="bd12f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bd12f-114">Requirement</span></span> | <span data-ttu-id="bd12f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bd12f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd12f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd12f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd12f-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd12f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd12f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd12f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd12f-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd12f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd12f-120">Header</span><span class="sxs-lookup"><span data-stu-id="bd12f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd12f-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd12f-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd12f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd12f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd12f-123">**EM \_ сетоптионс**</span><span class="sxs-lookup"><span data-stu-id="bd12f-123">**EM\_SETOPTIONS**</span></span>](em-setoptions.md)
</dt> </dl>

 

 





