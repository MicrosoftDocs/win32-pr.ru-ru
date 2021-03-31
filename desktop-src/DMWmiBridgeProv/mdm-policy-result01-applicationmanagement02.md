---
title: Класс MDM_Policy_Result01_ApplicationManagement02
description: '\_Класс политики MDM \_ Result01 \_ ApplicationManagement02 представляет доступные политики управления приложениями. \_Класс политики MDM \_ Result01 \_ ApplicationManagement02 представляет доступные политики управления приложениями.'
ms.assetid: 141614e4-b2b1-49d9-879c-f6f86bee070c
keywords:
- Класс MDM_Policy_Result01_ApplicationManagement02
- MDM_Policy_Result01_ApplicationManagement02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationManagement02
- MDM_Policy_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477e4e58216c912aa14ec17b8e5879643e3de83f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136031"
---
# <a name="mdm_policy_result01_applicationmanagement02-class"></a><span data-ttu-id="62c93-105">\_Класс политики MDM \_ Result01 \_ ApplicationManagement02</span><span class="sxs-lookup"><span data-stu-id="62c93-105">MDM\_Policy\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="62c93-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="62c93-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="62c93-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="62c93-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="62c93-108">Класс **\_ политики MDM \_ Result01 \_ ApplicationManagement02** представляет доступные политики управления приложениями.</span><span class="sxs-lookup"><span data-stu-id="62c93-108">The **MDM\_Policy\_Result01\_ApplicationManagement02** class represents the application management policies available.</span></span>

<span data-ttu-id="62c93-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="62c93-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c93-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62c93-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a><span data-ttu-id="62c93-111">Члены</span><span class="sxs-lookup"><span data-stu-id="62c93-111">Members</span></span>

<span data-ttu-id="62c93-112">Класс **\_ политики MDM \_ Result01 \_ ApplicationManagement02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62c93-112">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="62c93-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="62c93-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62c93-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="62c93-114">Properties</span></span>

<span data-ttu-id="62c93-115">Класс **\_ политики MDM \_ Result01 \_ ApplicationManagement02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="62c93-115">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="62c93-116">AllowAllTrustedApps</span><span class="sxs-lookup"><span data-stu-id="62c93-116">AllowAllTrustedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62c93-119">AllowAppStoreAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="62c93-119">AllowAppStoreAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62c93-122">AllowDeveloperUnlock</span><span class="sxs-lookup"><span data-stu-id="62c93-122">AllowDeveloperUnlock</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62c93-125">AllowGameDVR</span><span class="sxs-lookup"><span data-stu-id="62c93-125">AllowGameDVR</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62c93-128">AllowSharedUserAppData</span><span class="sxs-lookup"><span data-stu-id="62c93-128">AllowSharedUserAppData</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62c93-131">дисаблестореоригинатедаппс</span><span class="sxs-lookup"><span data-stu-id="62c93-131">DisableStoreOriginatedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="62c93-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="62c93-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62c93-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62c93-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62c93-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62c93-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="62c93-138">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="62c93-138">Identifies the name of the parent node.</span></span> <span data-ttu-id="62c93-139">Для этого класса строка имеет значение "Аппликатионманажемент".</span><span class="sxs-lookup"><span data-stu-id="62c93-139">For this class, the string is "ApplicationManagement".</span></span>

</dd> <dt>

<span data-ttu-id="62c93-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="62c93-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62c93-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62c93-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62c93-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62c93-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="62c93-144">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="62c93-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="62c93-145">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="62c93-145">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="62c93-146">RestrictAppDataToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="62c93-146">RestrictAppDataToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="62c93-149">RestrictAppToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="62c93-149">RestrictAppToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62c93-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="62c93-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="62c93-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62c93-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62c93-152">Требования</span><span class="sxs-lookup"><span data-stu-id="62c93-152">Requirements</span></span>



| <span data-ttu-id="62c93-153">Требование</span><span class="sxs-lookup"><span data-stu-id="62c93-153">Requirement</span></span> | <span data-ttu-id="62c93-154">Значение</span><span class="sxs-lookup"><span data-stu-id="62c93-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c93-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62c93-155">Minimum supported client</span></span><br/> | <span data-ttu-id="62c93-156">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="62c93-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62c93-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62c93-157">Minimum supported server</span></span><br/> | <span data-ttu-id="62c93-158">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62c93-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="62c93-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62c93-159">Namespace</span></span><br/>                | <span data-ttu-id="62c93-160">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="62c93-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="62c93-161">MOF</span><span class="sxs-lookup"><span data-stu-id="62c93-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62c93-162"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62c93-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="62c93-163">DLL</span><span class="sxs-lookup"><span data-stu-id="62c93-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c93-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c93-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c93-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62c93-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c93-166">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="62c93-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

