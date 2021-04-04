---
title: Класс MDM_VPNv2_Sso03
description: Класс MDM \_ Поддержка vpnv2 \_ Sso03 можно использовать для выбора сертификата, отличного от сертификата проверки подлинности VPN, для проверки подлинности Kerberos в случае соответствия устройства требованиям.
ms.assetid: 179b6b69-1319-4310-aebc-f61550af6c77
keywords:
- Класс MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Sso03
- MDM_VPNv2_Sso03.InstanceID
- MDM_VPNv2_Sso03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5f3f10d365e1405981e206963cd98f0b7f803c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989047"
---
# <a name="mdm_vpnv2_sso03-class"></a><span data-ttu-id="a8760-105">\_Класс MDM поддержка vpnv2 \_ Sso03</span><span class="sxs-lookup"><span data-stu-id="a8760-105">MDM\_VPNv2\_Sso03 class</span></span>

<span data-ttu-id="a8760-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a8760-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a8760-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a8760-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a8760-108">Класс **MDM \_ Поддержка vpnv2 \_ Sso03** можно использовать для выбора сертификата, отличного от сертификата проверки подлинности VPN, для проверки подлинности Kerberos в случае соответствия устройства требованиям.</span><span class="sxs-lookup"><span data-stu-id="a8760-108">The **MDM\_VPNv2\_Sso03** class can be used to select a certificate different from the VPN Authentication certificate for the Kerberos Authentication in the case of Device Compliance.</span></span>

<span data-ttu-id="a8760-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a8760-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8760-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8760-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Sso03
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
  string  IssuerHash;
  string  Eku;
};
```

## <a name="members"></a><span data-ttu-id="a8760-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a8760-111">Members</span></span>

<span data-ttu-id="a8760-112">Класс **MDM \_ Поддержка vpnv2 \_ Sso03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a8760-112">The **MDM\_VPNv2\_Sso03** class has these types of members:</span></span>

-   [<span data-ttu-id="a8760-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8760-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8760-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8760-114">Properties</span></span>

<span data-ttu-id="a8760-115">Класс **MDM \_ Поддержка vpnv2 \_ Sso03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a8760-115">The **MDM\_VPNv2\_Sso03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a8760-116">EKU</span><span class="sxs-lookup"><span data-stu-id="a8760-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8760-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8760-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8760-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8760-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a8760-119">Enabled</span><span class="sxs-lookup"><span data-stu-id="a8760-119">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8760-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a8760-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8760-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8760-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a8760-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a8760-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8760-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8760-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8760-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8760-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8760-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a8760-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a8760-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="a8760-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="a8760-127">иссуерхаш</span><span class="sxs-lookup"><span data-stu-id="a8760-127">IssuerHash</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-issuerhash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8760-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8760-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8760-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a8760-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a8760-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a8760-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8760-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a8760-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8760-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a8760-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8760-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a8760-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a8760-134">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="a8760-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="a8760-135">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/девицекомплианце"</span><span class="sxs-lookup"><span data-stu-id="a8760-135">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/DeviceCompliance"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8760-136">Требования</span><span class="sxs-lookup"><span data-stu-id="a8760-136">Requirements</span></span>



| <span data-ttu-id="a8760-137">Требование</span><span class="sxs-lookup"><span data-stu-id="a8760-137">Requirement</span></span> | <span data-ttu-id="a8760-138">Значение</span><span class="sxs-lookup"><span data-stu-id="a8760-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8760-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8760-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a8760-140">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a8760-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8760-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8760-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a8760-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a8760-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a8760-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a8760-143">Namespace</span></span><br/>                | <span data-ttu-id="a8760-144">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="a8760-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a8760-145">MOF</span><span class="sxs-lookup"><span data-stu-id="a8760-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8760-146"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8760-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8760-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a8760-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8760-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8760-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8760-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8760-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8760-150">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="a8760-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

