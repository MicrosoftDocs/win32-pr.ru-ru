---
title: Класс MDM_EnterpriseModernAppManagement_AppManagement01_03
description: Класс MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 03 предоставляет конкретные сведения о приложении, такие как имя, версия и издатель.
ms.assetid: 424e68de-1411-490f-b33b-5243ffa5a31e
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01_03
- MDM_EnterpriseModernAppManagement_AppManagement01_03.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01_03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f24c028c6a1f0d551fc54cb078376dcdef968abc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136770"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01_03-class"></a><span data-ttu-id="1e3ac-105">\_Класс MDM ентерприсемодернаппманажемент \_ AppManagement01 \_ 03</span><span class="sxs-lookup"><span data-stu-id="1e3ac-105">MDM\_EnterpriseModernAppManagement\_AppManagement01\_03 class</span></span>

<span data-ttu-id="1e3ac-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1e3ac-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1e3ac-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1e3ac-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1e3ac-108">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 03** предоставляет конкретные сведения о приложении, такие как имя, версия и издатель.</span><span class="sxs-lookup"><span data-stu-id="1e3ac-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class provides specific information about the app, such as name, version, and publisher.</span></span>

<span data-ttu-id="1e3ac-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1e3ac-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e3ac-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e3ac-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01_03
{
  string InstanceID;
  string ParentID;
  string Name;
  string Version;
  string Publisher;
  string Architecture;
  string InstallLocation;
  sint32 IsFramework;
  sint32 IsBundle;
  string InstallDate;
  string ResourceID;
  sint32 PackageStatus;
  sint32 RequiresReinstall;
  string Users;
  sint32 IsProvisioned;
};
```

## <a name="members"></a><span data-ttu-id="1e3ac-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1e3ac-111">Members</span></span>

<span data-ttu-id="1e3ac-112">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1e3ac-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these types of members:</span></span>

-   [<span data-ttu-id="1e3ac-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1e3ac-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e3ac-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1e3ac-114">Properties</span></span>

<span data-ttu-id="1e3ac-115">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 \_ 03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1e3ac-115">The **MDM\_EnterpriseModernAppManagement\_AppManagement01\_03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1e3ac-116">Архитектура</span><span class="sxs-lookup"><span data-stu-id="1e3ac-116">Architecture</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-architecture)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-119">InstallDate</span><span class="sxs-lookup"><span data-stu-id="1e3ac-119">InstallDate</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-122">InstallLocation</span><span class="sxs-lookup"><span data-stu-id="1e3ac-122">InstallLocation</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-installlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e3ac-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e3ac-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e3ac-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e3ac-129">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="1e3ac-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="1e3ac-130">Для этого класса строка является экземпляром полного имени пакета.</span><span class="sxs-lookup"><span data-stu-id="1e3ac-130">For this class, the string is the instance of the package full name.</span></span>

</dd> <dt>

[<span data-ttu-id="1e3ac-131">Набор</span><span class="sxs-lookup"><span data-stu-id="1e3ac-131">IsBundle</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isbundle)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-134">Платформа</span><span class="sxs-lookup"><span data-stu-id="1e3ac-134">IsFramework</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isframework)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-137">Подготавливается</span><span class="sxs-lookup"><span data-stu-id="1e3ac-137">IsProvisioned</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-isprovisioned)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-140">Name</span><span class="sxs-lookup"><span data-stu-id="1e3ac-140">Name</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-143">паккажестатус</span><span class="sxs-lookup"><span data-stu-id="1e3ac-143">PackageStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-packagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1e3ac-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1e3ac-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-149">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e3ac-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e3ac-150">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="1e3ac-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="1e3ac-151">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/аппманажемент/*EnterpriseID* / *паккажефамилинаме*"</span><span class="sxs-lookup"><span data-stu-id="1e3ac-151">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/*EnterpriseID*/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="1e3ac-152">Издатель</span><span class="sxs-lookup"><span data-stu-id="1e3ac-152">Publisher</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-publisher)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-155">рекуиресреинсталл</span><span class="sxs-lookup"><span data-stu-id="1e3ac-155">RequiresReinstall</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-requiresreinstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-158">ResourceID</span><span class="sxs-lookup"><span data-stu-id="1e3ac-158">ResourceID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-resourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-161">Пользователи</span><span class="sxs-lookup"><span data-stu-id="1e3ac-161">Users</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-users)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1e3ac-164">Version</span><span class="sxs-lookup"><span data-stu-id="1e3ac-164">Version</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#----packagefamilyname-packagefullname-version)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e3ac-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1e3ac-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e3ac-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1e3ac-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e3ac-167">Требования</span><span class="sxs-lookup"><span data-stu-id="1e3ac-167">Requirements</span></span>



| <span data-ttu-id="1e3ac-168">Требование</span><span class="sxs-lookup"><span data-stu-id="1e3ac-168">Requirement</span></span> | <span data-ttu-id="1e3ac-169">Значение</span><span class="sxs-lookup"><span data-stu-id="1e3ac-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e3ac-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e3ac-170">Minimum supported client</span></span><br/> | <span data-ttu-id="1e3ac-171">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1e3ac-171">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e3ac-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e3ac-172">Minimum supported server</span></span><br/> | <span data-ttu-id="1e3ac-173">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1e3ac-173">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1e3ac-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1e3ac-174">Namespace</span></span><br/>                | <span data-ttu-id="1e3ac-175">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1e3ac-175">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1e3ac-176">MOF</span><span class="sxs-lookup"><span data-stu-id="1e3ac-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e3ac-177"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e3ac-177"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e3ac-178">DLL</span><span class="sxs-lookup"><span data-stu-id="1e3ac-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e3ac-179"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e3ac-179"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e3ac-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e3ac-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e3ac-181">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="1e3ac-181">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

