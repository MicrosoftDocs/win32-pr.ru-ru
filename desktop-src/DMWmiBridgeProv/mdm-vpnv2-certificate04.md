---
title: Класс MDM_VPNv2_Certificate04
description: Зарезервировано для будущего использования.
ms.assetid: 0fa831e0-918a-472f-88bf-7e40c4081417
keywords:
- Класс MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04.InstanceID
- MDM_VPNv2_Certificate04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88bd26e8dc9916e7e2db97b980065d7a8733ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988669"
---
# <a name="mdm_vpnv2_certificate04-class"></a><span data-ttu-id="6d0fa-105">\_Класс MDM поддержка vpnv2 \_ Certificate04</span><span class="sxs-lookup"><span data-stu-id="6d0fa-105">MDM\_VPNv2\_Certificate04 class</span></span>

<span data-ttu-id="6d0fa-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="6d0fa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6d0fa-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="6d0fa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6d0fa-108">Зарезервировано для будущего использования</span><span class="sxs-lookup"><span data-stu-id="6d0fa-108">Reserved for future Use</span></span>

<span data-ttu-id="6d0fa-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6d0fa-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0fa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d0fa-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Certificate04
{
  string InstanceID;
  string ParentID;
  string Issuer;
  string Eku;
};
```

## <a name="members"></a><span data-ttu-id="6d0fa-111">Члены</span><span class="sxs-lookup"><span data-stu-id="6d0fa-111">Members</span></span>

<span data-ttu-id="6d0fa-112">Класс **MDM \_ Поддержка vpnv2 \_ Certificate04** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6d0fa-112">The **MDM\_VPNv2\_Certificate04** class has these types of members:</span></span>

-   [<span data-ttu-id="6d0fa-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d0fa-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d0fa-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d0fa-114">Properties</span></span>

<span data-ttu-id="6d0fa-115">Класс **MDM \_ Поддержка vpnv2 \_ Certificate04** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d0fa-115">The **MDM\_VPNv2\_Certificate04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6d0fa-116">EKU</span><span class="sxs-lookup"><span data-stu-id="6d0fa-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d0fa-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d0fa-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d0fa-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d0fa-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6d0fa-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6d0fa-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d0fa-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d0fa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d0fa-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d0fa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d0fa-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d0fa-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6d0fa-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="6d0fa-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="6d0fa-124">Для этого класса строка имеет значение "EAP".</span><span class="sxs-lookup"><span data-stu-id="6d0fa-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

[<span data-ttu-id="6d0fa-125">Издатель</span><span class="sxs-lookup"><span data-stu-id="6d0fa-125">Issuer</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-issuer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d0fa-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d0fa-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d0fa-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d0fa-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6d0fa-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6d0fa-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d0fa-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d0fa-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d0fa-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d0fa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d0fa-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d0fa-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6d0fa-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="6d0fa-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="6d0fa-133">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*/нативепрофиле/аусентикатион"</span><span class="sxs-lookup"><span data-stu-id="6d0fa-133">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d0fa-134">Требования</span><span class="sxs-lookup"><span data-stu-id="6d0fa-134">Requirements</span></span>



| <span data-ttu-id="6d0fa-135">Требование</span><span class="sxs-lookup"><span data-stu-id="6d0fa-135">Requirement</span></span> | <span data-ttu-id="6d0fa-136">Значение</span><span class="sxs-lookup"><span data-stu-id="6d0fa-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0fa-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d0fa-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6d0fa-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6d0fa-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d0fa-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d0fa-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6d0fa-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d0fa-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6d0fa-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d0fa-141">Namespace</span></span><br/>                | <span data-ttu-id="6d0fa-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="6d0fa-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6d0fa-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6d0fa-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d0fa-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d0fa-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d0fa-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6d0fa-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d0fa-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d0fa-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0fa-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d0fa-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0fa-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="6d0fa-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

