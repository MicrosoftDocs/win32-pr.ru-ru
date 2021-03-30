---
title: Константы WINBIO_PRESENCE_CHANGE (Винбио \_ types. h)
description: Описывает типы изменений, которые могут возникать, когда биометрическая платформа Windows наблюдает за присутствием отдельных пользователей.
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c864c82ddca6faec134716778dc2e795675371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071224"
---
# <a name="winbio_presence_change-constants"></a><span data-ttu-id="8ab9a-103">\_ \_ Константы изменения присутствия винбио</span><span class="sxs-lookup"><span data-stu-id="8ab9a-103">WINBIO\_PRESENCE\_CHANGE Constants</span></span>

<span data-ttu-id="8ab9a-104">Описывает типы изменений, которые могут возникать, когда биометрическая платформа Windows наблюдает за присутствием отдельных пользователей.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-104">Describes the types of changes that can occur when the Windows Biometric Framework monitors the presence of individuals.</span></span>



| <span data-ttu-id="8ab9a-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="8ab9a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="8ab9a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="8ab9a-106">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <span data-ttu-id="8ab9a-107"><dt>**Винбио \_ \_Неизвестный \_ тип \_ изменения присутствия**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9a-107"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>           | <span data-ttu-id="8ab9a-108">Тип события неизвестен.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-108">The type of event is unknown.</span></span> <span data-ttu-id="8ab9a-109">Это значение используется для неинициализированной структуры.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-109">This value is used for the uninitialized structure.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <span data-ttu-id="8ab9a-110"><dt>**Винбио \_ \_ \_ Обновление типа изменения \_ присутствия \_ все**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9a-110"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_UPDATE\_ALL**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="8ab9a-111">Предоставляет сведения обо всех лицах, текущих в кадре камеры.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-111">Provides information about all of the faces current in the camera frame.</span></span><br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <span data-ttu-id="8ab9a-112"><dt>**Винбио \_ \_ \_ \_ Прибытие типа изменения присутствия**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9a-112"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_ARRIVE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="8ab9a-113">Новый элемент, поступил в кадр камеры.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-113">A new face entered the camera frame.</span></span><br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <span data-ttu-id="8ab9a-114"><dt>**Винбио \_ \_Тип изменения присутствия, \_ \_ распознаваемый**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9a-114"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_RECOGNIZE**</dt> <dt>3</dt></span></span> </dl>     | <span data-ttu-id="8ab9a-115">Лицо было сопоставлено с зарегистрированным пользователем.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-115">A face was matched to an enrolled user.</span></span><br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <span data-ttu-id="8ab9a-116"><dt>**Винбио \_ \_Тип изменения \_ присутствия \_ выбывают**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9a-116"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_DEPART**</dt> <dt>4</dt></span></span> </dl>              | <span data-ttu-id="8ab9a-117">Ранее обнаруженная грань была вне рамки камеры в течение определенного периода времени.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-117">A previously detected face has been out of the camera frame for a period of time.</span></span><br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <span data-ttu-id="8ab9a-118"><dt>**Винбио \_ \_Тип изменения \_ присутствия \_ Track**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9a-118"><dt>**WINBIO\_PRESENCE\_CHANGE\_TYPE\_TRACK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="8ab9a-119">Предоставляет сведения об обновлении ограничивающего прямоугольника и отклонения подробных значений для подмножества лиц, которые в данный момент находятся в кадре камеры.</span><span class="sxs-lookup"><span data-stu-id="8ab9a-119">Provides updates information about the bounding box and reject detail values for a subset of the faces that are currently in the camera frame.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8ab9a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8ab9a-120">Requirements</span></span>



| <span data-ttu-id="8ab9a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8ab9a-121">Requirement</span></span> | <span data-ttu-id="8ab9a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8ab9a-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab9a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ab9a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab9a-124">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8ab9a-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="8ab9a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ab9a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab9a-126">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8ab9a-126">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="8ab9a-127">Header</span><span class="sxs-lookup"><span data-stu-id="8ab9a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ab9a-128"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="8ab9a-128"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



 

 





