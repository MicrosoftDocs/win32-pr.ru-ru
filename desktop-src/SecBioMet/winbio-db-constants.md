---
title: Константы WINBIO_DB (Винбио \_ types. h)
description: Укажите базу данных, которая будет использоваться в системном пуле.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136358"
---
# <a name="winbio_db-constants"></a><span data-ttu-id="6ab55-103">\_Константы винбио DB</span><span class="sxs-lookup"><span data-stu-id="6ab55-103">WINBIO\_DB Constants</span></span>

<span data-ttu-id="6ab55-104">При вызове [**винбиупенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) можно использовать следующие константы для указания базы данных, которая будет использоваться в системном пуле.</span><span class="sxs-lookup"><span data-stu-id="6ab55-104">The following constants can be used when calling [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to specify the database to be used for a system pool.</span></span>



| <span data-ttu-id="6ab55-105">Константа</span><span class="sxs-lookup"><span data-stu-id="6ab55-105">Constant</span></span>                                                                                                                                                                         | <span data-ttu-id="6ab55-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6ab55-106">Description</span></span>                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <span data-ttu-id="6ab55-107"><dt>**ВИНБИО \_ DB \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="6ab55-107"><dt>**WINBIO\_DB\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="6ab55-108">Каждая биометрическая единица в пуле датчиков использует базу данных по умолчанию, указанную в конфигурации биометрического модуля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ab55-108">Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration.</span></span><br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <span data-ttu-id="6ab55-109"><dt>**\_начальная загрузка базы данных винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ab55-109"><dt>**WINBIO\_DB\_BOOTSTRAP**</dt></span></span> </dl> | <span data-ttu-id="6ab55-110">Может использоваться для сценариев перед запуском Windows.</span><span class="sxs-lookup"><span data-stu-id="6ab55-110">Can be used for scenarios prior to starting Windows.</span></span> <span data-ttu-id="6ab55-111">Как правило, база данных является частью микросхемы датчика или входит в состав BIOS и может использоваться только для регистрации и удаления шаблона.</span><span class="sxs-lookup"><span data-stu-id="6ab55-111">Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.</span></span><br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <span data-ttu-id="6ab55-112"><dt>**Микросхема ВИНБИО \_ DB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6ab55-112"><dt>**WINBIO\_DB\_ONCHIP**</dt></span></span> </dl>          | <span data-ttu-id="6ab55-113">База данных находится в микросхеме датчика.</span><span class="sxs-lookup"><span data-stu-id="6ab55-113">The database resides on the sensor chip.</span></span><br/>                                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="6ab55-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6ab55-114">Requirements</span></span>



| <span data-ttu-id="6ab55-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6ab55-115">Requirement</span></span> | <span data-ttu-id="6ab55-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6ab55-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab55-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ab55-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab55-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6ab55-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6ab55-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ab55-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab55-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ab55-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6ab55-121">Header</span><span class="sxs-lookup"><span data-stu-id="6ab55-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab55-122"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab55-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ab55-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ab55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab55-124">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="6ab55-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





