---
title: Класс MDM_VPNv2_Manual03
description: MDM \_ Поддержка vpnv2 \_ Manual03class — это необязательный узел, содержащий параметры ручного сервера.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- Класс MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989218"
---
# <a name="mdm_vpnv2_manual03-class"></a><span data-ttu-id="113a0-105">\_Класс MDM поддержка vpnv2 \_ Manual03</span><span class="sxs-lookup"><span data-stu-id="113a0-105">MDM\_VPNv2\_Manual03 class</span></span>

<span data-ttu-id="113a0-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="113a0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="113a0-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="113a0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="113a0-108">Класс **MDM \_ Поддержка vpnv2 \_ Manual03** является дополнительным узлом, содержащим параметры ручного сервера.</span><span class="sxs-lookup"><span data-stu-id="113a0-108">The **MDM\_VPNv2\_Manual03** class is an optional node containing the manual server settings.</span></span>

<span data-ttu-id="113a0-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="113a0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="113a0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="113a0-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a><span data-ttu-id="113a0-111">Члены</span><span class="sxs-lookup"><span data-stu-id="113a0-111">Members</span></span>

<span data-ttu-id="113a0-112">Класс **MDM \_ Поддержка vpnv2 \_ Manual03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="113a0-112">The **MDM\_VPNv2\_Manual03** class has these types of members:</span></span>

-   [<span data-ttu-id="113a0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="113a0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="113a0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="113a0-114">Properties</span></span>

<span data-ttu-id="113a0-115">Класс **MDM \_ Поддержка vpnv2 \_ Manual03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="113a0-115">The **MDM\_VPNv2\_Manual03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="113a0-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="113a0-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="113a0-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="113a0-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="113a0-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="113a0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="113a0-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="113a0-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="113a0-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="113a0-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="113a0-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="113a0-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="113a0-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="113a0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="113a0-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="113a0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="113a0-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="113a0-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="113a0-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="113a0-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="113a0-126">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/прокси/"</span><span class="sxs-lookup"><span data-stu-id="113a0-126">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span></span>

</dd> <dt>

[<span data-ttu-id="113a0-127">Server</span><span class="sxs-lookup"><span data-stu-id="113a0-127">Server</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

<span data-ttu-id="113a0-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="113a0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="113a0-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="113a0-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="113a0-130">Требования</span><span class="sxs-lookup"><span data-stu-id="113a0-130">Requirements</span></span>



| <span data-ttu-id="113a0-131">Требование</span><span class="sxs-lookup"><span data-stu-id="113a0-131">Requirement</span></span> | <span data-ttu-id="113a0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="113a0-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="113a0-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="113a0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="113a0-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="113a0-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="113a0-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="113a0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="113a0-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="113a0-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="113a0-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="113a0-137">Namespace</span></span><br/>                | <span data-ttu-id="113a0-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="113a0-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="113a0-139">MOF</span><span class="sxs-lookup"><span data-stu-id="113a0-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="113a0-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="113a0-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="113a0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="113a0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="113a0-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="113a0-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="113a0-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="113a0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113a0-144">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="113a0-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

