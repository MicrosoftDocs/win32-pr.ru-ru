---
title: Класс MDM_Policy_Result01_Security02
description: '\_Класс политики MDM \_ Result01 \_ Security02 представляет доступные политики безопасности.'
ms.assetid: e4f9bbeb-b542-454d-930b-0b4ac88fe189
keywords:
- Класс MDM_Policy_Result01_Security02
- MDM_Policy_Result01_Security02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Security02
- MDM_Policy_Result01_Security02.InstanceID
- MDM_Policy_Result01_Security02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 959d5cbc9382b4bef0899f5b44d8ee2d171bd704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071424"
---
# <a name="mdm_policy_result01_security02-class"></a><span data-ttu-id="f569c-105">\_Класс политики MDM \_ Result01 \_ Security02</span><span class="sxs-lookup"><span data-stu-id="f569c-105">MDM\_Policy\_Result01\_Security02 class</span></span>

<span data-ttu-id="f569c-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f569c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f569c-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f569c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f569c-108">Класс **\_ политики MDM \_ Result01 \_ Security02** представляет доступные политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="f569c-108">The **MDM\_Policy\_Result01\_Security02** class represents the security policies available.</span></span>

<span data-ttu-id="f569c-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f569c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f569c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f569c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Security02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddProvisioningPackage;
  sint32 AllowRemoveProvisioningPackage;
  sint32 ClearTPMIfNotReady;
  sint32 PreventAutomaticDeviceEncryptionForAzureADJoinedDevices;
  sint32 RequireDeviceEncryption;
  sint32 RequireProvisioningPackageSignature;
  sint32 RequireRetrieveHealthCertificateOnBoot;
};
```

## <a name="members"></a><span data-ttu-id="f569c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f569c-111">Members</span></span>

<span data-ttu-id="f569c-112">Класс **\_ политики MDM \_ Result01 \_ Security02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f569c-112">The **MDM\_Policy\_Result01\_Security02** class has these types of members:</span></span>

-   [<span data-ttu-id="f569c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f569c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f569c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f569c-114">Properties</span></span>

<span data-ttu-id="f569c-115">Класс **\_ политики MDM \_ Result01 \_ Security02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f569c-115">The **MDM\_Policy\_Result01\_Security02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f569c-116">AllowAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="f569c-116">AllowAddProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowaddprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f569c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f569c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f569c-119">AllowRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="f569c-119">AllowRemoveProvisioningPackage</span></span>](/windows/client-management/mdm/policy-csp-security#security-allowremoveprovisioningpackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f569c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f569c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f569c-122">клеартпмифнотреади</span><span class="sxs-lookup"><span data-stu-id="f569c-122">ClearTPMIfNotReady</span></span>](/windows/client-management/mdm/policy-csp-security#security-cleartpmifnotready)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f569c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f569c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f569c-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f569c-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f569c-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f569c-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f569c-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f569c-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f569c-129">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f569c-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="f569c-130">Для этого класса строка имеет значение "Security".</span><span class="sxs-lookup"><span data-stu-id="f569c-130">For this class, the string is "Security".</span></span>

</dd> <dt>

<span data-ttu-id="f569c-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f569c-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f569c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f569c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f569c-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f569c-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f569c-135">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f569c-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="f569c-136">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="f569c-136">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="f569c-137">превентаутоматикдевицеенкриптионфоразуреаджоинеддевицес</span><span class="sxs-lookup"><span data-stu-id="f569c-137">PreventAutomaticDeviceEncryptionForAzureADJoinedDevices</span></span>](/windows/client-management/mdm/policy-csp-security#security-preventautomaticdeviceencryptionforazureadjoineddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f569c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f569c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f569c-140">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="f569c-140">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/policy-csp-security#security-requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f569c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f569c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f569c-143">RequireProvisioningPackageSignature</span><span class="sxs-lookup"><span data-stu-id="f569c-143">RequireProvisioningPackageSignature</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireprovisioningpackagesignature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f569c-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f569c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f569c-146">RequireRetrieveHealthCertificateOnBoot</span><span class="sxs-lookup"><span data-stu-id="f569c-146">RequireRetrieveHealthCertificateOnBoot</span></span>](/windows/client-management/mdm/policy-csp-security#security-requireretrievehealthcertificateonboot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f569c-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f569c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f569c-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f569c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f569c-149">Требования</span><span class="sxs-lookup"><span data-stu-id="f569c-149">Requirements</span></span>



| <span data-ttu-id="f569c-150">Требование</span><span class="sxs-lookup"><span data-stu-id="f569c-150">Requirement</span></span> | <span data-ttu-id="f569c-151">Значение</span><span class="sxs-lookup"><span data-stu-id="f569c-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f569c-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f569c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f569c-153">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f569c-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f569c-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f569c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f569c-155">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f569c-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f569c-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f569c-156">Namespace</span></span><br/>                | <span data-ttu-id="f569c-157">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f569c-157">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="f569c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="f569c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f569c-159"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f569c-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f569c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="f569c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f569c-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f569c-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f569c-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f569c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f569c-163">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="f569c-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

