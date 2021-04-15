---
title: Класс MDM_VPNv2_Proxy02
description: Класс MDM \_ Поддержка vpnv2 \_ Proxy02 определяет объект конфигурации, обеспечивающий поддержку прокси-сервера после подключения для VPN.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- Класс MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490659"
---
# <a name="mdm_vpnv2_proxy02-class"></a><span data-ttu-id="4fc36-105">\_Класс MDM поддержка vpnv2 \_ Proxy02</span><span class="sxs-lookup"><span data-stu-id="4fc36-105">MDM\_VPNv2\_Proxy02 class</span></span>

<span data-ttu-id="4fc36-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4fc36-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4fc36-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4fc36-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4fc36-108">Класс **MDM \_ Поддержка vpnv2 \_ Proxy02** определяет объект конфигурации, обеспечивающий поддержку прокси-сервера после подключения для VPN.</span><span class="sxs-lookup"><span data-stu-id="4fc36-108">The **MDM\_VPNv2\_Proxy02** class defines a configuration object to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="4fc36-109">Прокси-сервер, определенный для этого профиля, применяется, если этот профиль активен и подключен.</span><span class="sxs-lookup"><span data-stu-id="4fc36-109">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

<span data-ttu-id="4fc36-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4fc36-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc36-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fc36-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a><span data-ttu-id="4fc36-112">Члены</span><span class="sxs-lookup"><span data-stu-id="4fc36-112">Members</span></span>

<span data-ttu-id="4fc36-113">Класс **MDM \_ Поддержка vpnv2 \_ Proxy02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4fc36-113">The **MDM\_VPNv2\_Proxy02** class has these types of members:</span></span>

-   [<span data-ttu-id="4fc36-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4fc36-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4fc36-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="4fc36-115">Properties</span></span>

<span data-ttu-id="4fc36-116">Класс **MDM \_ Поддержка vpnv2 \_ Proxy02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4fc36-116">The **MDM\_VPNv2\_Proxy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4fc36-117">AutoConfigUrl</span><span class="sxs-lookup"><span data-stu-id="4fc36-117">AutoConfigUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc36-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4fc36-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fc36-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4fc36-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4fc36-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4fc36-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc36-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4fc36-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fc36-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4fc36-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fc36-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4fc36-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4fc36-124">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="4fc36-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="4fc36-125">Коллекция объектов конфигурации, обеспечивающая поддержку прокси-сервера после подключения для VPN.</span><span class="sxs-lookup"><span data-stu-id="4fc36-125">A collection of configuration objects to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="4fc36-126">Прокси-сервер, определенный для этого профиля, применяется, если этот профиль активен и подключен.</span><span class="sxs-lookup"><span data-stu-id="4fc36-126">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

</dd> <dt>

<span data-ttu-id="4fc36-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4fc36-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc36-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4fc36-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fc36-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4fc36-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fc36-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4fc36-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4fc36-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="4fc36-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="4fc36-132">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*"</span><span class="sxs-lookup"><span data-stu-id="4fc36-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fc36-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4fc36-133">Requirements</span></span>



| <span data-ttu-id="4fc36-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4fc36-134">Requirement</span></span> | <span data-ttu-id="4fc36-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4fc36-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc36-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4fc36-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc36-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4fc36-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fc36-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4fc36-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc36-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4fc36-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4fc36-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4fc36-140">Namespace</span></span><br/>                | <span data-ttu-id="4fc36-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4fc36-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4fc36-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4fc36-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fc36-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fc36-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fc36-144">DLL</span><span class="sxs-lookup"><span data-stu-id="4fc36-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fc36-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fc36-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc36-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4fc36-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc36-147">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="4fc36-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

