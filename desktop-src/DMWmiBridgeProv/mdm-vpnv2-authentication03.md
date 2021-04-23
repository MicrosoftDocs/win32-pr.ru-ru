---
title: Класс MDM_VPNv2_Authentication03
description: Класс MDM \_ Поддержка vpnv2 \_ Authentication03 содержит сведения о проверке подлинности для собственного профиля VPN.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- Класс MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071642"
---
# <a name="mdm_vpnv2_authentication03-class"></a><span data-ttu-id="f2a40-105">\_Класс MDM поддержка vpnv2 \_ Authentication03</span><span class="sxs-lookup"><span data-stu-id="f2a40-105">MDM\_VPNv2\_Authentication03 class</span></span>

<span data-ttu-id="f2a40-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f2a40-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f2a40-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f2a40-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f2a40-108">Класс [**MDM \_ Поддержка vpnv2 \_ Authentication03**](mdm-vpnv2-01.md) содержит сведения о проверке подлинности для собственного профиля VPN.</span><span class="sxs-lookup"><span data-stu-id="f2a40-108">The [**MDM\_VPNv2\_Authentication03**](mdm-vpnv2-01.md) class contains authentication information for the native VPN profile.</span></span>

<span data-ttu-id="f2a40-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f2a40-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2a40-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2a40-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a><span data-ttu-id="f2a40-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f2a40-111">Members</span></span>

<span data-ttu-id="f2a40-112">Класс **MDM \_ Поддержка vpnv2 \_ Authentication03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2a40-112">The **MDM\_VPNv2\_Authentication03** class has these types of members:</span></span>

-   [<span data-ttu-id="f2a40-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2a40-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2a40-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2a40-114">Properties</span></span>

<span data-ttu-id="f2a40-115">Класс **MDM \_ Поддержка vpnv2 \_ Authentication03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2a40-115">The **MDM\_VPNv2\_Authentication03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2a40-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f2a40-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a40-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2a40-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2a40-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2a40-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a40-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2a40-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2a40-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f2a40-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="f2a40-121">мачинемесод</span><span class="sxs-lookup"><span data-stu-id="f2a40-121">MachineMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a40-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2a40-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2a40-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2a40-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f2a40-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f2a40-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a40-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2a40-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2a40-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2a40-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f2a40-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f2a40-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f2a40-128">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f2a40-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="f2a40-129">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/нативепрофиле"</span><span class="sxs-lookup"><span data-stu-id="f2a40-129">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="f2a40-130">усермесод</span><span class="sxs-lookup"><span data-stu-id="f2a40-130">UserMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2a40-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f2a40-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f2a40-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f2a40-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f2a40-133">Требования</span><span class="sxs-lookup"><span data-stu-id="f2a40-133">Requirements</span></span>



| <span data-ttu-id="f2a40-134">Требование</span><span class="sxs-lookup"><span data-stu-id="f2a40-134">Requirement</span></span> | <span data-ttu-id="f2a40-135">Значение</span><span class="sxs-lookup"><span data-stu-id="f2a40-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a40-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2a40-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f2a40-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f2a40-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2a40-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2a40-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f2a40-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2a40-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f2a40-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f2a40-140">Namespace</span></span><br/>                | <span data-ttu-id="f2a40-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f2a40-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f2a40-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f2a40-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2a40-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2a40-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2a40-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f2a40-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2a40-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2a40-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2a40-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2a40-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a40-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="f2a40-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

