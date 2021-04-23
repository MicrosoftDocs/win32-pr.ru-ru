---
title: Константы IMAPI
description: IMAPI определяет следующие константы.
ms.assetid: 3ae67227-1cee-4e9c-a7fe-228de596030a
topic_type:
- apiref
api_name:
- IMAPI_SECTOR_SIZE
- IMAPI_SECTORS_PER_SECOND_AT_1X_CD
- IMAPI_SECTORS_PER_SECOND_AT_1X_DVD
- IMAPI_SECTORS_PER_SECOND_AT_1X_BD
api_location:
- Imapi2.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb8c6ac1d855509e67ce5e066410f107172d2ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719190"
---
# <a name="imapi-constants"></a><span data-ttu-id="87fb1-103">Константы IMAPI</span><span class="sxs-lookup"><span data-stu-id="87fb1-103">IMAPI Constants</span></span>

<span data-ttu-id="87fb1-104">IMAPI определяет следующие константы.</span><span class="sxs-lookup"><span data-stu-id="87fb1-104">IMAPI defines the following constants.</span></span>



| <span data-ttu-id="87fb1-105">Константа</span><span class="sxs-lookup"><span data-stu-id="87fb1-105">Constant</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="87fb1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="87fb1-106">Description</span></span>                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="IMAPI_SECTOR_SIZE"></span><span id="imapi_sector_size"></span><dl> <span data-ttu-id="87fb1-107"><dt>**\_Размер сектора \_ IMAPI**</dt></span><span class="sxs-lookup"><span data-stu-id="87fb1-107"><dt>**IMAPI\_SECTOR\_SIZE**</dt></span></span> </dl>                                                        | <span data-ttu-id="87fb1-108">Число байтов в секторе.</span><span class="sxs-lookup"><span data-stu-id="87fb1-108">Number of bytes in a sector.</span></span><br/>                                                  |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_CD"></span><span id="imapi_sectors_per_second_at_1x_cd"></span><dl> <span data-ttu-id="87fb1-109"><dt>**\_Секторов IMAPI в \_ \_ секунду \_ на \_ \_ компакт-диске 1x**</dt></span><span class="sxs-lookup"><span data-stu-id="87fb1-109"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_CD**</dt></span></span> </dl>    | <span data-ttu-id="87fb1-110">Базовый уровень скорости, в течение которого компакт-диск вращается в секторах в секунду.</span><span class="sxs-lookup"><span data-stu-id="87fb1-110">Base rate of speed that a CD spins, measured in sectors per second.</span></span><br/>           |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_DVD"></span><span id="imapi_sectors_per_second_at_1x_dvd"></span><dl> <span data-ttu-id="87fb1-111"><dt>**\_Секторов IMAPI в \_ \_ секунду \_ на \_ \_ DVD-диске 1x**</dt></span><span class="sxs-lookup"><span data-stu-id="87fb1-111"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_DVD**</dt></span></span> </dl> | <span data-ttu-id="87fb1-112">Базовый коэффициент скорости, с которой DVD-диск вращается, измеряется в секторах в секунду.</span><span class="sxs-lookup"><span data-stu-id="87fb1-112">Base rate of speed that a DVD spins, measured in sectors per second.</span></span><br/>          |
| <span id="IMAPI_SECTORS_PER_SECOND_AT_1X_BD"></span><span id="imapi_sectors_per_second_at_1x_bd"></span><dl> <span data-ttu-id="87fb1-113"><dt>**\_Секторов IMAPI в \_ \_ секунду \_ в \_ 1x \_ BD**</dt></span><span class="sxs-lookup"><span data-stu-id="87fb1-113"><dt>**IMAPI\_SECTORS\_PER\_SECOND\_AT\_1X\_BD**</dt></span></span> </dl>    | <span data-ttu-id="87fb1-114">Базовый уровень скорости, на который вращается диск Blu-Ray, измеряемый в секторах в секунду.</span><span class="sxs-lookup"><span data-stu-id="87fb1-114">Base rate of speed that a Blu-ray disc spins, measured in sectors per second.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="87fb1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="87fb1-115">Requirements</span></span>



| <span data-ttu-id="87fb1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="87fb1-116">Requirement</span></span> | <span data-ttu-id="87fb1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="87fb1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87fb1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87fb1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="87fb1-119">Windows Vista, Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="87fb1-119">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="87fb1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87fb1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="87fb1-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87fb1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="87fb1-122">IDL</span><span class="sxs-lookup"><span data-stu-id="87fb1-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87fb1-123"><dt>Imapi2. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87fb1-123"><dt>Imapi2.idl</dt></span></span> </dl> |



 

 





