---
title: Класс MDM_EnterpriseModernAppManagement_AppManagement01
description: Класс MDM \_ ентерприсемодернаппманажемент \_ AppManagement01 запускает центр обновления Windows Scan и сообщает о последней ошибке сканирования.
ms.assetid: f579a7c9-2e98-4e34-b45b-db8a4d553c57
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01
- MDM_EnterpriseModernAppManagement_AppManagement01.InstanceID
- MDM_EnterpriseModernAppManagement_AppManagement01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1f2a3739fe16d4a13e409d7d152645d4653336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262202"
---
# <a name="mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="4a625-105">\_Класс MDM ентерприсемодернаппманажемент \_ AppManagement01</span><span class="sxs-lookup"><span data-stu-id="4a625-105">MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="4a625-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4a625-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4a625-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4a625-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4a625-108">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** запускает центр обновления Windows Scan и сообщает о последней ошибке сканирования.</span><span class="sxs-lookup"><span data-stu-id="4a625-108">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class starts the Windows Update scan and reports the last scan error.</span></span>

<span data-ttu-id="4a625-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4a625-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a625-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a625-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppManagement01
{
  string InstanceID;
  string ParentID;
  sint32 LastScanError;
  string AppInventoryQuery;
  string AppInventoryResults;
  string RemovePackage;
};
```

## <a name="members"></a><span data-ttu-id="4a625-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4a625-111">Members</span></span>

<span data-ttu-id="4a625-112">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4a625-112">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these types of members:</span></span>

-   [<span data-ttu-id="4a625-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4a625-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="4a625-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4a625-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4a625-115">Методы</span><span class="sxs-lookup"><span data-stu-id="4a625-115">Methods</span></span>

<span data-ttu-id="4a625-116">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4a625-116">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these methods.</span></span>



| <span data-ttu-id="4a625-117">Метод</span><span class="sxs-lookup"><span data-stu-id="4a625-117">Method</span></span>                                                                                               | <span data-ttu-id="4a625-118">Описание</span><span class="sxs-lookup"><span data-stu-id="4a625-118">Description</span></span>                                             |
|:-----------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="4a625-119">**ремовепаккажемесод**</span><span class="sxs-lookup"><span data-stu-id="4a625-119">**RemovePackageMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-removepackagemethod.md) | <span data-ttu-id="4a625-120">Метод удаления пакетов.</span><span class="sxs-lookup"><span data-stu-id="4a625-120">Method for removing packages.</span></span><br/>                |
| [<span data-ttu-id="4a625-121">**упдатесканмесод**</span><span class="sxs-lookup"><span data-stu-id="4a625-121">**UpdateScanMethod**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01-updatescanmethod.md)       | <span data-ttu-id="4a625-122">Метод для запуска сканирования Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="4a625-122">Method for starting the Windows Update scan.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4a625-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="4a625-123">Properties</span></span>

<span data-ttu-id="4a625-124">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppManagement01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4a625-124">The **MDM\_EnterpriseModernAppManagement\_AppManagement01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4a625-125">аппинвенторикуери</span><span class="sxs-lookup"><span data-stu-id="4a625-125">AppInventoryQuery</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryquery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a625-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a625-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a625-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4a625-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4a625-128">аппинвенториресултс</span><span class="sxs-lookup"><span data-stu-id="4a625-128">AppInventoryResults</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-appinventoryresults)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a625-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a625-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a625-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4a625-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4a625-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4a625-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a625-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a625-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a625-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a625-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a625-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4a625-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4a625-135">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="4a625-135">Identifies the name of the parent node.</span></span> <span data-ttu-id="4a625-136">Для этого класса строка имеет значение "Аппманажемент".</span><span class="sxs-lookup"><span data-stu-id="4a625-136">For this class, the string is "AppManagement".</span></span>

</dd> <dt>

[<span data-ttu-id="4a625-137">ластсканеррор</span><span class="sxs-lookup"><span data-stu-id="4a625-137">LastScanError</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-lastscanerror)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a625-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4a625-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a625-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4a625-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4a625-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4a625-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a625-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a625-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a625-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a625-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a625-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4a625-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4a625-144">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="4a625-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="4a625-145">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/"</span><span class="sxs-lookup"><span data-stu-id="4a625-145">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/"</span></span>

</dd> <dt>

[<span data-ttu-id="4a625-146">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="4a625-146">RemovePackage</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp#appmanagement-removepackage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a625-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a625-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a625-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4a625-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a625-149">Требования</span><span class="sxs-lookup"><span data-stu-id="4a625-149">Requirements</span></span>



| <span data-ttu-id="4a625-150">Требование</span><span class="sxs-lookup"><span data-stu-id="4a625-150">Requirement</span></span> | <span data-ttu-id="4a625-151">Значение</span><span class="sxs-lookup"><span data-stu-id="4a625-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a625-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a625-152">Minimum supported client</span></span><br/> | <span data-ttu-id="4a625-153">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4a625-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4a625-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a625-154">Minimum supported server</span></span><br/> | <span data-ttu-id="4a625-155">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4a625-155">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4a625-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4a625-156">Namespace</span></span><br/>                | <span data-ttu-id="4a625-157">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4a625-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4a625-158">MOF</span><span class="sxs-lookup"><span data-stu-id="4a625-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a625-159"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a625-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a625-160">DLL</span><span class="sxs-lookup"><span data-stu-id="4a625-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a625-161"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a625-161"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a625-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a625-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a625-163">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="4a625-163">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

