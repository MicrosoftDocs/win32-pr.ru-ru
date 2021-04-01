---
title: Класс MDM_EnterpriseModernAppManagement_AppSettingPolicy04
description: Класс MDM \_ ентерприсемодернаппманажемент \_ AppSettingPolicy04 задает все значения параметров управляемого приложения.
ms.assetid: 65e2d2aa-31fd-4733-a1f7-8a572700a562
keywords:
- Класс MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.InstanceID
- MDM_EnterpriseModernAppManagement_AppSettingPolicy04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc9003ea7c9106f177958f7a15def3c60393346b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071848"
---
# <a name="mdm_enterprisemodernappmanagement_appsettingpolicy04-class"></a><span data-ttu-id="44fa5-105">\_Класс MDM ентерприсемодернаппманажемент \_ AppSettingPolicy04</span><span class="sxs-lookup"><span data-stu-id="44fa5-105">MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04 class</span></span>

<span data-ttu-id="44fa5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="44fa5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="44fa5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="44fa5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="44fa5-108">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppSettingPolicy04** задает все значения параметров управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="44fa5-108">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class specifies all managed app setting values.</span></span>

<span data-ttu-id="44fa5-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="44fa5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fa5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44fa5-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_EnterpriseModernAppManagement_AppSettingPolicy04
{
  string  InstanceID;
  string  ParentID;
  string  Value;
  boolean IsVariableLeaf;
};
```

## <a name="members"></a><span data-ttu-id="44fa5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="44fa5-111">Members</span></span>

<span data-ttu-id="44fa5-112">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppSettingPolicy04** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="44fa5-112">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these types of members:</span></span>

-   [<span data-ttu-id="44fa5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="44fa5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44fa5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="44fa5-114">Properties</span></span>

<span data-ttu-id="44fa5-115">Класс **MDM \_ ентерприсемодернаппманажемент \_ AppSettingPolicy04** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44fa5-115">The **MDM\_EnterpriseModernAppManagement\_AppSettingPolicy04** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44fa5-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="44fa5-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44fa5-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44fa5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44fa5-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44fa5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44fa5-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44fa5-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44fa5-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="44fa5-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="44fa5-121">Для этого класса это строка "Аппсеттингполици".</span><span class="sxs-lookup"><span data-stu-id="44fa5-121">For this class, the string "AppSettingPolicy".</span></span>

</dd> <dt>

[<span data-ttu-id="44fa5-122">исвариаблелеаф</span><span class="sxs-lookup"><span data-stu-id="44fa5-122">IsVariableLeaf</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="44fa5-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="44fa5-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44fa5-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44fa5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44fa5-125">Добавлено в Windows 10 версии 1511.</span><span class="sxs-lookup"><span data-stu-id="44fa5-125">Added in Windows 10, version 1511.</span></span> <span data-ttu-id="44fa5-126">**Сеттингвалуе** и данные представляют пару "ключ-значение", которая должна быть настроена для приложения.</span><span class="sxs-lookup"><span data-stu-id="44fa5-126">The **SettingValue** and data represent a key value pair to be configured for the app.</span></span> <span data-ttu-id="44fa5-127">Узел представляет имя ключа, а данные — значение.</span><span class="sxs-lookup"><span data-stu-id="44fa5-127">The node represents the name of the key and the data represents the value.</span></span> <span data-ttu-id="44fa5-128">Это значение можно найти в LocalSettings в контейнере Managed. app. Settings.</span><span class="sxs-lookup"><span data-stu-id="44fa5-128">You can find this value in LocalSettings in the Managed.App.Settings container.</span></span>

<span data-ttu-id="44fa5-129">Этот параметр работает только для приложений, поддерживающих эту функцию, и поддерживается только в контексте пользователя.</span><span class="sxs-lookup"><span data-stu-id="44fa5-129">This setting only works for apps that support the feature and it is only supported in the user context.</span></span>

</dd> <dt>

<span data-ttu-id="44fa5-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="44fa5-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44fa5-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44fa5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44fa5-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44fa5-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44fa5-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44fa5-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44fa5-134">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="44fa5-134">Describes the full path to the parent node.</span></span> <span data-ttu-id="44fa5-135">Для этого класса строка имеет значение "./вендор/мсфт/ентерприсемодернаппманажемент/аппманажемент/аппсторе/*паккажефамилинаме*"</span><span class="sxs-lookup"><span data-stu-id="44fa5-135">For this class, the string is "./Vendor/MSFT/EnterpriseModernAppManagement/AppManagement/AppStore/*PackageFamilyName*"</span></span>

</dd> <dt>

[<span data-ttu-id="44fa5-136">**Значение**</span><span class="sxs-lookup"><span data-stu-id="44fa5-136">**Value**</span></span>](/windows/client-management/mdm/enterprisemodernappmanagement-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="44fa5-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44fa5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44fa5-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="44fa5-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44fa5-139">Требования</span><span class="sxs-lookup"><span data-stu-id="44fa5-139">Requirements</span></span>



| <span data-ttu-id="44fa5-140">Требование</span><span class="sxs-lookup"><span data-stu-id="44fa5-140">Requirement</span></span> | <span data-ttu-id="44fa5-141">Значение</span><span class="sxs-lookup"><span data-stu-id="44fa5-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44fa5-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44fa5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="44fa5-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="44fa5-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44fa5-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44fa5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="44fa5-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="44fa5-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="44fa5-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="44fa5-146">Namespace</span></span><br/>                | <span data-ttu-id="44fa5-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="44fa5-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="44fa5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="44fa5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44fa5-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44fa5-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="44fa5-150">DLL</span><span class="sxs-lookup"><span data-stu-id="44fa5-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44fa5-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44fa5-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44fa5-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44fa5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fa5-153">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="44fa5-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

