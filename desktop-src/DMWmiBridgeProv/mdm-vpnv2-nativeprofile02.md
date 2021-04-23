---
title: Класс MDM_VPNv2_NativeProfile02
description: Класс MDM \_ Поддержка vpnv2 \_ NativeProfile2 определяет сведения о профиле при использовании протокола VPN Windows Inbox (IKEV2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- Класс MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892517"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a><span data-ttu-id="261e4-105">\_Класс MDM поддержка vpnv2 \_ NativeProfile02</span><span class="sxs-lookup"><span data-stu-id="261e4-105">MDM\_VPNv2\_NativeProfile02 class</span></span>

<span data-ttu-id="261e4-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="261e4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="261e4-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="261e4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="261e4-108">Класс **MDM \_ Поддержка vpnv2 \_ NativeProfile2** определяет сведения о профиле при использовании протокола VPN Windows Inbox (IKEV2, PPTP, L2TP).</span><span class="sxs-lookup"><span data-stu-id="261e4-108">The **MDM\_VPNv2\_NativeProfile2** class defines profile information when using a Windows Inbox VPN Protocol (IKEv2, PPTP, L2TP).</span></span>

<span data-ttu-id="261e4-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="261e4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="261e4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="261e4-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a><span data-ttu-id="261e4-111">Члены</span><span class="sxs-lookup"><span data-stu-id="261e4-111">Members</span></span>

<span data-ttu-id="261e4-112">Класс **MDM \_ Поддержка vpnv2 \_ NativeProfile02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="261e4-112">The **MDM\_VPNv2\_NativeProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="261e4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="261e4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="261e4-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="261e4-114">Properties</span></span>

<span data-ttu-id="261e4-115">Класс **MDM \_ Поддержка vpnv2 \_ NativeProfile02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="261e4-115">The **MDM\_VPNv2\_NativeProfile02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="261e4-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="261e4-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261e4-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="261e4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261e4-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="261e4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261e4-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="261e4-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="261e4-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="261e4-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="261e4-121">L2tpPsk</span><span class="sxs-lookup"><span data-stu-id="261e4-121">L2tpPsk</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

<span data-ttu-id="261e4-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="261e4-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261e4-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="261e4-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="261e4-124">NativeProtocolType</span><span class="sxs-lookup"><span data-stu-id="261e4-124">NativeProtocolType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="261e4-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="261e4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261e4-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="261e4-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="261e4-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="261e4-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="261e4-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="261e4-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261e4-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="261e4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="261e4-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="261e4-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="261e4-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="261e4-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="261e4-132">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*"</span><span class="sxs-lookup"><span data-stu-id="261e4-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="261e4-133">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="261e4-133">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="261e4-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="261e4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261e4-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="261e4-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="261e4-136">Серверы</span><span class="sxs-lookup"><span data-stu-id="261e4-136">Servers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="261e4-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="261e4-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="261e4-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="261e4-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="261e4-139">Требования</span><span class="sxs-lookup"><span data-stu-id="261e4-139">Requirements</span></span>



| <span data-ttu-id="261e4-140">Требование</span><span class="sxs-lookup"><span data-stu-id="261e4-140">Requirement</span></span> | <span data-ttu-id="261e4-141">Значение</span><span class="sxs-lookup"><span data-stu-id="261e4-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="261e4-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="261e4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="261e4-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="261e4-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="261e4-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="261e4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="261e4-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="261e4-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="261e4-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="261e4-146">Namespace</span></span><br/>                | <span data-ttu-id="261e4-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="261e4-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="261e4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="261e4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="261e4-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="261e4-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="261e4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="261e4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="261e4-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="261e4-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="261e4-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="261e4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261e4-153">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="261e4-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

