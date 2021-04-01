---
title: Константы TF_SS_ (Мсктф. h)
description: '\_ \_ Константы TF SS \, определенные до времени выполнения в \_ структуре состояния TF, описывают статические состояния документов.'
ms.assetid: 371aeeda-f081-4506-ba51-79c6a8bc8768
topic_type:
- apiref
api_name:
- TF_SS_DISJOINTSEL
- TF_SS_REGIONS
- TF_SS_TRANSITORY
- TF_SS_TKBAUTOCORRECTENABLE
- TF_SS_TKBPREDICTIONENABLE
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1028b78e74ed10c572feb904baa8ec395087ee3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071728"
---
# <a name="tf_ss_-constants"></a><span data-ttu-id="c981c-103">\_ \_ \* Константы TF SS</span><span class="sxs-lookup"><span data-stu-id="c981c-103">TF\_SS\_\* Constants</span></span>

<span data-ttu-id="c981c-104">\_ \_ \* Константы TF SS, определенные до времени выполнения в структуре [**\_ состояния TF**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) , описывают статические состояния документов.</span><span class="sxs-lookup"><span data-stu-id="c981c-104">The TF\_SS\_\* constants, defined before run time in the [**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure, describe static document states.</span></span>



| <span data-ttu-id="c981c-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="c981c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="c981c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c981c-106">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TF_SS_DISJOINTSEL"></span><span id="tf_ss_disjointsel"></span><dl> <span data-ttu-id="c981c-107"><dt>**Tf \_ СС \_ дисжоинтсел**</dt> <dt>(TS \_ SS \_ дисжоинтсел)</dt></span><span class="sxs-lookup"><span data-stu-id="c981c-107"><dt>**TF\_SS\_DISJOINTSEL**</dt> <dt>( TS\_SS\_DISJOINTSEL )</dt></span></span> </dl>                                     | <span data-ttu-id="c981c-108">Документ поддерживает несколько вариантов выбора.</span><span class="sxs-lookup"><span data-stu-id="c981c-108">The document supports multiple selections.</span></span><br/>                                                          |
| <span id="TF_SS_REGIONS"></span><span id="tf_ss_regions"></span><dl> <span data-ttu-id="c981c-109"><dt>**Tf \_ \_регионы SS**</dt> <dt>( \_ регионы TS SS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="c981c-109"><dt>**TF\_SS\_REGIONS**</dt> <dt>( TS\_SS\_REGIONS )</dt></span></span> </dl>                                                     | <span data-ttu-id="c981c-110">Документ может содержать несколько регионов.</span><span class="sxs-lookup"><span data-stu-id="c981c-110">The document can contain multiple regions.</span></span><br/>                                                          |
| <span id="TF_SS_TRANSITORY"></span><span id="tf_ss_transitory"></span><dl> <span data-ttu-id="c981c-111"><dt>**Tf \_ \_транзитный СС**</dt> <dt>( \_ \_ транзитный шлюз TS SS)</dt></span><span class="sxs-lookup"><span data-stu-id="c981c-111"><dt>**TF\_SS\_TRANSITORY**</dt> <dt>( TS\_SS\_TRANSITORY )</dt></span></span> </dl>                                         | <span data-ttu-id="c981c-112">Предполагается, что документ будет иметь короткий цикл использования.</span><span class="sxs-lookup"><span data-stu-id="c981c-112">The document is expected to have a short usage cycle.</span></span><br/>                                               |
| <span id="TF_SS_TKBAUTOCORRECTENABLE"></span><span id="tf_ss_tkbautocorrectenable"></span><dl> <span data-ttu-id="c981c-113"><dt>**Tf \_ СС \_ ткбаутокорректенабле**</dt> <dt>(TS \_ SS \_ ткбаутокорректенабле)</dt></span><span class="sxs-lookup"><span data-stu-id="c981c-113"><dt>**TF\_SS\_TKBAUTOCORRECTENABLE**</dt> <dt>( TS\_SS\_TKBAUTOCORRECTENABLE )</dt></span></span> </dl> | <span data-ttu-id="c981c-114">**Начиная с Windows 8:** Документ поддерживает автозамену, предоставляемую сенсорной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="c981c-114">**Starting with Windows 8:** The document supports autocorrection provided by the touch keyboard.</span></span><br/>   |
| <span id="TF_SS_TKBPREDICTIONENABLE"></span><span id="tf_ss_tkbpredictionenable"></span><dl> <span data-ttu-id="c981c-115"><dt>**Tf \_ СС \_ ткбпредиктионенабле**</dt> <dt>(TS \_ SS \_ ткбпредиктионенабле)</dt></span><span class="sxs-lookup"><span data-stu-id="c981c-115"><dt>**TF\_SS\_TKBPREDICTIONENABLE**</dt> <dt>( TS\_SS\_TKBPREDICTIONENABLE )</dt></span></span> </dl>     | <span data-ttu-id="c981c-116">**Начиная с Windows 8:** Документ поддерживает текстовые предложения, предоставляемые сенсорной клавиатурой.</span><span class="sxs-lookup"><span data-stu-id="c981c-116">**Starting with Windows 8:** The document supports text suggestions provided by the touch keyboard.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c981c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c981c-117">Remarks</span></span>

<span data-ttu-id="c981c-118">Элемент **двстатикфлагс** \_ структуры состояния TF использует эти константы.</span><span class="sxs-lookup"><span data-stu-id="c981c-118">The **dwStaticFlags** member of the TF\_STATUS structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="c981c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c981c-119">Requirements</span></span>



| <span data-ttu-id="c981c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c981c-120">Requirement</span></span> | <span data-ttu-id="c981c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c981c-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c981c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c981c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c981c-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c981c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c981c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c981c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c981c-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c981c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c981c-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c981c-126">Redistributable</span></span><br/>          | <span data-ttu-id="c981c-127">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="c981c-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="c981c-128">Header</span><span class="sxs-lookup"><span data-stu-id="c981c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c981c-129"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="c981c-129"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="c981c-130">IDL</span><span class="sxs-lookup"><span data-stu-id="c981c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c981c-131"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c981c-131"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c981c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c981c-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="c981c-133">[**TF \_ status**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c981c-133">[**TF\_STATUS**](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> </dl>

 

