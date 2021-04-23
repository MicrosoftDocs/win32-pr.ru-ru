---
title: Класс MDM_EnterpriseAPN_01
description: Класс MDM \_ EnterpriseAPN \_ 01 используется предприятием для предоставления точки доступа к Интернету.
ms.assetid: c5fc0a86-98b7-4d0c-aae5-be836e48eee7
keywords:
- Класс MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseAPN_01
- MDM_EnterpriseAPN_01.InstanceID
- MDM_EnterpriseAPN_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bf8b9563b2f681e71e355f4c21aa097eedf64a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262204"
---
# <a name="mdm_enterpriseapn_01-class"></a><span data-ttu-id="11f9f-105">\_Класс MDM EnterpriseAPN \_ 01</span><span class="sxs-lookup"><span data-stu-id="11f9f-105">MDM\_EnterpriseAPN\_01 class</span></span>

<span data-ttu-id="11f9f-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="11f9f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11f9f-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="11f9f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11f9f-108">Класс **MDM \_ EnterpriseAPN \_ 01** используется предприятием для предоставления точки доступа к Интернету.</span><span class="sxs-lookup"><span data-stu-id="11f9f-108">The **MDM\_EnterpriseAPN\_01** class is used by the enterprise to provision an APN for the Internet.</span></span>

<span data-ttu-id="11f9f-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="11f9f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f9f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11f9f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseAPN_01
{
  string  InstanceID;
  string  ParentID;
  string  APNName;
  string  IPType;
  boolean IsAttachAPN;
  string  ClassId;
  string  AuthType;
  string  UserName;
  string  Password;
  string  IccId;
  boolean AlwaysOn;
  boolean Enabled;
  string  Roaming;
};
```

## <a name="members"></a><span data-ttu-id="11f9f-111">Члены</span><span class="sxs-lookup"><span data-stu-id="11f9f-111">Members</span></span>

<span data-ttu-id="11f9f-112">Класс **MDM \_ EnterpriseAPN \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11f9f-112">The **MDM\_EnterpriseAPN\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="11f9f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="11f9f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11f9f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="11f9f-114">Properties</span></span>

<span data-ttu-id="11f9f-115">Класс **MDM \_ EnterpriseAPN \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="11f9f-115">The **MDM\_EnterpriseAPN\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="11f9f-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="11f9f-116">AlwaysOn</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="11f9f-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-119">APNName</span><span class="sxs-lookup"><span data-stu-id="11f9f-119">APNName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-apnname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-122">AuthType</span><span class="sxs-lookup"><span data-stu-id="11f9f-122">AuthType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-authtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-125">Класса</span><span class="sxs-lookup"><span data-stu-id="11f9f-125">ClassId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-classid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-128">Enabled</span><span class="sxs-lookup"><span data-stu-id="11f9f-128">Enabled</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="11f9f-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-131">IccId</span><span class="sxs-lookup"><span data-stu-id="11f9f-131">IccId</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iccid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11f9f-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11f9f-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11f9f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11f9f-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11f9f-138">Имя подключения, отображаемое диспетчером подключений Windows.</span><span class="sxs-lookup"><span data-stu-id="11f9f-138">Name of the connection as seen by Windows Connection Manager.</span></span>

</dd> <dt>

[<span data-ttu-id="11f9f-139">IPType</span><span class="sxs-lookup"><span data-stu-id="11f9f-139">IPType</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-iptype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-142">IsAttachAPN</span><span class="sxs-lookup"><span data-stu-id="11f9f-142">IsAttachAPN</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-isattachapn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="11f9f-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="11f9f-145">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="11f9f-145">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="11f9f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-148">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="11f9f-148">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="11f9f-149">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="11f9f-149">Describes the full path to the parent node.</span></span> <span data-ttu-id="11f9f-150">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсеапн"</span><span class="sxs-lookup"><span data-stu-id="11f9f-150">For this class, the string is "./Vendor/MSFT/EnterpriseAPN"</span></span>

</dd> <dt>

[<span data-ttu-id="11f9f-151">Пароль</span><span class="sxs-lookup"><span data-stu-id="11f9f-151">Password</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-154">Роуминге</span><span class="sxs-lookup"><span data-stu-id="11f9f-154">Roaming</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-roaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="11f9f-157">UserName</span><span class="sxs-lookup"><span data-stu-id="11f9f-157">UserName</span></span>](/windows/client-management/mdm/enterpriseapn-csp#enterpriseapn-connectionname-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="11f9f-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="11f9f-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11f9f-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="11f9f-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11f9f-160">Требования</span><span class="sxs-lookup"><span data-stu-id="11f9f-160">Requirements</span></span>



| <span data-ttu-id="11f9f-161">Требование</span><span class="sxs-lookup"><span data-stu-id="11f9f-161">Requirement</span></span> | <span data-ttu-id="11f9f-162">Значение</span><span class="sxs-lookup"><span data-stu-id="11f9f-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f9f-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11f9f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="11f9f-164">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="11f9f-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11f9f-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11f9f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="11f9f-166">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="11f9f-166">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="11f9f-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="11f9f-167">Namespace</span></span><br/>                | <span data-ttu-id="11f9f-168">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="11f9f-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="11f9f-169">MOF</span><span class="sxs-lookup"><span data-stu-id="11f9f-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11f9f-170"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11f9f-170"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11f9f-171">DLL</span><span class="sxs-lookup"><span data-stu-id="11f9f-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f9f-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f9f-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11f9f-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11f9f-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f9f-174">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="11f9f-174">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

