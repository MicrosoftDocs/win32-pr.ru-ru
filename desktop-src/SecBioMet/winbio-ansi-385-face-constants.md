---
title: Константы WINBIO_ANSI_385_FACE (Винбио \_ types. h)
description: Укажите типы изображений лицевой стороны для распознавания лиц.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137054"
---
# <a name="winbio_ansi_385_face-constants"></a><span data-ttu-id="5ca13-103">\_ \_ Константы винбио ANSI 385 \_</span><span class="sxs-lookup"><span data-stu-id="5ca13-103">WINBIO\_ANSI\_385\_FACE Constants</span></span>

<span data-ttu-id="5ca13-104">Следующие константы являются **значениями \_ \_ ПОДтипа БИОметрической метрики винбио** , которые можно использовать для указания двух типов изображений переднего плана, как определено в ANSI ИнЦитс 385-2004: "формат распознавания лиц для обмена данными": полное разрешение и низкое разрешение.</span><span class="sxs-lookup"><span data-stu-id="5ca13-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the two types of frontal face images as defined by ANSI INCITS 385-2004: "Face Recognition Format for Data Interchange": full resolution and low resolution.</span></span> <span data-ttu-id="5ca13-105">На практике биометрическая платформа будет использовать только образы с полным разрешением для распознавания лиц.</span><span class="sxs-lookup"><span data-stu-id="5ca13-105">In practice, the biometric framework will use only full resolution images for facial recognition.</span></span>



| <span data-ttu-id="5ca13-106">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="5ca13-106">Constant/value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="5ca13-107">Описание</span><span class="sxs-lookup"><span data-stu-id="5ca13-107">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <span data-ttu-id="5ca13-108"><dt>**Винбио \_ \_Неизвестный \_ \_ тип шрифта \_ ANSI 385**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5ca13-108"><dt>**WINBIO\_ANSI\_385\_FACE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="5ca13-109">Тип изображения лицевой стороны неизвестен.</span><span class="sxs-lookup"><span data-stu-id="5ca13-109">The frontal face image type is unknown.</span></span><br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <span data-ttu-id="5ca13-110"><dt>**Винбио \_ \_Интерфейс ANSI 385 \_ лицевой стороной, \_ \_ полный**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5ca13-110"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_FULL**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="5ca13-111">Тип образа лицевой стороны — полное разрешение.</span><span class="sxs-lookup"><span data-stu-id="5ca13-111">The frontal face image type is full resolution.</span></span><br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <span data-ttu-id="5ca13-112"><dt>**Винбио \_ \_ \_ Лицевой \_ \_ маркер 2 ANSI 385**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5ca13-112"><dt>**WINBIO\_ANSI\_385\_FACE\_FRONTAL\_TOKEN**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="5ca13-113">Тип изображения лицевой стороны имеет низкую разрешающую способность.</span><span class="sxs-lookup"><span data-stu-id="5ca13-113">The frontal face image type is low resolution.</span></span><br/>  |



## <a name="requirements"></a><span data-ttu-id="5ca13-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5ca13-114">Requirements</span></span>



| <span data-ttu-id="5ca13-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5ca13-115">Requirement</span></span> | <span data-ttu-id="5ca13-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5ca13-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca13-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ca13-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca13-118">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5ca13-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5ca13-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ca13-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca13-120">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="5ca13-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5ca13-121">Header</span><span class="sxs-lookup"><span data-stu-id="5ca13-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca13-122"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ca13-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





