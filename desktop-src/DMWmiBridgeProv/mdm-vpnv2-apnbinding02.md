---
title: Класс MDM_VPNv2_APNBinding02
description: Зарезервировано для будущего использования. | Класс MDM_VPNv2_APNBinding02
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- Класс MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4447d1403903c9633523466504817338db969f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352402"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a><span data-ttu-id="c038c-106">\_Класс MDM поддержка vpnv2 \_ APNBinding02</span><span class="sxs-lookup"><span data-stu-id="c038c-106">MDM\_VPNv2\_APNBinding02 class</span></span>

<span data-ttu-id="c038c-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c038c-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c038c-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c038c-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c038c-109">Зарезервировано для будущего использования</span><span class="sxs-lookup"><span data-stu-id="c038c-109">Reserved for Future Use</span></span>

<span data-ttu-id="c038c-110">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c038c-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c038c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c038c-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a><span data-ttu-id="c038c-112">Члены</span><span class="sxs-lookup"><span data-stu-id="c038c-112">Members</span></span>

<span data-ttu-id="c038c-113">Класс **MDM \_ Поддержка vpnv2 \_ APNBinding02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c038c-113">The **MDM\_VPNv2\_APNBinding02** class has these types of members:</span></span>

-   [<span data-ttu-id="c038c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c038c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c038c-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="c038c-115">Properties</span></span>

<span data-ttu-id="c038c-116">Класс **MDM \_ Поддержка vpnv2 \_ APNBinding02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c038c-116">The **MDM\_VPNv2\_APNBinding02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c038c-117">акцесспоинтнаме</span><span class="sxs-lookup"><span data-stu-id="c038c-117">AccessPointName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c038c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c038c-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c038c-120">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c038c-120">AuthenticationType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c038c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c038c-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c038c-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c038c-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c038c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c038c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c038c-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c038c-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c038c-127">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="c038c-127">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="c038c-128">искомпрессионенаблед</span><span class="sxs-lookup"><span data-stu-id="c038c-128">IsCompressionEnabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c038c-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c038c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c038c-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c038c-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c038c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c038c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c038c-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c038c-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c038c-135">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="c038c-135">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="c038c-136">Пароль</span><span class="sxs-lookup"><span data-stu-id="c038c-136">Password</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c038c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c038c-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c038c-139">ProviderId</span><span class="sxs-lookup"><span data-stu-id="c038c-139">ProviderId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c038c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c038c-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c038c-142">UserName</span><span class="sxs-lookup"><span data-stu-id="c038c-142">UserName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c038c-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c038c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c038c-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c038c-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c038c-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c038c-145">Requirements</span></span>



| <span data-ttu-id="c038c-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c038c-146">Requirement</span></span> | <span data-ttu-id="c038c-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c038c-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c038c-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c038c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c038c-149">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c038c-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c038c-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c038c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c038c-151">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c038c-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c038c-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c038c-152">Namespace</span></span><br/>                | <span data-ttu-id="c038c-153">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c038c-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c038c-154">MOF</span><span class="sxs-lookup"><span data-stu-id="c038c-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c038c-155"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c038c-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c038c-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c038c-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c038c-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c038c-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c038c-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c038c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c038c-159">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="c038c-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

