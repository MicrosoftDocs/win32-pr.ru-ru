---
title: Константы WINBIO_BIR_DATA_FLAGS (Винбио \_ types. h)
description: Укажите условие для данных.
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416137"
---
# <a name="winbio_bir_data_flags-constants"></a><span data-ttu-id="0a38b-103">\_ \_ \_ Константы флагов данных винбио Бир</span><span class="sxs-lookup"><span data-stu-id="0a38b-103">WINBIO\_BIR\_DATA\_FLAGS Constants</span></span>

<span data-ttu-id="0a38b-104">Следующие константы используются элементом " **Флаги** данных" в структуре [**заголовка винбио \_ Бир \_**](winbio-bir-header.md) .</span><span class="sxs-lookup"><span data-stu-id="0a38b-104">The following constants are used by the **DataFlags** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="0a38b-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="0a38b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="0a38b-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0a38b-106">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="0a38b-107"><dt>**Винбио \_ \_ \_ Конфиденциальность флагов данных**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-107"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>0x02</dt></span></span> </dl>                                       | <span data-ttu-id="0a38b-108">Данные зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="0a38b-108">The data is encrypted.</span></span><br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="0a38b-109"><dt>**Винбио \_ \_ \_ Целостность ФЛАГов данных**</dt> — <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-109"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>0x01</dt></span></span> </dl>                                 | <span data-ttu-id="0a38b-110">Данные имеют цифровую подпись или защищаются с помощью кода проверки подлинности сообщений (MAC).</span><span class="sxs-lookup"><span data-stu-id="0a38b-110">The data is digitally signed or is protected by a message authentication code (MAC).</span></span><br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="0a38b-111"><dt>**Винбио \_ Флаг данных, \_ \_ подписанный**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-111"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>0x04</dt></span></span> </dl>                                          | <span data-ttu-id="0a38b-112">Если установлен этот флаг и **флаг \_ \_ \_ целостности флага данных винбио** , данные подписываются.</span><span class="sxs-lookup"><span data-stu-id="0a38b-112">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="0a38b-113">Если этот флаг не установлен, но установлен **флаг \_ \_ \_ целостности флага данных винбио** , то для данных будет рассчитан Mac.</span><span class="sxs-lookup"><span data-stu-id="0a38b-113">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed on the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="0a38b-114"><dt>**Винбио \_ \_ \_ Необработанный флаг данных**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-114"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>0x20</dt></span></span> </dl>                                                   | <span data-ttu-id="0a38b-115">Данные имеют формат, с которым они были захвачены.</span><span class="sxs-lookup"><span data-stu-id="0a38b-115">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="0a38b-116"><dt>**Винбио \_ \_Флаг данных \_ промежуточный**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-116"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>0x40</dt></span></span> </dl>                        | <span data-ttu-id="0a38b-117">Данные не являются необработанными, но обработаны не полностью.</span><span class="sxs-lookup"><span data-stu-id="0a38b-117">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="0a38b-118"><dt>**Винбио \_ \_ \_ Обработанный флаг данных**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-118"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>0x80</dt></span></span> </dl>                                 | <span data-ttu-id="0a38b-119">Данные обработаны.</span><span class="sxs-lookup"><span data-stu-id="0a38b-119">The data has been processed.</span></span><br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="0a38b-120"><dt>**Винбио \_ \_Маска параметра флага данных \_ \_ \_ представляет**</dt> собой <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-120"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="0a38b-121">Маска флага.</span><span class="sxs-lookup"><span data-stu-id="0a38b-121">The flag mask.</span></span> <span data-ttu-id="0a38b-122">Это значение всегда равно единице (1).</span><span class="sxs-lookup"><span data-stu-id="0a38b-122">This value is always one (1).</span></span><br/>                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="0a38b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0a38b-123">Requirements</span></span>



| <span data-ttu-id="0a38b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0a38b-124">Requirement</span></span> | <span data-ttu-id="0a38b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0a38b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a38b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a38b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0a38b-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0a38b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="0a38b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a38b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0a38b-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a38b-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0a38b-130">Header</span><span class="sxs-lookup"><span data-stu-id="0a38b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a38b-131"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a38b-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a38b-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a38b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a38b-133">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="0a38b-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





