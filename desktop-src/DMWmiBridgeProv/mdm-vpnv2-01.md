---
title: Класс MDM_VPNv2_01
description: Класс MDM \_ Поддержка vpnv2 \_ 01 позволяет НАСТРАИВАТЬ профиль VPN устройства.
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- Класс MDM_VPNv2_01
- MDM_VPNv2_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3457220c438d0143db90c1955d48352353fee29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988815"
---
# <a name="mdm_vpnv2_01-class"></a><span data-ttu-id="32b77-105">\_Класс MDM поддержка vpnv2 \_ 01</span><span class="sxs-lookup"><span data-stu-id="32b77-105">MDM\_VPNv2\_01 class</span></span>

<span data-ttu-id="32b77-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="32b77-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32b77-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="32b77-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32b77-108">Класс **MDM \_ Поддержка vpnv2 \_ 01** позволяет настраивать профиль VPN устройства.</span><span class="sxs-lookup"><span data-stu-id="32b77-108">The **MDM\_VPNv2\_01** class allows configuration of the VPN profile of the device.</span></span>

<span data-ttu-id="32b77-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="32b77-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b77-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32b77-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a><span data-ttu-id="32b77-111">Члены</span><span class="sxs-lookup"><span data-stu-id="32b77-111">Members</span></span>

<span data-ttu-id="32b77-112">Класс **MDM \_ Поддержка vpnv2 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="32b77-112">The **MDM\_VPNv2\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="32b77-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="32b77-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32b77-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="32b77-114">Properties</span></span>

<span data-ttu-id="32b77-115">Класс **MDM \_ Поддержка vpnv2 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="32b77-115">The **MDM\_VPNv2\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="32b77-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="32b77-116">AlwaysOn</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="32b77-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32b77-119">ByPassForLocal</span><span class="sxs-lookup"><span data-stu-id="32b77-119">ByPassForLocal</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="32b77-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32b77-122">DnsSuffix</span><span class="sxs-lookup"><span data-stu-id="32b77-122">DnsSuffix</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32b77-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32b77-125">едпмодеид</span><span class="sxs-lookup"><span data-stu-id="32b77-125">EdpModeId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32b77-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32b77-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="32b77-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32b77-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32b77-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b77-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32b77-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32b77-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="32b77-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="32b77-133">Для этого класса строка представляет собой имя профиля VPN.</span><span class="sxs-lookup"><span data-stu-id="32b77-133">For this class, the string is the VPN profile name.</span></span>

</dd> <dt>

[<span data-ttu-id="32b77-134">LockDown</span><span class="sxs-lookup"><span data-stu-id="32b77-134">LockDown</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="32b77-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32b77-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="32b77-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32b77-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32b77-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32b77-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32b77-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32b77-141">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="32b77-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="32b77-142">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2"</span><span class="sxs-lookup"><span data-stu-id="32b77-142">For this class, the string is "./Vendor/MSFT/VPNv2"</span></span>

</dd> <dt>

[<span data-ttu-id="32b77-143">профилексмл</span><span class="sxs-lookup"><span data-stu-id="32b77-143">ProfileXML</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32b77-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32b77-146">RememberCredentials</span><span class="sxs-lookup"><span data-stu-id="32b77-146">RememberCredentials</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-147">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="32b77-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32b77-149">TrustedNetworkDetection</span><span class="sxs-lookup"><span data-stu-id="32b77-149">TrustedNetworkDetection</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32b77-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32b77-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32b77-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32b77-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32b77-152">Требования</span><span class="sxs-lookup"><span data-stu-id="32b77-152">Requirements</span></span>



| <span data-ttu-id="32b77-153">Требование</span><span class="sxs-lookup"><span data-stu-id="32b77-153">Requirement</span></span> | <span data-ttu-id="32b77-154">Значение</span><span class="sxs-lookup"><span data-stu-id="32b77-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b77-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32b77-155">Minimum supported client</span></span><br/> | <span data-ttu-id="32b77-156">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="32b77-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32b77-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32b77-157">Minimum supported server</span></span><br/> | <span data-ttu-id="32b77-158">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="32b77-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="32b77-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="32b77-159">Namespace</span></span><br/>                | <span data-ttu-id="32b77-160">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="32b77-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="32b77-161">MOF</span><span class="sxs-lookup"><span data-stu-id="32b77-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32b77-162"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32b77-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="32b77-163">DLL</span><span class="sxs-lookup"><span data-stu-id="32b77-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32b77-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32b77-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b77-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32b77-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b77-166">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="32b77-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

