---
description: Описывает устройство доверенный платформенный модуль (TPM) (TPM).
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: Класс CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080602"
---
# <a name="cim_tpm-class"></a><span data-ttu-id="1637e-103">\_Класс TPM CIM</span><span class="sxs-lookup"><span data-stu-id="1637e-103">CIM\_TPM class</span></span>

<span data-ttu-id="1637e-104">Описывает устройство доверенный платформенный модуль (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="1637e-104">Describes a Trusted Platform Module (TPM) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1637e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1637e-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a><span data-ttu-id="1637e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1637e-106">Members</span></span>

<span data-ttu-id="1637e-107">Класс **\_ TPM CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1637e-107">The **CIM\_TPM** class has these types of members:</span></span>

-   [<span data-ttu-id="1637e-108">Методы</span><span class="sxs-lookup"><span data-stu-id="1637e-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="1637e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1637e-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1637e-110">Методы</span><span class="sxs-lookup"><span data-stu-id="1637e-110">Methods</span></span>

<span data-ttu-id="1637e-111">Класс **\_ TPM CIM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1637e-111">The **CIM\_TPM** class has these methods.</span></span>



| <span data-ttu-id="1637e-112">Метод</span><span class="sxs-lookup"><span data-stu-id="1637e-112">Method</span></span>                                                         | <span data-ttu-id="1637e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1637e-113">Description</span></span>                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1637e-114">**чанжеовнераус**</span><span class="sxs-lookup"><span data-stu-id="1637e-114">**ChangeOwnerAuth**</span></span>](cim-tpm-changeownerauth.md)             | <span data-ttu-id="1637e-115">Изменяет учетные данные авторизации владельца устройства TPM.</span><span class="sxs-lookup"><span data-stu-id="1637e-115">Changes the owner authorization credential of a TPM device.</span></span><br/>                                                  |
| [<span data-ttu-id="1637e-116">**рекуесттпмстатечанже**</span><span class="sxs-lookup"><span data-stu-id="1637e-116">**RequestTPMStateChange**</span></span>](cim-tpm-requesttpmstatechange.md) | <span data-ttu-id="1637e-117">Запрашивает изменение состояния TPM на значение, указанное в параметре **рекуестедтпмстате** .</span><span class="sxs-lookup"><span data-stu-id="1637e-117">Requests that the state of the TPM be changed to the value specified in the **RequestedTPMState** parameter.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1637e-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="1637e-118">Properties</span></span>

<span data-ttu-id="1637e-119">Класс **\_ TPM CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1637e-119">The **CIM\_TPM** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1637e-120">**аваилаблерекуестедтпмстатес**</span><span class="sxs-lookup"><span data-stu-id="1637e-120">**AvailableRequestedTPMStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-121">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="1637e-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1637e-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-123">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ доверенный платформенный модуль CIM**.**Рекуесттпмстатечанже**, CIM \_ Тпмкапабилитиес. рекуестедтпмстатессуппортед ")</span><span class="sxs-lookup"><span data-stu-id="1637e-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**, CIM\_TPMCapabilities.RequestedTPMStatesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-124">Возможные значения для параметра *рекуестедтпмстате* метода [**рекуесттпмстатечанже**](cim-tpm-requesttpmstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="1637e-124">The possible values for the *RequestedTPMState* parameter of the [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) method.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1637e-125">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1637e-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="1637e-126">**S1 Enabled — активный — владелец** (2)</span><span class="sxs-lookup"><span data-stu-id="1637e-126">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="1637e-127">**Недоступность S2 — активный — владелец** (3)</span><span class="sxs-lookup"><span data-stu-id="1637e-127">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="1637e-128">**S3 Enabled — неактивно — владелец** (4)</span><span class="sxs-lookup"><span data-stu-id="1637e-128">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="1637e-129">**Состояние S4 отключено — неактивно — владелец** (5)</span><span class="sxs-lookup"><span data-stu-id="1637e-129">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-130">**S5 включено — активно — не владеет** (6)</span><span class="sxs-lookup"><span data-stu-id="1637e-130">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-131">**S6 Disabled — активный — не владеет** (7)</span><span class="sxs-lookup"><span data-stu-id="1637e-131">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-132">**S7 Enabled — Inactive — не владеет** (8)</span><span class="sxs-lookup"><span data-stu-id="1637e-132">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-133">**S8 Disabled — неактивный — не владеет** (9)</span><span class="sxs-lookup"><span data-stu-id="1637e-133">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1637e-134">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1637e-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1637e-135">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1637e-135">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1637e-136">**тпмманафуктурермажорревисион**</span><span class="sxs-lookup"><span data-stu-id="1637e-136">**TPMManafucturerMajorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1637e-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (TPM. TCG, \| часть 2 v1dot2, \| раздел 5,3 \| версии \| ревмажор ")</span><span class="sxs-lookup"><span data-stu-id="1637e-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMajor")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-140">Основная Редакция поставщика TPM.</span><span class="sxs-lookup"><span data-stu-id="1637e-140">The manufacturer major revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="1637e-141">**тпммануфактурерид**</span><span class="sxs-lookup"><span data-stu-id="1637e-141">**TPMManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1637e-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-144">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (TPM. TCG \| часть 2 v1dot2 \| раздел 21,6 \| \_ \_ сведения о версии заглушки TPM \_ \| тпмвендорид ")</span><span class="sxs-lookup"><span data-stu-id="1637e-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|tpmVendorID")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-145">ИДЕНТИФИКАТОР производителя доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="1637e-145">The TPM manufacturer ID.</span></span>

</dd> <dt>

<span data-ttu-id="1637e-146">**тпммануфактуреринфо**</span><span class="sxs-lookup"><span data-stu-id="1637e-146">**TPMManufacturerInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1637e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-149">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (TPM. TCG \| Part 2 v 1.2. TCG \| раздел 21,6 \| \_ \_ сведения о версии заглушки TPM \_ \| вендорспеЦифик ")</span><span class="sxs-lookup"><span data-stu-id="1637e-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1.2.TCG\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|vendorSpecific")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-150">Дополнительные сведения, определяемые производителем TPM.</span><span class="sxs-lookup"><span data-stu-id="1637e-150">The additional information defined by the TPM manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="1637e-151">**тпммануфактурерминорревисион**</span><span class="sxs-lookup"><span data-stu-id="1637e-151">**TPMManufacturerMinorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1637e-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-154">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (TPM. TCG, \| часть 2 v1dot2, \| раздел 5,3 \| версии \| ревминор ")</span><span class="sxs-lookup"><span data-stu-id="1637e-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMinor")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-155">Незначительная редакция изготовителя TPM.</span><span class="sxs-lookup"><span data-stu-id="1637e-155">The manufacturer minor revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="1637e-156">**тпмспекмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="1637e-156">**TPMSpecMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1637e-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-159">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (TPM. TCG \| часть 2 v1dot2 \| раздел 5,3 \| версии \| Major "," Тсс. \|Раздел "TCG Level 1 v 1.2 \| " 2.3.2.18 ")</span><span class="sxs-lookup"><span data-stu-id="1637e-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|major", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-160">Основная версия TPM.</span><span class="sxs-lookup"><span data-stu-id="1637e-160">The major version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="1637e-161">**тпмспекминорверсион**</span><span class="sxs-lookup"><span data-stu-id="1637e-161">**TPMSpecMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1637e-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-164">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (TPM. TCG \| , часть 2 \| , v1dot2 раздел 5,3 \| \| номер дополнительной версии "," Тсс. \|Раздел "TCG Level 1 v 1.2 \| " 2.3.2.18 ")</span><span class="sxs-lookup"><span data-stu-id="1637e-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|minor", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-165">Дополнительный номер версии TPM.</span><span class="sxs-lookup"><span data-stu-id="1637e-165">The minor version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="1637e-166">**тпмстате**</span><span class="sxs-lookup"><span data-stu-id="1637e-166">**TPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1637e-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-169">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (TPM. TCG \| Part 1 v1dot2 \| Section 9,4 "," TPM. TCG \| часть 2 v1dot2 \| раздел 7,1 \| \_ "постоянные \_ Флаги TPM"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM CIM**.**Рекуесттпмстатечанже**","**CIM \_ TPM**.**Транситионингтотпмстате**")</span><span class="sxs-lookup"><span data-stu-id="1637e-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 1 v1dot2\|Section 9.4", "TPM.TCG\|Part 2 v1dot2\|Section 7.1\|TPM\_PERMANENT\_FLAGS"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TransitioningToTPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-170">Рабочее состояние доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="1637e-170">The operational state of the TPM.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1637e-171">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1637e-171">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="1637e-172">**S1 Enabled — активный — владелец** (2)</span><span class="sxs-lookup"><span data-stu-id="1637e-172">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="1637e-173">**Недоступность S2 — активный — владелец** (3)</span><span class="sxs-lookup"><span data-stu-id="1637e-173">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="1637e-174">**S3 Enabled — неактивно — владелец** (4)</span><span class="sxs-lookup"><span data-stu-id="1637e-174">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="1637e-175">**Состояние S4 отключено — неактивно — владелец** (5)</span><span class="sxs-lookup"><span data-stu-id="1637e-175">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-176">**S5 включено — активно — не владеет** (6)</span><span class="sxs-lookup"><span data-stu-id="1637e-176">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-177">**S6 Disabled — активный — не владеет** (7)</span><span class="sxs-lookup"><span data-stu-id="1637e-177">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-178">**S7 Enabled — Inactive — не владеет** (8)</span><span class="sxs-lookup"><span data-stu-id="1637e-178">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-179">**S8 Disabled — неактивный — не владеет** (9)</span><span class="sxs-lookup"><span data-stu-id="1637e-179">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1637e-180">**Неприменимо** (10)</span><span class="sxs-lookup"><span data-stu-id="1637e-180">**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1637e-181">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1637e-181">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1637e-182">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1637e-182">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1637e-183">**транситионингтотпмстате**</span><span class="sxs-lookup"><span data-stu-id="1637e-183">**TransitioningToTPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1637e-184">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1637e-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1637e-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1637e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1637e-186">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ доверенный платформенный модуль CIM**.**Рекуесттпмстатечанже**","**CIM \_ TPM**.**Тпмстате**")</span><span class="sxs-lookup"><span data-stu-id="1637e-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="1637e-187">Целевое состояние, в которое будет переходить доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="1637e-187">The target state to which the TPM is transitioning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1637e-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1637e-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="1637e-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled — активный — владелец** (2)</span><span class="sxs-lookup"><span data-stu-id="1637e-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="1637e-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**Недоступность S2 — активный — владелец** (3)</span><span class="sxs-lookup"><span data-stu-id="1637e-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="1637e-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled — неактивно — владелец** (4)</span><span class="sxs-lookup"><span data-stu-id="1637e-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="1637e-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**Состояние S4 отключено — неактивно — владелец** (5)</span><span class="sxs-lookup"><span data-stu-id="1637e-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 включено — активно — не владеет** (6)</span><span class="sxs-lookup"><span data-stu-id="1637e-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled — активный — не владеет** (7)</span><span class="sxs-lookup"><span data-stu-id="1637e-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled — Inactive — не владеет** (8)</span><span class="sxs-lookup"><span data-stu-id="1637e-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="1637e-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled — неактивный — не владеет** (9)</span><span class="sxs-lookup"><span data-stu-id="1637e-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1637e-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (10)</span><span class="sxs-lookup"><span data-stu-id="1637e-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="1637e-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Без изменений** (11)</span><span class="sxs-lookup"><span data-stu-id="1637e-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (11)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1637e-199">(12)</span><span class="sxs-lookup"><span data-stu-id="1637e-199">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1637e-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="1637e-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1637e-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1637e-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="1637e-202"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1637e-202"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1637e-203">Требования</span><span class="sxs-lookup"><span data-stu-id="1637e-203">Requirements</span></span>



| <span data-ttu-id="1637e-204">Требование</span><span class="sxs-lookup"><span data-stu-id="1637e-204">Requirement</span></span> | <span data-ttu-id="1637e-205">Значение</span><span class="sxs-lookup"><span data-stu-id="1637e-205">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1637e-206">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1637e-206">Minimum supported client</span></span><br/> | <span data-ttu-id="1637e-207">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1637e-207">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1637e-208">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1637e-208">Minimum supported server</span></span><br/> | <span data-ttu-id="1637e-209">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1637e-209">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1637e-210">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1637e-210">Namespace</span></span><br/>                | <span data-ttu-id="1637e-211">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1637e-211">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1637e-212">MOF</span><span class="sxs-lookup"><span data-stu-id="1637e-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1637e-213"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1637e-213"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1637e-214">DLL</span><span class="sxs-lookup"><span data-stu-id="1637e-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1637e-215"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1637e-215"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1637e-216">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1637e-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1637e-217">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="1637e-217">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

