---
title: Константы TS_SHIFT_ (Текстстор. h)
description: В \_ \_ интерфейсе ианчор для манипуляции скрытым текстом и подсчетом символов используются константы TS Shift \.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415569"
---
# <a name="ts_shift_-constants"></a><span data-ttu-id="6d00a-103">\_Константы сдвига служб терминалов \_ \*</span><span class="sxs-lookup"><span data-stu-id="6d00a-103">TS\_SHIFT\_\* Constants</span></span>

<span data-ttu-id="6d00a-104">\_Константы сдвига TS \_ \* используются интерфейсом **ианчор** для обработки скрытого текста и подсчета символов.</span><span class="sxs-lookup"><span data-stu-id="6d00a-104">The TS\_Shift\_\* constants are used by the **IAnchor** interface for manipulation of hidden text and character counting.</span></span>



| <span data-ttu-id="6d00a-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="6d00a-105">Constant/value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="6d00a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6d00a-106">Description</span></span>                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <span data-ttu-id="6d00a-107"><dt>**TS \_ Счетчик СДВИГов \_ \_ скрыт**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="6d00a-107"><dt>**TS\_SHIFT\_COUNT\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="6d00a-108">Указывает, что привязка будет перемещена на следующую границу области, включая границу скрытой области текста.</span><span class="sxs-lookup"><span data-stu-id="6d00a-108">Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region.</span></span> <span data-ttu-id="6d00a-109">Если не задано, привязка будет смещена после любого соседнего скрытого текста, пока не будет найдена область видимого текста.</span><span class="sxs-lookup"><span data-stu-id="6d00a-109">If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.</span></span><br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <span data-ttu-id="6d00a-110"><dt>**TS \_ SHIFT \_ Остановка \_ скрытия**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="6d00a-110"><dt>**TS\_SHIFT\_HALT\_HIDDEN**</dt> <dt>( 0x2 )</dt></span></span> </dl>    | <span data-ttu-id="6d00a-111">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6d00a-111">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <span data-ttu-id="6d00a-112"><dt>**TS \_ СДВИГ \_ остановлен \_ видимым**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="6d00a-112"><dt>**TS\_SHIFT\_HALT\_VISIBLE**</dt> <dt>( 0x4 )</dt></span></span> </dl> | <span data-ttu-id="6d00a-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6d00a-113">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <span data-ttu-id="6d00a-114"><dt>**TS \_ \_ \_ Только количество сдвигов**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="6d00a-114"><dt>**TS\_SHIFT\_COUNT\_ONLY**</dt> <dt>( 0x8 )</dt></span></span> </dl>       | <span data-ttu-id="6d00a-115">Привязка не смещается.</span><span class="sxs-lookup"><span data-stu-id="6d00a-115">The anchor is not shifted.</span></span><br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="6d00a-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6d00a-116">Requirements</span></span>



| <span data-ttu-id="6d00a-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6d00a-117">Requirement</span></span> | <span data-ttu-id="6d00a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6d00a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d00a-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d00a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d00a-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d00a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d00a-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d00a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d00a-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d00a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d00a-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6d00a-123">Redistributable</span></span><br/>          | <span data-ttu-id="6d00a-124">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="6d00a-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="6d00a-125">Header</span><span class="sxs-lookup"><span data-stu-id="6d00a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d00a-126"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d00a-126"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d00a-127">IDL</span><span class="sxs-lookup"><span data-stu-id="6d00a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d00a-128"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d00a-128"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d00a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d00a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d00a-130">Ианчор:: Шифтрегион</span><span class="sxs-lookup"><span data-stu-id="6d00a-130">IAnchor::ShiftRegion</span></span>](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





