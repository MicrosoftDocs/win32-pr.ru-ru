---
title: Константы WINBIO_FLAG (Винбио \_ types. h)
description: Укажите конфигурацию биометрического модуля и характеристики доступа для нового сеанса.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414989"
---
# <a name="winbio_flag-constants"></a><span data-ttu-id="fd187-103">\_Константы флага винбио</span><span class="sxs-lookup"><span data-stu-id="fd187-103">WINBIO\_FLAG Constants</span></span>

<span data-ttu-id="fd187-104">Следующие константы можно использовать в функции [**винбиупенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) для указания конфигурации биометрического модуля и характеристик доступа для нового сеанса.</span><span class="sxs-lookup"><span data-stu-id="fd187-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify biometric unit configuration and access characteristics for the new session.</span></span>



| <span data-ttu-id="fd187-105">Константа</span><span class="sxs-lookup"><span data-stu-id="fd187-105">Constant</span></span>                                                                                                                                                                                     | <span data-ttu-id="fd187-106">Описание</span><span class="sxs-lookup"><span data-stu-id="fd187-106">Description</span></span>                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <span data-ttu-id="fd187-107"><dt>**\_флаг винбио \_ по умолчанию**</dt></span><span class="sxs-lookup"><span data-stu-id="fd187-107"><dt>**WINBIO\_FLAG\_DEFAULT**</dt></span></span> </dl>             | <span data-ttu-id="fd187-108">Флаг конфигурации датчика.</span><span class="sxs-lookup"><span data-stu-id="fd187-108">Sensor configuration flag.</span></span> <span data-ttu-id="fd187-109">Биометрические единицы работают так, как указано во время установки.</span><span class="sxs-lookup"><span data-stu-id="fd187-109">The biometric units operate in the manner specified during installation.</span></span><br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <span data-ttu-id="fd187-110"><dt>**\_базовый флаг \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="fd187-110"><dt>**WINBIO\_FLAG\_BASIC**</dt></span></span> </dl>                   | <span data-ttu-id="fd187-111">Флаг конфигурации датчика.</span><span class="sxs-lookup"><span data-stu-id="fd187-111">Sensor configuration flag.</span></span> <span data-ttu-id="fd187-112">Биометрические единицы работают только как базовые устройства записи.</span><span class="sxs-lookup"><span data-stu-id="fd187-112">The biometric units operate only as basic capture devices.</span></span><br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <span data-ttu-id="fd187-113"><dt>**\_Расширенный флаг \_ винбио**</dt></span><span class="sxs-lookup"><span data-stu-id="fd187-113"><dt>**WINBIO\_FLAG\_ADVANCED**</dt></span></span> </dl>          | <span data-ttu-id="fd187-114">Флаг конфигурации датчика.</span><span class="sxs-lookup"><span data-stu-id="fd187-114">Sensor configuration flag.</span></span> <span data-ttu-id="fd187-115">В биометрических единицах используются внутренние возможности обработки и хранения.</span><span class="sxs-lookup"><span data-stu-id="fd187-115">The biometric units use internal processing and storage capabilities.</span></span><br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <span data-ttu-id="fd187-116"><dt>**\_необработанный флаг винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd187-116"><dt>**WINBIO\_FLAG\_RAW**</dt></span></span> </dl>                         | <span data-ttu-id="fd187-117">Требуемый флаг доступа.</span><span class="sxs-lookup"><span data-stu-id="fd187-117">Desired access flag.</span></span> <span data-ttu-id="fd187-118">Клиентское приложение захватывает необработанные биометрические данные с помощью [**винбиокаптуресампле**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="fd187-118">The client application captures raw biometric data using [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span><br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <span data-ttu-id="fd187-119"><dt>**\_обслуживание флагов винбио \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fd187-119"><dt>**WINBIO\_FLAG\_MAINTENANCE**</dt></span></span> </dl> | <span data-ttu-id="fd187-120">Требуемый флаг доступа.</span><span class="sxs-lookup"><span data-stu-id="fd187-120">Desired access flag.</span></span> <span data-ttu-id="fd187-121">Клиент выполняет определяемые поставщиком операции управления на биометрической единице, вызывая [**винбиоконтролунитпривилежед**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="fd187-121">The client performs vendor-defined control operations on a biometric unit by calling [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fd187-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fd187-122">Requirements</span></span>



| <span data-ttu-id="fd187-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fd187-123">Requirement</span></span> | <span data-ttu-id="fd187-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fd187-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd187-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd187-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fd187-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fd187-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="fd187-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd187-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fd187-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd187-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fd187-129">Header</span><span class="sxs-lookup"><span data-stu-id="fd187-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd187-130"><dt>Винбио \_ types. h (include винбио. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd187-130"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd187-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd187-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd187-132">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="fd187-132">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





