---
title: Класс MDM_Policy_Result01_Bluetooth02
description: '\_Класс политики MDM \_ Result01 \_ Bluetooth02 представляет доступные политики управления Bluetooth.'
ms.assetid: 629f2323-f6f6-4d4f-8558-9553f4dbe871
keywords:
- Класс MDM_Policy_Result01_Bluetooth02
- MDM_Policy_Result01_Bluetooth02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Bluetooth02
- MDM_Policy_Result01_Bluetooth02.InstanceID
- MDM_Policy_Result01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ceb0a3b7a3d2440f9769fde72c01ce4d68c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071992"
---
# <a name="mdm_policy_result01_bluetooth02-class"></a><span data-ttu-id="26d39-105">\_Класс политики MDM \_ Result01 \_ Bluetooth02</span><span class="sxs-lookup"><span data-stu-id="26d39-105">MDM\_Policy\_Result01\_Bluetooth02 class</span></span>

<span data-ttu-id="26d39-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="26d39-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26d39-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="26d39-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26d39-108">Класс **\_ политики MDM \_ Result01 \_ Bluetooth02** представляет доступные политики управления Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="26d39-108">The **MDM\_Policy\_Result01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="26d39-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="26d39-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26d39-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="26d39-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a><span data-ttu-id="26d39-111">Члены</span><span class="sxs-lookup"><span data-stu-id="26d39-111">Members</span></span>

<span data-ttu-id="26d39-112">Класс **\_ политики MDM \_ Result01 \_ Bluetooth02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="26d39-112">The **MDM\_Policy\_Result01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="26d39-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="26d39-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26d39-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="26d39-114">Properties</span></span>

<span data-ttu-id="26d39-115">Класс **\_ политики MDM \_ Result01 \_ Bluetooth02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="26d39-115">The **MDM\_Policy\_Result01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="26d39-116">AllowAdvertising</span><span class="sxs-lookup"><span data-stu-id="26d39-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d39-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26d39-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d39-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26d39-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d39-119">AllowDiscoverableMode</span><span class="sxs-lookup"><span data-stu-id="26d39-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d39-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26d39-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d39-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26d39-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26d39-122">AllowPrepairing</span><span class="sxs-lookup"><span data-stu-id="26d39-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d39-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="26d39-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26d39-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26d39-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26d39-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26d39-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d39-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26d39-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d39-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26d39-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d39-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26d39-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26d39-129">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="26d39-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="26d39-130">Для этого класса строка имеет значение "Bluetooth".</span><span class="sxs-lookup"><span data-stu-id="26d39-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="26d39-131">LocalDeviceName</span><span class="sxs-lookup"><span data-stu-id="26d39-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d39-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26d39-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d39-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26d39-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26d39-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="26d39-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d39-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26d39-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d39-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="26d39-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26d39-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26d39-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26d39-138">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="26d39-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="26d39-139">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="26d39-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="26d39-140">ServicesAllowedList</span><span class="sxs-lookup"><span data-stu-id="26d39-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26d39-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="26d39-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26d39-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="26d39-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26d39-143">Требования</span><span class="sxs-lookup"><span data-stu-id="26d39-143">Requirements</span></span>



| <span data-ttu-id="26d39-144">Требование</span><span class="sxs-lookup"><span data-stu-id="26d39-144">Requirement</span></span> | <span data-ttu-id="26d39-145">Значение</span><span class="sxs-lookup"><span data-stu-id="26d39-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26d39-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="26d39-146">Minimum supported client</span></span><br/> | <span data-ttu-id="26d39-147">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="26d39-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="26d39-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="26d39-148">Minimum supported server</span></span><br/> | <span data-ttu-id="26d39-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="26d39-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="26d39-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="26d39-150">Namespace</span></span><br/>                | <span data-ttu-id="26d39-151">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="26d39-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="26d39-152">MOF</span><span class="sxs-lookup"><span data-stu-id="26d39-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26d39-153"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26d39-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="26d39-154">DLL</span><span class="sxs-lookup"><span data-stu-id="26d39-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26d39-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26d39-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26d39-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26d39-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26d39-157">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="26d39-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

