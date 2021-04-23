---
title: Константы WINBIO_OPERATION_TYPE (Винбио \_ types. h)
description: Укажите тип выполняемой асинхронной операции.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137775"
---
# <a name="winbio_operation_type-constants"></a><span data-ttu-id="42f61-103">\_ \_ Константы типа операции винбио</span><span class="sxs-lookup"><span data-stu-id="42f61-103">WINBIO\_OPERATION\_TYPE Constants</span></span>

<span data-ttu-id="42f61-104">Следующие константы могут возвращаться биометрическая платформа Windows в [**\_ асинхронном \_ результате винбио**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) для указания типа выполняемой асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="42f61-104">The following constants can be returned by the Windows Biometric Framework in a [**WINBIO\_ASYNC\_RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) to specify the type of asynchronous operation being performed.</span></span>

<dl> <dt>

<span data-ttu-id="42f61-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_Операция винбио \_ None**</span><span class="sxs-lookup"><span data-stu-id="42f61-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO\_OPERATION\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-106">0</span><span class="sxs-lookup"><span data-stu-id="42f61-106">0</span></span>
</dt> <dt>



<span data-ttu-id="42f61-107">Операции не обнаружены.</span><span class="sxs-lookup"><span data-stu-id="42f61-107">No operation has been identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_Операция винбио \_ открыта**</span><span class="sxs-lookup"><span data-stu-id="42f61-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO\_OPERATION\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-109">1</span><span class="sxs-lookup"><span data-stu-id="42f61-109">1</span></span>
</dt> <dt>



<span data-ttu-id="42f61-110">Был открыт сеанс биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="42f61-110">A biometric session was opened.</span></span> <span data-ttu-id="42f61-111">Дополнительные сведения см. в разделе [**винбиоасинкопенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span><span class="sxs-lookup"><span data-stu-id="42f61-111">For more information see [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_закрытие операции \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO\_OPERATION\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-113">2</span><span class="sxs-lookup"><span data-stu-id="42f61-113">2</span></span>
</dt> <dt>



<span data-ttu-id="42f61-114">Биометрическая сессия закрыта.</span><span class="sxs-lookup"><span data-stu-id="42f61-114">A biometric session was closed.</span></span> <span data-ttu-id="42f61-115">Дополнительные сведения см. в разделе [**винбиоклосесессион**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span><span class="sxs-lookup"><span data-stu-id="42f61-115">For more information, see [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**\_Проверка операции \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO\_OPERATION\_VERIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-117">3</span><span class="sxs-lookup"><span data-stu-id="42f61-117">3</span></span>
</dt> <dt>



<span data-ttu-id="42f61-118">Образец биометрической метрики проверен на соответствие удостоверению пользователя.</span><span class="sxs-lookup"><span data-stu-id="42f61-118">A biometric sample was verified against a user identity.</span></span> <span data-ttu-id="42f61-119">Дополнительные сведения см. в разделе [**винбиоверифи**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span><span class="sxs-lookup"><span data-stu-id="42f61-119">For more information, see [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**ВИНБИО \_ операция \_ обнаружения**</span><span class="sxs-lookup"><span data-stu-id="42f61-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO\_OPERATION\_IDENTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-121">4</span><span class="sxs-lookup"><span data-stu-id="42f61-121">4</span></span>
</dt> <dt>



<span data-ttu-id="42f61-122">Биометрическая выборка была захвачена и сравнена с существующим шаблоном.</span><span class="sxs-lookup"><span data-stu-id="42f61-122">A biometric sample was captured and compared to an existing template.</span></span> <span data-ttu-id="42f61-123">Дополнительные сведения см. в разделе [**винбиоидентифи**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span><span class="sxs-lookup"><span data-stu-id="42f61-123">For more information, see [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**ВИНБИО \_ операция при \_ поиске \_ датчика**</span><span class="sxs-lookup"><span data-stu-id="42f61-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO\_OPERATION\_LOCATE\_SENSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-125">5</span><span class="sxs-lookup"><span data-stu-id="42f61-125">5</span></span>
</dt> <dt>



<span data-ttu-id="42f61-126">Номер идентификатора биометрического блока был получен.</span><span class="sxs-lookup"><span data-stu-id="42f61-126">The ID number of a biometric unit was retrieved.</span></span> <span data-ttu-id="42f61-127">Дополнительные сведения см. в разделе [**винбиолокатесенсор**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span><span class="sxs-lookup"><span data-stu-id="42f61-127">For more information, see [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**\_ \_ Начало регистрации операции \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO\_OPERATION\_ENROLL\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-129">6</span><span class="sxs-lookup"><span data-stu-id="42f61-129">6</span></span>
</dt> <dt>



<span data-ttu-id="42f61-130">Инициирована биометрическая последовательность регистрации.</span><span class="sxs-lookup"><span data-stu-id="42f61-130">A biometric enrollment sequence was initiated.</span></span> <span data-ttu-id="42f61-131">Дополнительные сведения см. в разделе [**винбиоенроллбегин**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span><span class="sxs-lookup"><span data-stu-id="42f61-131">For more information, see [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**\_ \_ запись регистрации винбио \_ операции**</span><span class="sxs-lookup"><span data-stu-id="42f61-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO\_OPERATION\_ENROLL\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-133">7</span><span class="sxs-lookup"><span data-stu-id="42f61-133">7</span></span>
</dt> <dt>



<span data-ttu-id="42f61-134">Образец биометрической метрики был захвачен и добавлен в шаблон.</span><span class="sxs-lookup"><span data-stu-id="42f61-134">A biometric sample was captured and added to the template.</span></span> <span data-ttu-id="42f61-135">Дополнительные сведения см. в разделе [**винбиоенроллкаптуре**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span><span class="sxs-lookup"><span data-stu-id="42f61-135">For more information, see [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**\_ \_ фиксация регистрации операции винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO\_OPERATION\_ENROLL\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-137">8</span><span class="sxs-lookup"><span data-stu-id="42f61-137">8</span></span>
</dt> <dt>



<span data-ttu-id="42f61-138">Завершено Завершение ожидающего шаблона биометрического метрики.</span><span class="sxs-lookup"><span data-stu-id="42f61-138">A pending biometric template was finalized.</span></span> <span data-ttu-id="42f61-139">Дополнительные сведения см. в разделе [**винбиоенроллкоммит**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span><span class="sxs-lookup"><span data-stu-id="42f61-139">For more information, see [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**\_ \_ Отмена регистрации операции \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO\_OPERATION\_ENROLL\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-141">9</span><span class="sxs-lookup"><span data-stu-id="42f61-141">9</span></span>
</dt> <dt>



<span data-ttu-id="42f61-142">Незавершенный биометрический шаблон был отклонен.</span><span class="sxs-lookup"><span data-stu-id="42f61-142">A pending biometric template was discarded.</span></span> <span data-ttu-id="42f61-143">Дополнительные сведения см. в разделе [**винбиоенроллдискард**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span><span class="sxs-lookup"><span data-stu-id="42f61-143">For more information, see [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_ \_ Регистрация перечислений операций винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO\_OPERATION\_ENUM\_ENROLLMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-145">10</span><span class="sxs-lookup"><span data-stu-id="42f61-145">10</span></span>
</dt> <dt>



<span data-ttu-id="42f61-146">Подразделы для данного шаблона были перечислены.</span><span class="sxs-lookup"><span data-stu-id="42f61-146">The sub-factors for a given template were enumerated.</span></span> <span data-ttu-id="42f61-147">Дополнительные сведения см. в разделе [**винбиоенуменроллментс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span><span class="sxs-lookup"><span data-stu-id="42f61-147">For more information, see [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**\_ \_ шаблон удаления винбио \_ операции**</span><span class="sxs-lookup"><span data-stu-id="42f61-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO\_OPERATION\_DELETE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-149">11</span><span class="sxs-lookup"><span data-stu-id="42f61-149">11</span></span>
</dt> <dt>



<span data-ttu-id="42f61-150">Биометрическая шаблон удален из хранилища.</span><span class="sxs-lookup"><span data-stu-id="42f61-150">A biometric template was deleted from the store.</span></span> <span data-ttu-id="42f61-151">Дополнительные сведения см. в разделе [**винбиоделететемплате**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span><span class="sxs-lookup"><span data-stu-id="42f61-151">For more information, see [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_ \_ Пример записи операции \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO\_OPERATION\_CAPTURE\_SAMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-153">12</span><span class="sxs-lookup"><span data-stu-id="42f61-153">12</span></span>
</dt> <dt>



<span data-ttu-id="42f61-154">Был собран образец биометрической метрики.</span><span class="sxs-lookup"><span data-stu-id="42f61-154">A biometric sample was captured.</span></span> <span data-ttu-id="42f61-155">Дополнительные сведения см. в разделе [**винбиокаптуресампле**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="42f61-155">For more information, see [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**ВИНБИО \_ операция \_ получения \_ Свойства**</span><span class="sxs-lookup"><span data-stu-id="42f61-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO\_OPERATION\_GET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-157">13</span><span class="sxs-lookup"><span data-stu-id="42f61-157">13</span></span>
</dt> <dt>



<span data-ttu-id="42f61-158">Получено свойство сеанса биометрической метрики, единицы измерения или шаблона.</span><span class="sxs-lookup"><span data-stu-id="42f61-158">A biometric session, unit, or template property was retrieved.</span></span> <span data-ttu-id="42f61-159">Дополнительные сведения см. в разделе [**винбиожетпроперти**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span><span class="sxs-lookup"><span data-stu-id="42f61-159">For more information, see [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_ \_ свойство набора операций \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO\_OPERATION\_SET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-161">14</span><span class="sxs-lookup"><span data-stu-id="42f61-161">14</span></span>
</dt> <dt>



<span data-ttu-id="42f61-162">Задано свойство "биометрическая сессия", "единица", "шаблон" или "учетная запись".</span><span class="sxs-lookup"><span data-stu-id="42f61-162">A biometric session, unit, template, or account property was set.</span></span> <span data-ttu-id="42f61-163">Дополнительные сведения см. в разделе [**винбиосетпроперти**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span><span class="sxs-lookup"><span data-stu-id="42f61-163">For more information, see [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ событие получения винбио \_ операции**</span><span class="sxs-lookup"><span data-stu-id="42f61-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO\_OPERATION\_GET\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-165">15</span><span class="sxs-lookup"><span data-stu-id="42f61-165">15</span></span>
</dt> <dt>



<span data-ttu-id="42f61-166">Не используется.</span><span class="sxs-lookup"><span data-stu-id="42f61-166">Not used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_ \_ блок блокировки операции \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO\_OPERATION\_LOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-168">16</span><span class="sxs-lookup"><span data-stu-id="42f61-168">16</span></span>
</dt> <dt>



<span data-ttu-id="42f61-169">Биометрическая единица заблокирована для монопольного использования в сеансе.</span><span class="sxs-lookup"><span data-stu-id="42f61-169">A biometric unit was locked for exclusive use by a session.</span></span> <span data-ttu-id="42f61-170">Дополнительные сведения см. в разделе [**винбиолоккунит**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span><span class="sxs-lookup"><span data-stu-id="42f61-170">For more information, see [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_ \_ единица разблокировки операции винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO\_OPERATION\_UNLOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-172">17</span><span class="sxs-lookup"><span data-stu-id="42f61-172">17</span></span>
</dt> <dt>



<span data-ttu-id="42f61-173">Блокировка сеанса на биометрической единице была освобождена.</span><span class="sxs-lookup"><span data-stu-id="42f61-173">The session lock on a biometric unit was released.</span></span> <span data-ttu-id="42f61-174">Дополнительные сведения см. в разделе [**винбиаунлоккунит**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span><span class="sxs-lookup"><span data-stu-id="42f61-174">For more information, see [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_ \_ единица управления ОПЕРАЦИей винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-176">18</span><span class="sxs-lookup"><span data-stu-id="42f61-176">18</span></span>
</dt> <dt>



<span data-ttu-id="42f61-177">Определенные поставщиком операции были выполнены над единицей управления.</span><span class="sxs-lookup"><span data-stu-id="42f61-177">Vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="42f61-178">Дополнительные сведения см. в разделе [**винбиоконтролунит**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span><span class="sxs-lookup"><span data-stu-id="42f61-178">For more information, see [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_ \_ \_ привилегированный доступ к единице управления Operation винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-180">19</span><span class="sxs-lookup"><span data-stu-id="42f61-180">19</span></span>
</dt> <dt>



<span data-ttu-id="42f61-181">Определенные привилегированные операции, определяемые поставщиком, выполнялись на единице управления.</span><span class="sxs-lookup"><span data-stu-id="42f61-181">Privileged vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="42f61-182">Дополнительные сведения см. в разделе [**винбиоконтролунитпривилежед**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="42f61-182">For more information, see [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**ВИНБИО \_ операция \_ Open \_ Framework**</span><span class="sxs-lookup"><span data-stu-id="42f61-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO\_OPERATION\_OPEN\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-184">20</span><span class="sxs-lookup"><span data-stu-id="42f61-184">20</span></span>
</dt> <dt>



<span data-ttu-id="42f61-185">Был открыт обработчик биометрической платформы.</span><span class="sxs-lookup"><span data-stu-id="42f61-185">A handle to the biometric framework was opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**ВИНБИО \_ операция \_ закрытия \_ платформы**</span><span class="sxs-lookup"><span data-stu-id="42f61-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO\_OPERATION\_CLOSE\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-187">21</span><span class="sxs-lookup"><span data-stu-id="42f61-187">21</span></span>
</dt> <dt>



<span data-ttu-id="42f61-188">Маркер биометрической платформы был закрыт.</span><span class="sxs-lookup"><span data-stu-id="42f61-188">A handle to the biometric framework was closed.</span></span> <span data-ttu-id="42f61-189">Дополнительные сведения см. в разделе [**винбиоклосефрамеворк**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span><span class="sxs-lookup"><span data-stu-id="42f61-189">For more information, see [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_ \_ \_ поставщики служб ПЕРЕЧИСЛЕНИЯ для операций винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO\_OPERATION\_ENUM\_SERVICE\_PROVIDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-191">22</span><span class="sxs-lookup"><span data-stu-id="42f61-191">22</span></span>
</dt> <dt>



<span data-ttu-id="42f61-192">Установленные поставщики биометрических служб были перечислены.</span><span class="sxs-lookup"><span data-stu-id="42f61-192">The installed biometric service providers were enumerated.</span></span> <span data-ttu-id="42f61-193">Дополнительные сведения см. в разделе [**винбиоенумсервицепровидерс**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span><span class="sxs-lookup"><span data-stu-id="42f61-193">For more information, see [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ биометрические единицы ПЕРЕчислителя операции винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO\_OPERATION\_ENUM\_BIOMETRIC\_UNITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-195">23</span><span class="sxs-lookup"><span data-stu-id="42f61-195">23</span></span>
</dt> <dt>



<span data-ttu-id="42f61-196">Подключенные биометрические единицы были перечислены.</span><span class="sxs-lookup"><span data-stu-id="42f61-196">The attached biometric units were enumerated.</span></span> <span data-ttu-id="42f61-197">Дополнительные сведения см. в разделе [**винбиоасинценумбиометрикунитс**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span><span class="sxs-lookup"><span data-stu-id="42f61-197">For more information, see [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_ \_ базы данных перечислений операций винбио \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO\_OPERATION\_ENUM\_DATABASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-199">24</span><span class="sxs-lookup"><span data-stu-id="42f61-199">24</span></span>
</dt> <dt>



<span data-ttu-id="42f61-200">Зарегистрированные базы данных были перечислены.</span><span class="sxs-lookup"><span data-stu-id="42f61-200">The registered databases were enumerated.</span></span> <span data-ttu-id="42f61-201">Дополнительные сведения см. в разделе [**винбиоенумдатабасес**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span><span class="sxs-lookup"><span data-stu-id="42f61-201">For more information, see [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**\_ \_ Получение единиц операций \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO\_OPERATION\_UNIT\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-203">25</span><span class="sxs-lookup"><span data-stu-id="42f61-203">25</span></span>
</dt> <dt>



<span data-ttu-id="42f61-204">Был создан биометрический модуль.</span><span class="sxs-lookup"><span data-stu-id="42f61-204">A biometric unit was created.</span></span> <span data-ttu-id="42f61-205">Дополнительные сведения см. в разделе [**винбиоасинкмониторфрамеворкчанжес**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="42f61-205">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**\_ \_ Удаление единицы операции \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="42f61-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO\_OPERATION\_UNIT\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-207">26</span><span class="sxs-lookup"><span data-stu-id="42f61-207">26</span></span>
</dt> <dt>



<span data-ttu-id="42f61-208">Биометрическая единица была удалена.</span><span class="sxs-lookup"><span data-stu-id="42f61-208">A biometric unit was deleted.</span></span> <span data-ttu-id="42f61-209">Дополнительные сведения см. в разделе [**винбиоасинкмониторфрамеворкчанжес**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="42f61-209">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**ВИНБИО \_ операции \_ обнаружения \_ и \_ освобождения \_**</span><span class="sxs-lookup"><span data-stu-id="42f61-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO\_OPERATION\_IDENTIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-211">27</span><span class="sxs-lookup"><span data-stu-id="42f61-211">27</span></span>
</dt> <dt>



<span data-ttu-id="42f61-212">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="42f61-212">Reserved.</span></span> <span data-ttu-id="42f61-213">Это значение поддерживается начиная с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="42f61-213">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**ВИНБИО \_ операции \_ проверки \_ и \_ освобождения \_ билета**</span><span class="sxs-lookup"><span data-stu-id="42f61-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO\_OPERATION\_VERIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-215">28</span><span class="sxs-lookup"><span data-stu-id="42f61-215">28</span></span>
</dt> <dt>



<span data-ttu-id="42f61-216">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="42f61-216">Reserved.</span></span> <span data-ttu-id="42f61-217">Это значение поддерживается начиная с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="42f61-217">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_ \_ присутствие монитора винбио \_ Operation**</span><span class="sxs-lookup"><span data-stu-id="42f61-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO\_OPERATION\_MONITOR\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-219">29</span><span class="sxs-lookup"><span data-stu-id="42f61-219">29</span></span>
</dt> <dt>



<span data-ttu-id="42f61-220">Механизм распознавания лиц или контроля IRI был включен.</span><span class="sxs-lookup"><span data-stu-id="42f61-220">The facial recognition or iris monitoring mechanism was turned on.</span></span> <span data-ttu-id="42f61-221">Дополнительные сведения см. в разделе [**винбиомониторпресенце**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span><span class="sxs-lookup"><span data-stu-id="42f61-221">For more information, see [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span></span> <span data-ttu-id="42f61-222">Это значение поддерживается начиная с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="42f61-222">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42f61-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**ВИНБИО \_ операции \_ регистрации \_ SELECT**</span><span class="sxs-lookup"><span data-stu-id="42f61-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO\_OPERATION\_ENROLL\_SELECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f61-224">30</span><span class="sxs-lookup"><span data-stu-id="42f61-224">30</span></span>
</dt> <dt>



<span data-ttu-id="42f61-225">Отдельный пользователь из группы лиц, представленных данными в буфере выборки, был указан для регистрации.</span><span class="sxs-lookup"><span data-stu-id="42f61-225">An individual from a group of individuals that are represented by data in the sample buffer was specified as the individual to enroll.</span></span> <span data-ttu-id="42f61-226">Дополнительные сведения см. в разделе [**винбиоенроллселект**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span><span class="sxs-lookup"><span data-stu-id="42f61-226">For more information, see [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span></span> <span data-ttu-id="42f61-227">Это значение поддерживается начиная с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="42f61-227">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42f61-228">Требования</span><span class="sxs-lookup"><span data-stu-id="42f61-228">Requirements</span></span>



| <span data-ttu-id="42f61-229">Требование</span><span class="sxs-lookup"><span data-stu-id="42f61-229">Requirement</span></span> | <span data-ttu-id="42f61-230">Значение</span><span class="sxs-lookup"><span data-stu-id="42f61-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f61-231">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42f61-231">Minimum supported client</span></span><br/> | <span data-ttu-id="42f61-232">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="42f61-232">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="42f61-233">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42f61-233">Minimum supported server</span></span><br/> | <span data-ttu-id="42f61-234">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="42f61-234">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="42f61-235">Header</span><span class="sxs-lookup"><span data-stu-id="42f61-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f61-236"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="42f61-236"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f61-237">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42f61-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f61-238">Константы клиентского приложения</span><span class="sxs-lookup"><span data-stu-id="42f61-238">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





