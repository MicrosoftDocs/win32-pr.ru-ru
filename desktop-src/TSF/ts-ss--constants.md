---
title: Константы TS_SS_ (Текстстор. h)
description: '\_ \_ Константы TS SS \, определенные до времени выполнения в \_ структуре состояния служб терминалов, описывают статические состояния документов.'
ms.assetid: 17264527-946a-4648-a4eb-30db751602ab
topic_type:
- apiref
api_name:
- TS_SS_DISJOINTSEL
- TS_SS_REGIONS
- TS_SS_TRANSITORY
- TS_SS_NOHIDDENTEXT
- TS_SS_TKBAUTOCORRECTENABLE
- TS_SS_TKBPREDICTIONENABLE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773645b8a75b7e8eeafa40ed9fa95067743628d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681771"
---
# <a name="ts_ss_-constants"></a><span data-ttu-id="7490d-103">\_ \_ \* Константы TS SS</span><span class="sxs-lookup"><span data-stu-id="7490d-103">TS\_SS\_\* Constants</span></span>

<span data-ttu-id="7490d-104">\_ \_ \* Константы TS SS, определенные до времени выполнения в структуре [**\_ состояния служб терминалов**](/windows/desktop/api/Textstor/ns-textstor-ts_status) , описывают статические состояния документов.</span><span class="sxs-lookup"><span data-stu-id="7490d-104">The TS\_SS\_\* constants, defined before run time in the [**TS\_STATUS**](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure, describe static document states.</span></span>



| <span data-ttu-id="7490d-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="7490d-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="7490d-106">Описание</span><span class="sxs-lookup"><span data-stu-id="7490d-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TS_SS_DISJOINTSEL"></span><span id="ts_ss_disjointsel"></span><dl> <span data-ttu-id="7490d-107"><dt>**TS \_ СС \_ дисжоинтсел**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-107"><dt>**TS\_SS\_DISJOINTSEL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                             | <span data-ttu-id="7490d-108">Документ поддерживает несколько вариантов выбора.</span><span class="sxs-lookup"><span data-stu-id="7490d-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TS_SS_REGIONS"></span><span id="ts_ss_regions"></span><dl> <span data-ttu-id="7490d-109"><dt>**TS \_ \_Регионы SS**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-109"><dt>**TS\_SS\_REGIONS**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                         | <span data-ttu-id="7490d-110">Документ может содержать несколько регионов.</span><span class="sxs-lookup"><span data-stu-id="7490d-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TS_SS_TRANSITORY"></span><span id="ts_ss_transitory"></span><dl> <span data-ttu-id="7490d-111"><dt>**TS \_ \_Транзитный СС**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-111"><dt>**TS\_SS\_TRANSITORY**</dt> <dt>( 0x4 )</dt></span></span> </dl>                                | <span data-ttu-id="7490d-112">Предполагается, что документ будет иметь короткий цикл использования.</span><span class="sxs-lookup"><span data-stu-id="7490d-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TS_SS_NOHIDDENTEXT"></span><span id="ts_ss_nohiddentext"></span><dl> <span data-ttu-id="7490d-113"><dt>**TS \_ СС \_ нохиддентекст**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-113"><dt>**TS\_SS\_NOHIDDENTEXT**</dt> <dt>( 0x8 )</dt></span></span> </dl>                          | <span data-ttu-id="7490d-114">Документ никогда не будет содержать скрытый текст.</span><span class="sxs-lookup"><span data-stu-id="7490d-114">The document will never contain hidden text.</span></span><br/>                                                        |
| <span id="TS_SS_TKBAUTOCORRECTENABLE"></span><span id="ts_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="7490d-115"><dt>**TS \_ СС \_ ткбаутокорректенабле**</dt> <dt>(0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-115"><dt>**TS\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( 0x10 )</dt></span></span> </dl> | <span data-ttu-id="7490d-116">**Начиная с Windows 8:** Документ поддерживает автозамену, предоставляемую сенсорной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="7490d-116">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TS_SS_TKBPREDICTIONENABLE"></span><span id="ts_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="7490d-117"><dt>**TS \_ СС \_ ткбпредиктионенабле**</dt> <dt>(0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-117"><dt>**TS\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( 0x20 )</dt></span></span> </dl>    | <span data-ttu-id="7490d-118">**Начиная с Windows 8:** Документ поддерживает текстовые предложения, предоставляемые сенсорной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="7490d-118">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7490d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7490d-119">Remarks</span></span>

<span data-ttu-id="7490d-120">Элемент **двстатикфлагс** структуры **\_ состояния служб терминалов** использует эти константы.</span><span class="sxs-lookup"><span data-stu-id="7490d-120">The **dwStaticFlags** member of the **TS\_STATUS** structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="7490d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="7490d-121">Requirements</span></span>



| <span data-ttu-id="7490d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="7490d-122">Requirement</span></span> | <span data-ttu-id="7490d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="7490d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7490d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7490d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7490d-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7490d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7490d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7490d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7490d-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7490d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7490d-128">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="7490d-128">Redistributable</span></span><br/>          | <span data-ttu-id="7490d-129">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="7490d-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="7490d-130">Header</span><span class="sxs-lookup"><span data-stu-id="7490d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7490d-131"><dt>Текстстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-131"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="7490d-132">IDL</span><span class="sxs-lookup"><span data-stu-id="7490d-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7490d-133"><dt>Текстстор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7490d-133"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7490d-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7490d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7490d-135">**\_состояние TS**</span><span class="sxs-lookup"><span data-stu-id="7490d-135">**TS\_STATUS**</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

<span data-ttu-id="7490d-136">[**TF \_ status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7490d-136">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

