---
description: Флаги в следующей таблице указывают механизмы защиты выходных данных для OUTPUT Protection Manager (ОПМ).
ms.assetid: 484dfea9-301d-4b2b-b5d1-d785ebaa8c8f
title: Флаги типа защиты ОПМ (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc8b30a18f5c7bf68fb01775751aa56e1e619f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711428"
---
# <a name="opm-protection-type-flags"></a><span data-ttu-id="cc479-103">Флаги типа защиты ОПМ</span><span class="sxs-lookup"><span data-stu-id="cc479-103">OPM Protection Type Flags</span></span>

<span data-ttu-id="cc479-104">Флаги в следующей таблице указывают механизмы защиты выходных данных для OUTPUT Protection Manager (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="cc479-104">The flags in the following table specify output protection mechanisms for Output Protection Manager (OPM).</span></span>



| <span data-ttu-id="cc479-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="cc479-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="cc479-106">Описание</span><span class="sxs-lookup"><span data-stu-id="cc479-106">Description</span></span>                                                                                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_PROTECTION_TYPE_OTHER"></span><span id="opm_protection_type_other"></span><dl> <span data-ttu-id="cc479-107"><dt>**ОПМ \_ \_ \_ Другой 0X80000000 тип защиты**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cc479-107"><dt>**OPM\_PROTECTION\_TYPE\_OTHER**</dt> <dt>0x80000000</dt></span></span> </dl>                                                | <span data-ttu-id="cc479-108">Неизвестный механизм защиты.</span><span class="sxs-lookup"><span data-stu-id="cc479-108">Unknown protection mechanism.</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_NONE"></span><span id="opm_protection_type_none"></span><dl> <span data-ttu-id="cc479-109"><dt>**ОПМ \_ Тип защиты — \_ \_ нет**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="cc479-109"><dt>**OPM\_PROTECTION\_TYPE\_NONE**</dt> <dt>0x00000000</dt></span></span> </dl>                                                   | <span data-ttu-id="cc479-110">Нет механизмов защиты.</span><span class="sxs-lookup"><span data-stu-id="cc479-110">No protection mechanisms.</span></span><br/>                                                                                                                                                                                        |
| <span id="OPM_PROTECTION_TYPE_COPP_COMPATIBLE_HDCP"></span><span id="opm_protection_type_copp_compatible_hdcp"></span><dl> <span data-ttu-id="cc479-111"><dt>**ОПМ \_ \_Тип защиты \_ Копп \_ совместимая \_ HDCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cc479-111"><dt>**OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="cc479-112">High-Bandwidth цифровой Защита содержимого (HDCP).</span><span class="sxs-lookup"><span data-stu-id="cc479-112">High-Bandwidth Digital Content Protection (HDCP).</span></span> <span data-ttu-id="cc479-113">Этот флаг используется при эмуляции сертифицированного протокола защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="cc479-113">This flag is used when emulating Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="cc479-114">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="cc479-114">For more information, see Remarks.</span></span> <span data-ttu-id="cc479-115">Этот флаг не поддерживается для семантики ОПМ.</span><span class="sxs-lookup"><span data-stu-id="cc479-115">This flag is not supported for OPM semantics.</span></span><br/> |
| <span id="OPM_PROTECTION_TYPE_ACP"></span><span id="opm_protection_type_acp"></span><dl> <span data-ttu-id="cc479-116"><dt>**ОПМ \_ \_Тип защиты \_ ACP**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="cc479-116"><dt>**OPM\_PROTECTION\_TYPE\_ACP**</dt> <dt>0x00000002</dt></span></span> </dl>                                                      | <span data-ttu-id="cc479-117">Аналоговая защита от копирования (ACP).</span><span class="sxs-lookup"><span data-stu-id="cc479-117">Analog Copy Protection (ACP).</span></span><br/>                                                                                                                                                                                    |
| <span id="OPM_PROTECTION_TYPE_CGMSA"></span><span id="opm_protection_type_cgmsa"></span><dl> <span data-ttu-id="cc479-118"><dt>**ОПМ \_ \_Тип защиты \_ кгмса**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="cc479-118"><dt>**OPM\_PROTECTION\_TYPE\_CGMSA**</dt> <dt>0x00000004</dt></span></span> </dl>                                                | <span data-ttu-id="cc479-119">Система управления поколением копий — аналоговая (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="cc479-119">Copy Generation Management System—Analog (CGMS-A).</span></span><br/>                                                                                                                                                               |
| <span id="OPM_PROTECTION_TYPE_HDCP"></span><span id="opm_protection_type_hdcp"></span><dl> <span data-ttu-id="cc479-120"><dt>**ОПМ \_ \_Тип защиты \_ HDCP**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="cc479-120"><dt>**OPM\_PROTECTION\_TYPE\_HDCP**</dt> <dt>0x00000008</dt></span></span> </dl>                                                   | <span data-ttu-id="cc479-121">Поддерживающ.</span><span class="sxs-lookup"><span data-stu-id="cc479-121">HDCP.</span></span> <span data-ttu-id="cc479-122">Этот флаг используется, если объект ОПМ имеет семантику ОПМ.</span><span class="sxs-lookup"><span data-stu-id="cc479-122">This flag is used when the OPM object has OPM semantics.</span></span> <span data-ttu-id="cc479-123">Она не поддерживается для семантики Копп.</span><span class="sxs-lookup"><span data-stu-id="cc479-123">It is not supported for COPP semantics.</span></span><br/>                                                                                                           |
| <span id="OPM_PROTECTION_TYPE_DPCP"></span><span id="opm_protection_type_dpcp"></span><dl> <span data-ttu-id="cc479-124"><dt>**ОПМ \_ \_Тип защиты \_ ДПКП**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="cc479-124"><dt>**OPM\_PROTECTION\_TYPE\_DPCP**</dt> <dt>0x00000010</dt></span></span> </dl>                                                   | <span data-ttu-id="cc479-125">Дисплайпорт Защита содержимого (ДПКП).</span><span class="sxs-lookup"><span data-stu-id="cc479-125">DisplayPort Content Protection (DPCP).</span></span><br/>                                                                                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="cc479-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc479-126">Remarks</span></span>

<span data-ttu-id="cc479-127">Эти флаги используются в следующих командах ОПМ и запросах о состоянии.</span><span class="sxs-lookup"><span data-stu-id="cc479-127">These flags are used in the following OPM commands and status requests.</span></span>

-   [<span data-ttu-id="cc479-128">ОПМ \_ установить \_ \_ уровень защиты</span><span class="sxs-lookup"><span data-stu-id="cc479-128">OPM\_SET\_PROTECTION\_LEVEL</span></span>](opm-set-protection-level.md)
-   [<span data-ttu-id="cc479-129">ОПМ \_ получить \_ \_ уровень защиты \_ виртуальной системы</span><span class="sxs-lookup"><span data-stu-id="cc479-129">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-virtual-protection-level.md)
-   [<span data-ttu-id="cc479-130">ОПМ \_ получить \_ фактический \_ \_ уровень защиты</span><span class="sxs-lookup"><span data-stu-id="cc479-130">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>](opm-get-actual-protection-level.md)

### <a name="hdcp"></a><span data-ttu-id="cc479-131">ПОДДЕРЖИВАЮЩ</span><span class="sxs-lookup"><span data-stu-id="cc479-131">HDCP</span></span>

<span data-ttu-id="cc479-132">Для HDCP определены следующие два флага.</span><span class="sxs-lookup"><span data-stu-id="cc479-132">The following two flags are defined for HDCP.</span></span>



| <span data-ttu-id="cc479-133">Значение</span><span class="sxs-lookup"><span data-stu-id="cc479-133">Value</span></span>                                         | <span data-ttu-id="cc479-134">Описание</span><span class="sxs-lookup"><span data-stu-id="cc479-134">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc479-135">\_Тип защиты \_ ОПМ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="cc479-135">OPM\_PROTECTION\_TYPE\_HDCP</span></span>                   | <span data-ttu-id="cc479-136">Используйте этот флаг, если указатель [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) был создан с семантикой ОПМ.</span><span class="sxs-lookup"><span data-stu-id="cc479-136">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with OPM semantics.</span></span>                                                                        |
| <span data-ttu-id="cc479-137">\_ \_ совместимый с ОПМ тип защиты \_ Копп \_ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="cc479-137">OPM\_PROTECTION\_TYPE\_COPP\_COMPATIBLE\_HDCP</span></span> | <span data-ttu-id="cc479-138">Используйте этот флаг, если указатель [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) был создан с семантикой Копп.</span><span class="sxs-lookup"><span data-stu-id="cc479-138">Use this flag if the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer was created with COPP semantics.</span></span> <span data-ttu-id="cc479-139">Этот флаг соответствует \_ флагу Копп ProtectionType \_ HDCP в Копп.</span><span class="sxs-lookup"><span data-stu-id="cc479-139">This flag corresponds to the COPP\_ProtectionType\_HDCP flag in COPP.</span></span> |



 

<span data-ttu-id="cc479-140">Оба режима (семантика ОПМ и семантика Копп) поддерживают следующие операции для HDCP:</span><span class="sxs-lookup"><span data-stu-id="cc479-140">Both modes (OPM semantics and COPP semantics) support the following operations for HDCP:</span></span>

-   <span data-ttu-id="cc479-141">Включите или отключите HDCP с помощью команды [ОПМ \_ Set \_ Protection \_ Level](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="cc479-141">Enable or disable HDCP by using the [OPM\_SET\_PROTECTION\_LEVEL](opm-set-protection-level.md) command.</span></span>
-   <span data-ttu-id="cc479-142">Запросите, включена ли защита HDCP с помощью [ОПМ \_ Получение \_ виртуальной \_ защиты \_ ](opm-get-virtual-protection-level.md) или [ОПМ \_ Получение \_ фактического состояния \_ \_ уровня защиты](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="cc479-142">Query whether HDCP is enabled by using the [OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL](opm-get-virtual-protection-level.md) or [OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL](opm-get-actual-protection-level.md) status request.</span></span>

<span data-ttu-id="cc479-143">Семантика ОПМ также поддерживает следующее:</span><span class="sxs-lookup"><span data-stu-id="cc479-143">OPM semantics also support the following:</span></span>

-   <span data-ttu-id="cc479-144">Повторители HDCP.</span><span class="sxs-lookup"><span data-stu-id="cc479-144">HDCP repeaters.</span></span> <span data-ttu-id="cc479-145">*Повторитель HDCP* — это устройство HDCP, которое может получить содержимое HDCP, а также повторно зашифровать и передать то же содержимое.</span><span class="sxs-lookup"><span data-stu-id="cc479-145">An *HDCP repeater* is an HDCP device that can receive HDCP content and also re-encrypt and transmit the same content.</span></span>
-   <span data-ttu-id="cc479-146">Отзыв HDCP.</span><span class="sxs-lookup"><span data-stu-id="cc479-146">HDCP revocation.</span></span> <span data-ttu-id="cc479-147">Если к выходному видео ОПМ подключено отозванное устройство HDCP, видеопотокы не будут передавать видео.</span><span class="sxs-lookup"><span data-stu-id="cc479-147">If a revoked HDCP device is attached to the OPM video output, the video output will not transmit the video.</span></span> <span data-ttu-id="cc479-148">Приложению не нужно анализировать сообщения о возобновлении системы HDCP (Срмс) или определять, было ли отменено выходное устройство.</span><span class="sxs-lookup"><span data-stu-id="cc479-148">The application does not need to parse HDCP system renewability messages (SRMs) or determine whether the output device has been revoked.</span></span> <span data-ttu-id="cc479-149">Дополнительные сведения см. в описании команды [**ОПМ \_ Set \_ HDCP \_ СРМ**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="cc479-149">For more information, see the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="cc479-150">При использовании семантики Копп интерфейс [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) не поддерживает повторители HDCP.</span><span class="sxs-lookup"><span data-stu-id="cc479-150">When COPP semantics are used, the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface does not support HDCP repeaters.</span></span> <span data-ttu-id="cc479-151">Кроме того, он не обрабатывает отзыв HDCP.</span><span class="sxs-lookup"><span data-stu-id="cc479-151">Also, it does not handle HDCP revocation.</span></span> <span data-ttu-id="cc479-152">Вместо этого приложение должно проанализировать СРМ, чтобы определить, было ли отозвано устройство HDCP.</span><span class="sxs-lookup"><span data-stu-id="cc479-152">Instead, the application must parse the SRM to determine whether an HDCP device has been revoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc479-153">Требования</span><span class="sxs-lookup"><span data-stu-id="cc479-153">Requirements</span></span>



| <span data-ttu-id="cc479-154">Требование</span><span class="sxs-lookup"><span data-stu-id="cc479-154">Requirement</span></span> | <span data-ttu-id="cc479-155">Значение</span><span class="sxs-lookup"><span data-stu-id="cc479-155">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc479-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc479-156">Minimum supported client</span></span><br/> | <span data-ttu-id="cc479-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc479-157">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cc479-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc479-158">Minimum supported server</span></span><br/> | <span data-ttu-id="cc479-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc479-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cc479-160">Header</span><span class="sxs-lookup"><span data-stu-id="cc479-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc479-161"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc479-161"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc479-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc479-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc479-163">Перечисления ОПМ</span><span class="sxs-lookup"><span data-stu-id="cc479-163">OPM Enumerations</span></span>](opm-enumerations.md)
</dt> </dl>

 

 




