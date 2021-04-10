---
title: Класс MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Класс MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01 используется для управления лицензиями для приложений Магазина.
ms.assetid: 9fdcba35-6c21-4a39-99f4-470acf7d35bb
keywords:
- Класс MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.InstanceID
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a4549ba473afaf76bea3f23ec65aacf301121a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071847"
---
# <a name="mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="00d2e-105">\_Класс MDM ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="00d2e-105">MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="00d2e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="00d2e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="00d2e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="00d2e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="00d2e-108">Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** используется для управления лицензиями для приложений Магазина.</span><span class="sxs-lookup"><span data-stu-id="00d2e-108">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class is used to manage licenses for store apps.</span></span>

<span data-ttu-id="00d2e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="00d2e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d2e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00d2e-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_StoreLicenses02_01
{
  string InstanceID;
  string ParentID;
  string LicenseCategory;
  string LicenseUsage;
  string RequesterID;
};
```

## <a name="members"></a><span data-ttu-id="00d2e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="00d2e-111">Members</span></span>

<span data-ttu-id="00d2e-112">Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="00d2e-112">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="00d2e-113">Методы</span><span class="sxs-lookup"><span data-stu-id="00d2e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="00d2e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="00d2e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="00d2e-115">Методы</span><span class="sxs-lookup"><span data-stu-id="00d2e-115">Methods</span></span>

<span data-ttu-id="00d2e-116">Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="00d2e-116">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these methods.</span></span>



| <span data-ttu-id="00d2e-117">Метод</span><span class="sxs-lookup"><span data-stu-id="00d2e-117">Method</span></span>                                                                                                              | <span data-ttu-id="00d2e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="00d2e-118">Description</span></span>                                             |
|:--------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="00d2e-119">**аддлиценсемесод**</span><span class="sxs-lookup"><span data-stu-id="00d2e-119">**AddLicenseMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-addlicensemethod.md)                   | <span data-ttu-id="00d2e-120">Метод добавления лицензии.</span><span class="sxs-lookup"><span data-stu-id="00d2e-120">Method for adding a license.</span></span><br/>                 |
| [<span data-ttu-id="00d2e-121">**жетлиценсефромсторемесод**</span><span class="sxs-lookup"><span data-stu-id="00d2e-121">**GetLicenseFromStoreMethod**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01-getlicensefromstoremethod.md) | <span data-ttu-id="00d2e-122">Метод получения лицензии из магазина.</span><span class="sxs-lookup"><span data-stu-id="00d2e-122">Method for getting a license from the store.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="00d2e-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="00d2e-123">Properties</span></span>

<span data-ttu-id="00d2e-124">Класс **MDM \_ ентерприсемодернаппманажемент \_ StoreLicenses02 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="00d2e-124">The **MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00d2e-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="00d2e-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00d2e-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00d2e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00d2e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00d2e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00d2e-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00d2e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="00d2e-129">Необязательный узел.</span><span class="sxs-lookup"><span data-stu-id="00d2e-129">Optional node.</span></span> <span data-ttu-id="00d2e-130">Идентификатор лицензии для хранилища установленного приложения.</span><span class="sxs-lookup"><span data-stu-id="00d2e-130">License ID for a store installed app.</span></span> <span data-ttu-id="00d2e-131">Идентификатор лицензии обычно является PFNом приложения.</span><span class="sxs-lookup"><span data-stu-id="00d2e-131">The license ID is generally the PFN of the app.</span></span>

<span data-ttu-id="00d2e-132">Поддерживаются операции добавления, получения и удаления.</span><span class="sxs-lookup"><span data-stu-id="00d2e-132">Supported operations are Add, Get, and Delete.</span></span>

</dd> <dt>

[<span data-ttu-id="00d2e-133">лиценсекатегори</span><span class="sxs-lookup"><span data-stu-id="00d2e-133">LicenseCategory</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licensecategory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00d2e-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00d2e-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00d2e-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="00d2e-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="00d2e-136">лиценсеусаже</span><span class="sxs-lookup"><span data-stu-id="00d2e-136">LicenseUsage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-licenseusage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00d2e-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00d2e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00d2e-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="00d2e-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="00d2e-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="00d2e-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00d2e-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00d2e-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00d2e-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="00d2e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00d2e-142">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="00d2e-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="00d2e-143">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="00d2e-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="00d2e-144">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/апплиценсес/сторелиценсес"</span><span class="sxs-lookup"><span data-stu-id="00d2e-144">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppLicenses/StoreLicenses"</span></span>

</dd> <dt>

[<span data-ttu-id="00d2e-145">рекуестерид</span><span class="sxs-lookup"><span data-stu-id="00d2e-145">RequesterID</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#applicenses-storelicenses-licenseid-requesterid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="00d2e-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="00d2e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00d2e-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="00d2e-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00d2e-148">Требования</span><span class="sxs-lookup"><span data-stu-id="00d2e-148">Requirements</span></span>



| <span data-ttu-id="00d2e-149">Требование</span><span class="sxs-lookup"><span data-stu-id="00d2e-149">Requirement</span></span> | <span data-ttu-id="00d2e-150">Значение</span><span class="sxs-lookup"><span data-stu-id="00d2e-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d2e-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00d2e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="00d2e-152">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="00d2e-152">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00d2e-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00d2e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="00d2e-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="00d2e-154">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="00d2e-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="00d2e-155">Namespace</span></span><br/>                | <span data-ttu-id="00d2e-156">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="00d2e-156">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="00d2e-157">MOF</span><span class="sxs-lookup"><span data-stu-id="00d2e-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00d2e-158"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00d2e-158"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="00d2e-159">DLL</span><span class="sxs-lookup"><span data-stu-id="00d2e-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d2e-160"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d2e-160"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d2e-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00d2e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d2e-162">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="00d2e-162">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

