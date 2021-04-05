---
title: Класс MDM_VPNv2_PluginProfile02
description: Класс MDM \_ Поддержка vpnv2 \_ PlugInProfile02 описывает сведения, необходимые при использовании подключаемого модуля VPN на основе магазина Windows.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- Класс MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d60b28ec1d2cec9431cc63ac4d0c406d18060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988666"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a><span data-ttu-id="39733-105">\_Класс MDM поддержка vpnv2 \_ PluginProfile02</span><span class="sxs-lookup"><span data-stu-id="39733-105">MDM\_VPNv2\_PluginProfile02 class</span></span>

<span data-ttu-id="39733-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="39733-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="39733-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="39733-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="39733-108">Класс **MDM \_ Поддержка vpnv2 \_ PlugInProfile02** описывает сведения, необходимые при использовании подключаемого модуля VPN на основе магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="39733-108">The **MDM\_VPNv2\_PlugInProfile02** class describes the information needed when using a Windows Store based VPN plugin.</span></span>

<span data-ttu-id="39733-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="39733-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39733-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39733-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a><span data-ttu-id="39733-111">Члены</span><span class="sxs-lookup"><span data-stu-id="39733-111">Members</span></span>

<span data-ttu-id="39733-112">Класс **MDM \_ Поддержка vpnv2 \_ PluginProfile02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39733-112">The **MDM\_VPNv2\_PluginProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="39733-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="39733-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39733-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="39733-114">Properties</span></span>

<span data-ttu-id="39733-115">Класс **MDM \_ Поддержка vpnv2 \_ PluginProfile02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39733-115">The **MDM\_VPNv2\_PluginProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="39733-116">кустомконфигуратион</span><span class="sxs-lookup"><span data-stu-id="39733-116">CustomConfiguration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39733-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39733-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39733-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="39733-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39733-119">кустомстореурл</span><span class="sxs-lookup"><span data-stu-id="39733-119">CustomStoreUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39733-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39733-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39733-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="39733-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39733-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="39733-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39733-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39733-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39733-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39733-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39733-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39733-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="39733-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="39733-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="39733-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="39733-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39733-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39733-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39733-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39733-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39733-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="39733-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="39733-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="39733-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="39733-132">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*"</span><span class="sxs-lookup"><span data-stu-id="39733-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="39733-133">плугинпаккажефамилинаме</span><span class="sxs-lookup"><span data-stu-id="39733-133">PluginPackageFamilyName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39733-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39733-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39733-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="39733-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="39733-136">серверурллист</span><span class="sxs-lookup"><span data-stu-id="39733-136">ServerUrlList</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="39733-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="39733-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39733-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="39733-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39733-139">Требования</span><span class="sxs-lookup"><span data-stu-id="39733-139">Requirements</span></span>



| <span data-ttu-id="39733-140">Требование</span><span class="sxs-lookup"><span data-stu-id="39733-140">Requirement</span></span> | <span data-ttu-id="39733-141">Значение</span><span class="sxs-lookup"><span data-stu-id="39733-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39733-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39733-142">Minimum supported client</span></span><br/> | <span data-ttu-id="39733-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="39733-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39733-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39733-144">Minimum supported server</span></span><br/> | <span data-ttu-id="39733-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="39733-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="39733-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39733-146">Namespace</span></span><br/>                | <span data-ttu-id="39733-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="39733-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="39733-148">MOF</span><span class="sxs-lookup"><span data-stu-id="39733-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39733-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39733-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="39733-150">DLL</span><span class="sxs-lookup"><span data-stu-id="39733-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39733-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39733-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39733-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39733-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39733-153">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="39733-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

