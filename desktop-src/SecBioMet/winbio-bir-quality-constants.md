---
title: Константы WINBIO_BIR_QUALITY (Винбио \_ types. h)
description: Укажите относительное качество биометрических данных в Бир, если не указано целочисленное значение от 0 до 100.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137574"
---
# <a name="winbio_bir_quality-constants"></a><span data-ttu-id="cd55a-103">\_ \_ Константы качества винбио Бир</span><span class="sxs-lookup"><span data-stu-id="cd55a-103">WINBIO\_BIR\_QUALITY Constants</span></span>

<span data-ttu-id="cd55a-104">Следующие флаги используются элементом **Quality** структуры [**\_ \_ заголовка винбио Бир**](winbio-bir-header.md) для указания относительного качества биометрических данных в Бир, если не указано целочисленное значение от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="cd55a-104">The following flags are used by the **DataQuality** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the relative quality of biometric data in the BIR if an integer value from 0 to 100 has not been specified.</span></span>



| <span data-ttu-id="cd55a-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="cd55a-105">Constant/value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="cd55a-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cd55a-106">Description</span></span>                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="cd55a-107"><dt>**Винбио \_ \_Качество данных \_ не \_ задано**</dt> <dt> 1</dt></span><span class="sxs-lookup"><span data-stu-id="cd55a-107"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt> 1</dt></span></span> </dl>                   | <span data-ttu-id="cd55a-108">Измерения качества поддерживаются создателем Бир, но в Бир не задано значение.</span><span class="sxs-lookup"><span data-stu-id="cd55a-108">Quality measurements are supported by the BIR creator, but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="cd55a-109"><dt>**Винбио \_ \_Качество данных \_ не \_ поддерживается**</dt> <dt> 2</dt></span><span class="sxs-lookup"><span data-stu-id="cd55a-109"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt> 2</dt></span></span> </dl> | <span data-ttu-id="cd55a-110">Измерения качества не поддерживаются создателем Бир.</span><span class="sxs-lookup"><span data-stu-id="cd55a-110">Quality measurements are not supported by the BIR creator.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="cd55a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="cd55a-111">Requirements</span></span>



| <span data-ttu-id="cd55a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="cd55a-112">Requirement</span></span> | <span data-ttu-id="cd55a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cd55a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd55a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd55a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cd55a-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cd55a-115">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="cd55a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd55a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cd55a-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd55a-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="cd55a-118">Header</span><span class="sxs-lookup"><span data-stu-id="cd55a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd55a-119"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd55a-119"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd55a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd55a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd55a-121">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="cd55a-121">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





