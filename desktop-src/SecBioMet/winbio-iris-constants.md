---
title: Константы WINBIO_IRIS (Винбио \_ types. h)
description: Укажите типы для распознавания IRI.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491382"
---
# <a name="winbio_iris-constants"></a><span data-ttu-id="e2d3c-103">\_Константы IRI винбио</span><span class="sxs-lookup"><span data-stu-id="e2d3c-103">WINBIO\_IRIS Constants</span></span>

<span data-ttu-id="e2d3c-104">Следующие константы — это значения **\_ \_ ПОДтипа БИОметрической метрики винбио** , которые можно использовать для указания типов для распознавания IRI за пределами ANSI ИнЦитс 379-2004: "формат IRI Image Interchange", который не определяет значения видимости слева и справа:</span><span class="sxs-lookup"><span data-stu-id="e2d3c-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the types for iris recognition beyond ANSI INCITS 379-2004: "Iris Image Interchange Format", which does not define any left/right eye values:</span></span>



| <span data-ttu-id="e2d3c-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="e2d3c-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="e2d3c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="e2d3c-106">Description</span></span>                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <span data-ttu-id="e2d3c-107"><dt> **\_ Неизвестный \_ тип \_ диафрагмы винбио**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e2d3c-107"><dt>**WINBIO\_IRIS\_TYPE\_UNKNOWN** </dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e2d3c-108">Тип диафрагмы неизвестен.</span><span class="sxs-lookup"><span data-stu-id="e2d3c-108">The iris type is unknown.</span></span> <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <span data-ttu-id="e2d3c-109"><dt> **\_ \_ \_ Винбиоая**</dt> <dt>0xF5а</dt> IRI</span><span class="sxs-lookup"><span data-stu-id="e2d3c-109"><dt>**WINBIO\_IRIS\_LEFT\_EYE** </dt> <dt>0xF5 </dt></span></span> </dl>                               | <span data-ttu-id="e2d3c-110">Тип IRI является левым глазом.</span><span class="sxs-lookup"><span data-stu-id="e2d3c-110">The iris type is the left eye.</span></span> <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <span data-ttu-id="e2d3c-111"><dt> **\_ \_ \_ Винбиоая**</dt> <dt>0xF6а</dt> IRI</span><span class="sxs-lookup"><span data-stu-id="e2d3c-111"><dt>**WINBIO\_IRIS\_RIGHT\_EYE** </dt> <dt>0xF6 </dt></span></span> </dl>                            | <span data-ttu-id="e2d3c-112">Тип IRI является верным глазом.</span><span class="sxs-lookup"><span data-stu-id="e2d3c-112">The iris type is the right eye.</span></span> <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <span data-ttu-id="e2d3c-113"><dt>**Винбио \_ IRI \_ НЕуказанная \_ POS \_ 01**</dt> <dt>0xF7</dt></span><span class="sxs-lookup"><span data-stu-id="e2d3c-113"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_01**</dt> <dt>0xF7</dt></span></span> </dl>    | <span data-ttu-id="e2d3c-114">Подтип, связанный с первым шаблоном пользователя, если только один глаз является кадром камеры и не может быть определен, является ли он пользовательским.</span><span class="sxs-lookup"><span data-stu-id="e2d3c-114">Subtype associated with a user s first template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <span data-ttu-id="e2d3c-115"><dt> **Винбиоая IRI, не \_ \_ указанная \_ POS \_ 02**</dt> <dt>0xf8</dt></span><span class="sxs-lookup"><span data-stu-id="e2d3c-115"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_02** </dt> <dt>0xF8</dt></span></span> </dl> | <span data-ttu-id="e2d3c-116">Подтип, связанный с вторым шаблоном пользователя, когда только один глаз является кадром камеры, и не может быть определен, является ли он продолжением пользователя или вправо.</span><span class="sxs-lookup"><span data-stu-id="e2d3c-116">Subtype associated with a user s second template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <span data-ttu-id="e2d3c-117"><dt> **Винбиоая \_ диафрагма \_ \_**</dt> <dt>0xF9</dt></span><span class="sxs-lookup"><span data-stu-id="e2d3c-117"><dt>**WINBIO\_IRIS\_BOTH\_EYES** </dt> <dt>0xF9</dt></span></span> </dl>                             | <span data-ttu-id="e2d3c-118">Тип IRI — это оба глаза.</span><span class="sxs-lookup"><span data-stu-id="e2d3c-118">The iris type is both eyes.</span></span> <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <span data-ttu-id="e2d3c-119"><dt> **Винбио \_ \_ \_ диафрагмы**</dt> <dt>0xFA</dt></span><span class="sxs-lookup"><span data-stu-id="e2d3c-119"><dt>**WINBIO\_IRIS\_EITHER\_EYE** </dt> <dt>0xFA</dt></span></span> </dl>                          | <span data-ttu-id="e2d3c-120">Тип диафрагмы — это либо глаз.</span><span class="sxs-lookup"><span data-stu-id="e2d3c-120">The iris type is either eye.</span></span> <br/>                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="e2d3c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e2d3c-121">Requirements</span></span>



| <span data-ttu-id="e2d3c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e2d3c-122">Requirement</span></span> | <span data-ttu-id="e2d3c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e2d3c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d3c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2d3c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2d3c-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e2d3c-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e2d3c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2d3c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2d3c-127">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e2d3c-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e2d3c-128">Header</span><span class="sxs-lookup"><span data-stu-id="e2d3c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2d3c-129"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d3c-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





