---
description: Запрашивает изменение состояния TPM на значение, указанное в параметре Рекуестедтпмстате.
ms.assetid: 7ad8bf4e-6263-45d5-8f33-fb842bbf1f1a
title: Метод Рекуесттпмстатечанже класса CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.RequestTPMStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39bded1a43dd547780c3924f3af9c37cfc79aa1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991593"
---
# <a name="requesttpmstatechange-method-of-the-cim_tpm-class"></a><span data-ttu-id="abb6e-103">Метод Рекуесттпмстатечанже \_ класса TPM CIM</span><span class="sxs-lookup"><span data-stu-id="abb6e-103">RequestTPMStateChange method of the CIM\_TPM class</span></span>

<span data-ttu-id="abb6e-104">Запрашивает изменение состояния TPM на значение, указанное в параметре *рекуестедтпмстате* .</span><span class="sxs-lookup"><span data-stu-id="abb6e-104">Requests that the state of the TPM be changed to the value specified in the *RequestedTPMState* parameter.</span></span> <span data-ttu-id="abb6e-105">Если вызов метода завершается успешно, свойство **тпмстате** должно быть равно значению параметра **рекуестедтпмстате** .</span><span class="sxs-lookup"><span data-stu-id="abb6e-105">If the method invocation completes successfully, the **TPMState** property shall be equal to the **RequestedTPMState** parameter.</span></span> <span data-ttu-id="abb6e-106">Вызов метода **рекуесттпмстатечанже** несколько раз может привести к перезаписанию или потере более ранних запросов.</span><span class="sxs-lookup"><span data-stu-id="abb6e-106">Invoking the **RequestTPMStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb6e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abb6e-107">Syntax</span></span>


```mof
uint32 RequestTPMStateChange(
  [in]  uint16              RequestedTPMState,
  [in]  string              AuthorizationToken,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="abb6e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="abb6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abb6e-109">*Рекуестедтпмстате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abb6e-109">*RequestedTPMState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb6e-110">Запрошенное состояние доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="abb6e-110">The requested TPM states.</span></span>

<dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="abb6e-111">**S1 Enabled — активный — владелец** (2)</span><span class="sxs-lookup"><span data-stu-id="abb6e-111">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="abb6e-112">**Недоступность S2 — активный — владелец** (3)</span><span class="sxs-lookup"><span data-stu-id="abb6e-112">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="abb6e-113">**S3 Enabled — неактивно — владелец** (4)</span><span class="sxs-lookup"><span data-stu-id="abb6e-113">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="abb6e-114">**Состояние S4 отключено — неактивно — владелец** (5)</span><span class="sxs-lookup"><span data-stu-id="abb6e-114">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="abb6e-115">**S5 включено — активно — не владеет** (6)</span><span class="sxs-lookup"><span data-stu-id="abb6e-115">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="abb6e-116">**S6 Disabled — активный — не владеет** (7)</span><span class="sxs-lookup"><span data-stu-id="abb6e-116">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="abb6e-117">**S7 Enabled — Inactive — не владеет** (8)</span><span class="sxs-lookup"><span data-stu-id="abb6e-117">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="abb6e-118">**S8 Disabled — неактивный — не владеет** (9)</span><span class="sxs-lookup"><span data-stu-id="abb6e-118">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="abb6e-119">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="abb6e-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="abb6e-120">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="abb6e-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="abb6e-121">*Аусоризатионтокен* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abb6e-121">*AuthorizationToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb6e-122">Токен авторизации, который может потребоваться для вступления в силу действия.</span><span class="sxs-lookup"><span data-stu-id="abb6e-122">Authorization token that may be required for the action to take effect.</span></span> <span data-ttu-id="abb6e-123">Параметр *аусоризатионтокен* может потребоваться для установления физического присутствия или для передачи овнераус, определяемого TCG пароля авторизации владельца.</span><span class="sxs-lookup"><span data-stu-id="abb6e-123">The *AuthorizationToken* parameter may be required to establish Physical Presence, or to pass the OwnerAuth, the TCG defined owner authorization password.</span></span> <span data-ttu-id="abb6e-124">В случае с Овнераус может потребоваться шаредкредентиал CIM \_ со значением, отличным от NULL \_ Шаредкредентиал. Secret.</span><span class="sxs-lookup"><span data-stu-id="abb6e-124">In the case of OwnerAuth, the CIM\_SharedCredential with non-null value of the CIM\_SharedCredential.Secret may be required.</span></span> <span data-ttu-id="abb6e-125">Свойство CIM \_ шаредкредентиал. Algorithm также может быть задано на основе свойства CIM \_ Тпмкапабилитиес. суппортедпассвордалгорисмс.</span><span class="sxs-lookup"><span data-stu-id="abb6e-125">The CIM\_SharedCredential.Algorithm property may also be specified based on the property CIM\_TPMCapabilities.SupportedPasswordAlgorithms.</span></span>

</dd> <dt>

<span data-ttu-id="abb6e-126">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="abb6e-126">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abb6e-127">Может содержать ссылку на [**\_ конкретежоб CIM**](cim-concretejob.md) , созданную для отслеживания перехода состояния, инициированного вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="abb6e-127">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="abb6e-128">*Тимеаутпериод* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abb6e-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abb6e-129">Период времени ожидания, указывающий максимальный период времени, в течение которого клиент ждет перехода в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="abb6e-129">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="abb6e-130">Для указания *тимеаутпериод* необходимо использовать формат интервала.</span><span class="sxs-lookup"><span data-stu-id="abb6e-130">The interval format must be used to specify the *TimeoutPeriod*.</span></span> <span data-ttu-id="abb6e-131">Значение 0 или параметр NULL указывает, что у клиента нет требований к времени для перехода.</span><span class="sxs-lookup"><span data-stu-id="abb6e-131">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abb6e-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abb6e-132">Return value</span></span>

<span data-ttu-id="abb6e-133">При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="abb6e-133">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="abb6e-134">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="abb6e-134">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-135">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="abb6e-135">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-136">**Неизвестная или Неуказанная ошибка** (2)</span><span class="sxs-lookup"><span data-stu-id="abb6e-136">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-137">**Невозможно завершить в течение времени ожидания** (3)</span><span class="sxs-lookup"><span data-stu-id="abb6e-137">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-138">**Сбой** (4)</span><span class="sxs-lookup"><span data-stu-id="abb6e-138">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-139">**Недопустимый параметр** (5)</span><span class="sxs-lookup"><span data-stu-id="abb6e-139">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-140">**Используется** (6)</span><span class="sxs-lookup"><span data-stu-id="abb6e-140">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-141">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="abb6e-141">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-142">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="abb6e-142">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-143">**Недопустимая смена состояния** (4097)</span><span class="sxs-lookup"><span data-stu-id="abb6e-143">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-144">**Использование параметра времени ожидания не поддерживается** (4098)</span><span class="sxs-lookup"><span data-stu-id="abb6e-144">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-145">**Занято** (4099)</span><span class="sxs-lookup"><span data-stu-id="abb6e-145">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-146">**Метод зарезервирован** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="abb6e-146">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="abb6e-147">**Зависит от поставщика** (32768.65 535)</span><span class="sxs-lookup"><span data-stu-id="abb6e-147">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="abb6e-148">Требования</span><span class="sxs-lookup"><span data-stu-id="abb6e-148">Requirements</span></span>



| <span data-ttu-id="abb6e-149">Требование</span><span class="sxs-lookup"><span data-stu-id="abb6e-149">Requirement</span></span> | <span data-ttu-id="abb6e-150">Значение</span><span class="sxs-lookup"><span data-stu-id="abb6e-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb6e-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abb6e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="abb6e-152">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="abb6e-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="abb6e-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abb6e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="abb6e-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="abb6e-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="abb6e-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="abb6e-155">Namespace</span></span><br/>                | <span data-ttu-id="abb6e-156">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="abb6e-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="abb6e-157">MOF</span><span class="sxs-lookup"><span data-stu-id="abb6e-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abb6e-158"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abb6e-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abb6e-159">DLL</span><span class="sxs-lookup"><span data-stu-id="abb6e-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abb6e-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abb6e-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="abb6e-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abb6e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abb6e-162">**\_TPM CIM**</span><span class="sxs-lookup"><span data-stu-id="abb6e-162">**CIM\_TPM**</span></span>](cim-tpm.md)
</dt> </dl>

 

 




