---
title: Класс MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Класс MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01 используется для установки приложений из Магазина Windows или из размещенного расположения.
ms.assetid: fc4c4c82-6f43-41fc-863b-940c0517f28b
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.InstanceID
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6cd3fc5478e73df5276fdc9d6a1d66c9649dd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989051"
---
# <a name="mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="4c4ea-105">\_Класс MDM ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="4c4ea-105">MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="4c4ea-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4c4ea-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4c4ea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4c4ea-108">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** используется для установки приложений из Магазина Windows или из размещенного расположения.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-108">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class is used to install apps from the Windows Store or a hosted location.</span></span>

<span data-ttu-id="4c4ea-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4ea-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c4ea-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppInstallation01_01
{
  string InstanceID;
  string ParentID;
  sint32 LastError;
  string LastErrorDesc;
  sint32 Status;
  sint32 ProgressStatus;
};
```

## <a name="members"></a><span data-ttu-id="4c4ea-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4c4ea-111">Members</span></span>

<span data-ttu-id="4c4ea-112">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4c4ea-112">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="4c4ea-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4c4ea-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="4c4ea-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c4ea-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4c4ea-115">Методы</span><span class="sxs-lookup"><span data-stu-id="4c4ea-115">Methods</span></span>

<span data-ttu-id="4c4ea-116">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-116">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these methods.</span></span>



| <span data-ttu-id="4c4ea-117">Метод</span><span class="sxs-lookup"><span data-stu-id="4c4ea-117">Method</span></span>                                                                                                    | <span data-ttu-id="4c4ea-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4c4ea-118">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4c4ea-119">**хостединсталлмесод**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-119">**HostedInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-hostedinstallmethod.md) | <span data-ttu-id="4c4ea-120">Метод для выполнения установки пакета приложения из размещенного расположения (это может быть локальный диск, UNC-источник данных или HTTPS).</span><span class="sxs-lookup"><span data-stu-id="4c4ea-120">Method to perform an install of an app package from a hosted location (this can be a local drive, a UNC, or https data source).</span></span><br/> |
| [<span data-ttu-id="4c4ea-121">**стореинсталлмесод**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-121">**StoreInstallMethod**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01-storeinstallmethod.md)   | <span data-ttu-id="4c4ea-122">Метод для выполнения установки приложения и лицензии из Магазина Windows.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-122">Method to perform an install of an app and a license from the Windows Store.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="4c4ea-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c4ea-123">Properties</span></span>

<span data-ttu-id="4c4ea-124">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-124">The **MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c4ea-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4ea-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c4ea-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c4ea-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c4ea-129">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="4c4ea-130">Для этого класса строка имеет значение "Аппинсталлатион".</span><span class="sxs-lookup"><span data-stu-id="4c4ea-130">For this class, the string is "AppInstallation".</span></span>

</dd> <dt>

[<span data-ttu-id="4c4ea-131">LastError</span><span class="sxs-lookup"><span data-stu-id="4c4ea-131">LastError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-lasterror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4ea-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4c4ea-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4c4ea-134">ластеррордеск</span><span class="sxs-lookup"><span data-stu-id="4c4ea-134">LastErrorDesc</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4ea-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4c4ea-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4c4ea-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4ea-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c4ea-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4c4ea-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4c4ea-141">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="4c4ea-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="4c4ea-142">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/аппинсталлатион"</span><span class="sxs-lookup"><span data-stu-id="4c4ea-142">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppInstallation"</span></span>

</dd> <dt>

[<span data-ttu-id="4c4ea-143">прогрессстатус</span><span class="sxs-lookup"><span data-stu-id="4c4ea-143">ProgressStatus</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4ea-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4c4ea-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4c4ea-146">Состояние</span><span class="sxs-lookup"><span data-stu-id="4c4ea-146">Status</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appinstallation-packagefamilyname-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c4ea-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4c4ea-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c4ea-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4c4ea-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c4ea-149">Требования</span><span class="sxs-lookup"><span data-stu-id="4c4ea-149">Requirements</span></span>



| <span data-ttu-id="4c4ea-150">Требование</span><span class="sxs-lookup"><span data-stu-id="4c4ea-150">Requirement</span></span> | <span data-ttu-id="4c4ea-151">Значение</span><span class="sxs-lookup"><span data-stu-id="4c4ea-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4ea-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c4ea-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4ea-153">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4c4ea-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c4ea-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c4ea-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4ea-155">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4c4ea-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4c4ea-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4c4ea-156">Namespace</span></span><br/>                | <span data-ttu-id="4c4ea-157">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4c4ea-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4c4ea-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4c4ea-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c4ea-159"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c4ea-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c4ea-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4c4ea-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c4ea-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c4ea-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c4ea-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c4ea-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4ea-163">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="4c4ea-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

