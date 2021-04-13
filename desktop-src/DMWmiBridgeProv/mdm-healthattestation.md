---
title: Класс MDM_HealthAttestation
description: Класс MDM \_ хеалсаттестатион позволяет ИТ директорам предприятия оценивать работоспособность управляемых устройств и выполнять действия политики предприятия.
ms.assetid: 64f40ccc-98f6-48d6-bcd4-793375e3dbfb
keywords:
- Класс MDM_HealthAttestation
- MDM_HealthAttestation класс, описание
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7f76af135e7eac09b3b104e924b26efbb359b256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489933"
---
# <a name="mdm_healthattestation-class"></a><span data-ttu-id="b701b-105">\_Класс MDM хеалсаттестатион</span><span class="sxs-lookup"><span data-stu-id="b701b-105">MDM\_HealthAttestation class</span></span>

<span data-ttu-id="b701b-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b701b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b701b-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b701b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b701b-108">Класс **MDM \_ ХЕАЛСАТТЕСТАТИОН** позволяет ИТ директорам предприятия оценивать работоспособность управляемых устройств и выполнять действия политики предприятия.</span><span class="sxs-lookup"><span data-stu-id="b701b-108">The **MDM\_HealthAttestation** class enables enterprise IT managers to assess the health of managed devices and take enterprise policy actions.</span></span>

<span data-ttu-id="b701b-109">Ниже приведен список функций, выполняемых CSP Хеалсаттестатион.</span><span class="sxs-lookup"><span data-stu-id="b701b-109">The following is a list of functions performed by the HealthAttestation CSP:</span></span>

-   <span data-ttu-id="b701b-110">Собирает данные, используемые для проверки состояния работоспособности устройств</span><span class="sxs-lookup"><span data-stu-id="b701b-110">Collects data that is used in verifying a devices health states</span></span>
-   <span data-ttu-id="b701b-111">передача данных службе аттестации работоспособности;</span><span class="sxs-lookup"><span data-stu-id="b701b-111">Forwards the data to the Health Attestation Service (HAS)</span></span>
-   <span data-ttu-id="b701b-112">Подготавливает сертификат аттестации работоспособности, который он получает от,</span><span class="sxs-lookup"><span data-stu-id="b701b-112">Provisions the Health Attestation Certificate that it receives from HAS</span></span>
-   <span data-ttu-id="b701b-113">После запроса перенаправляет сертификат аттестации работоспособности (полученный от) и связанные с ним сведения о среде выполнения на сервер MDM для проверки.</span><span class="sxs-lookup"><span data-stu-id="b701b-113">Upon request, forwards the Health Attestation Certificate (received from HAS) and related runtime information to the MDM Server for verification</span></span>

<span data-ttu-id="b701b-114">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b701b-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b701b-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b701b-115">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_HealthAttestation
{
  string  InstanceID;
  string  ParentID;
  sint32  Status;
  boolean ForceRetrieve;
  string  Certificate;
  string  Nonce;
  string  CorrelationID;
  sint32  TpmReadyStatus;
  sint32  MaxSupportedProtocolVersion;
  sint32  PreferredMaxProtocolVersion;
  sint32  CurrentProtocolVersion;
  string  HASEndpoint;
};
```

## <a name="members"></a><span data-ttu-id="b701b-116">Члены</span><span class="sxs-lookup"><span data-stu-id="b701b-116">Members</span></span>

<span data-ttu-id="b701b-117">Класс **MDM \_ хеалсаттестатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b701b-117">The **MDM\_HealthAttestation** class has these types of members:</span></span>

-   [<span data-ttu-id="b701b-118">Методы</span><span class="sxs-lookup"><span data-stu-id="b701b-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="b701b-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="b701b-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b701b-120">Методы</span><span class="sxs-lookup"><span data-stu-id="b701b-120">Methods</span></span>

<span data-ttu-id="b701b-121">Класс **MDM \_ хеалсаттестатион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b701b-121">The **MDM\_HealthAttestation** class has these methods.</span></span>



| <span data-ttu-id="b701b-122">Метод</span><span class="sxs-lookup"><span data-stu-id="b701b-122">Method</span></span>                                                                 | <span data-ttu-id="b701b-123">Описание</span><span class="sxs-lookup"><span data-stu-id="b701b-123">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b701b-124">**верифихеалсмесод**</span><span class="sxs-lookup"><span data-stu-id="b701b-124">**VerifyHealthMethod**</span></span>](mdm-healthattestation-verifyhealthmethod.md) | <span data-ttu-id="b701b-125">Способ уведомления устройства о подготовке запроса на проверку сертификата работоспособности.</span><span class="sxs-lookup"><span data-stu-id="b701b-125">Method to notify the device to prepare a health certificate verification request.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b701b-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="b701b-126">Properties</span></span>

<span data-ttu-id="b701b-127">Класс **MDM \_ хеалсаттестатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b701b-127">The **MDM\_HealthAttestation** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b701b-128">Сертификат</span><span class="sxs-lookup"><span data-stu-id="b701b-128">Certificate</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b701b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b701b-131">Квалификаторы: **октетстринг**</span><span class="sxs-lookup"><span data-stu-id="b701b-131">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b701b-132">CorrelationID</span><span class="sxs-lookup"><span data-stu-id="b701b-132">CorrelationID</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b701b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b701b-135">**куррентпротоколверсион**</span><span class="sxs-lookup"><span data-stu-id="b701b-135">**CurrentProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-136">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b701b-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b701b-138">TBD</span><span class="sxs-lookup"><span data-stu-id="b701b-138">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="b701b-139">форцеретриеве</span><span class="sxs-lookup"><span data-stu-id="b701b-139">ForceRetrieve</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-140">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b701b-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b701b-142">хасендпоинт</span><span class="sxs-lookup"><span data-stu-id="b701b-142">HASEndpoint</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b701b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b701b-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b701b-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b701b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b701b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b701b-148">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b701b-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b701b-149">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="b701b-149">Identifies the name of the parent node.</span></span> <span data-ttu-id="b701b-150">Для этого класса строка имеет значение "Хеалсаттестатион".</span><span class="sxs-lookup"><span data-stu-id="b701b-150">For this class, the string is "HealthAttestation".</span></span>

</dd> <dt>

<span data-ttu-id="b701b-151">**макссуппортедпротоколверсион**</span><span class="sxs-lookup"><span data-stu-id="b701b-151">**MaxSupportedProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-152">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b701b-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b701b-154">TBD</span><span class="sxs-lookup"><span data-stu-id="b701b-154">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="b701b-155">Требуем</span><span class="sxs-lookup"><span data-stu-id="b701b-155">Nonce</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b701b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b701b-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b701b-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b701b-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b701b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b701b-161">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b701b-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b701b-162">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="b701b-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="b701b-163">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="b701b-163">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

<span data-ttu-id="b701b-164">**преферредмакспротоколверсион**</span><span class="sxs-lookup"><span data-stu-id="b701b-164">**PreferredMaxProtocolVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b701b-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-166">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b701b-167">TBD</span><span class="sxs-lookup"><span data-stu-id="b701b-167">TBD</span></span>

</dd> <dt>

[<span data-ttu-id="b701b-168">Состояние</span><span class="sxs-lookup"><span data-stu-id="b701b-168">Status</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-169">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b701b-169">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b701b-171">тпмреадистатус</span><span class="sxs-lookup"><span data-stu-id="b701b-171">TpmReadyStatus</span></span>](/windows/client-management/mdm/healthattestation-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b701b-172">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b701b-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b701b-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b701b-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b701b-174">Требования</span><span class="sxs-lookup"><span data-stu-id="b701b-174">Requirements</span></span>



| <span data-ttu-id="b701b-175">Требование</span><span class="sxs-lookup"><span data-stu-id="b701b-175">Requirement</span></span> | <span data-ttu-id="b701b-176">Значение</span><span class="sxs-lookup"><span data-stu-id="b701b-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b701b-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b701b-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b701b-178">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b701b-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b701b-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b701b-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b701b-180">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b701b-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b701b-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b701b-181">Namespace</span></span><br/>                | <span data-ttu-id="b701b-182">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="b701b-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b701b-183">MOF</span><span class="sxs-lookup"><span data-stu-id="b701b-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b701b-184"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b701b-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b701b-185">DLL</span><span class="sxs-lookup"><span data-stu-id="b701b-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b701b-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b701b-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b701b-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b701b-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b701b-188">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="b701b-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

