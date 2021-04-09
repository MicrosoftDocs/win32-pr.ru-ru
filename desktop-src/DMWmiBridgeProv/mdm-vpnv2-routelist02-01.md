---
title: Класс MDM_VPNv2_RouteList02_01
description: Класс MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01 содержит необязательный список маршрутов, которые будут добавлены в таблицу МАРШРУТИЗАЦИИ для интерфейса VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- Класс MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071843"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a><span data-ttu-id="10abb-105">\_Класс MDM поддержка vpnv2 \_ RouteList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="10abb-105">MDM\_VPNv2\_RouteList02\_01 class</span></span>

<span data-ttu-id="10abb-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="10abb-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="10abb-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="10abb-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="10abb-108">Класс **MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01** содержит необязательный список маршрутов, которые будут добавлены в таблицу маршрутизации для интерфейса VPN.</span><span class="sxs-lookup"><span data-stu-id="10abb-108">The **MDM\_VPNv2\_RouteList02\_01** class contains an optional list of routes to be added to the routing table for the VPN interface.</span></span>

<span data-ttu-id="10abb-109">Это необходимо для случая разделенного туннелирования, когда сайт VPN-сервера имеет больше подсетей, подсеть по умолчанию на основе IP-адреса, назначенного интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="10abb-109">This is required for split tunneling case where the VPN server site has more subnets that the default subnet based on the IP assigned to the interface.</span></span>

<span data-ttu-id="10abb-110">Каждый компьютер, на котором работает TCP/IP, принимает решения о маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="10abb-110">Every computer that runs TCP/IP makes routing decisions.</span></span> <span data-ttu-id="10abb-111">Эти решения контролируются таблицей IP-маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="10abb-111">These decisions are controlled by the IP routing table.</span></span> <span data-ttu-id="10abb-112">Добавление значений в этом узле обновляет таблицу маршрутизации с маршрутами для подключения к интерфейсу VPN POST.</span><span class="sxs-lookup"><span data-stu-id="10abb-112">Adding values under this node updates the routing table with routes for the VPN interface post connection.</span></span> <span data-ttu-id="10abb-113">Значения в этом узле представляют префикс назначения для IP-маршрутов.</span><span class="sxs-lookup"><span data-stu-id="10abb-113">The values under this node represent the destination prefix of IP routes.</span></span> <span data-ttu-id="10abb-114">Префикс назначения состоит из префикса IP-адреса и длины префикса.</span><span class="sxs-lookup"><span data-stu-id="10abb-114">A destination prefix consists of an IP address prefix and a prefix length.</span></span>

<span data-ttu-id="10abb-115">Добавление маршрута позволяет сетевому стеку обнаруживать трафик, который должен пройти через VPN-интерфейс для разбиения VPN-подключения с разделением туннеля.</span><span class="sxs-lookup"><span data-stu-id="10abb-115">Adding a route here allows the networking stack to identify the traffic that needs to go over the VPN interface for split tunnel VPN.</span></span> <span data-ttu-id="10abb-116">Некоторые VPN-серверы могут настроить это во время согласования подключения, и эти сведения не нужны в профиле VPN.</span><span class="sxs-lookup"><span data-stu-id="10abb-116">Some VPN servers can configure this during connect negotiation and do not need this information in the VPN Profile.</span></span> <span data-ttu-id="10abb-117">Обратитесь к администратору VPN-сервера, чтобы определить, требуются ли эти сведения в профиле VPN.</span><span class="sxs-lookup"><span data-stu-id="10abb-117">Please check with your VPN server administrator to determine whether you need this information in the VPN profile.</span></span>

<span data-ttu-id="10abb-118">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="10abb-118">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10abb-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10abb-119">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a><span data-ttu-id="10abb-120">Члены</span><span class="sxs-lookup"><span data-stu-id="10abb-120">Members</span></span>

<span data-ttu-id="10abb-121">Класс **MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="10abb-121">The **MDM\_VPNv2\_RouteList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="10abb-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="10abb-122">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10abb-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="10abb-123">Properties</span></span>

<span data-ttu-id="10abb-124">Класс **MDM \_ Поддержка vpnv2 \_ RouteList02 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="10abb-124">The **MDM\_VPNv2\_RouteList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="10abb-125">Адрес</span><span class="sxs-lookup"><span data-stu-id="10abb-125">Address</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

<span data-ttu-id="10abb-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10abb-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10abb-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10abb-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="10abb-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="10abb-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10abb-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10abb-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10abb-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10abb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10abb-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="10abb-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="10abb-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="10abb-132">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="10abb-133">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="10abb-133">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10abb-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10abb-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10abb-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10abb-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10abb-136">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="10abb-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="10abb-137">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="10abb-137">Describes the full path to the parent node.</span></span> <span data-ttu-id="10abb-138">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/раутелист"</span><span class="sxs-lookup"><span data-stu-id="10abb-138">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span></span>

</dd> <dt>

[<span data-ttu-id="10abb-139">префикссизе</span><span class="sxs-lookup"><span data-stu-id="10abb-139">PrefixSize</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="10abb-140">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="10abb-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="10abb-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10abb-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10abb-142">Требования</span><span class="sxs-lookup"><span data-stu-id="10abb-142">Requirements</span></span>



| <span data-ttu-id="10abb-143">Требование</span><span class="sxs-lookup"><span data-stu-id="10abb-143">Requirement</span></span> | <span data-ttu-id="10abb-144">Значение</span><span class="sxs-lookup"><span data-stu-id="10abb-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10abb-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10abb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="10abb-146">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="10abb-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="10abb-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10abb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="10abb-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="10abb-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="10abb-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="10abb-149">Namespace</span></span><br/>                | <span data-ttu-id="10abb-150">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="10abb-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="10abb-151">MOF</span><span class="sxs-lookup"><span data-stu-id="10abb-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10abb-152"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10abb-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="10abb-153">DLL</span><span class="sxs-lookup"><span data-stu-id="10abb-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10abb-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10abb-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10abb-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10abb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10abb-156">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="10abb-156">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

