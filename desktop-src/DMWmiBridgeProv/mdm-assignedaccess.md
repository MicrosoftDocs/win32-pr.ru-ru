---
title: Класс MDM_AssignedAccess
description: Класс MDM \_ ассигнедакцесс используется для настройки запуска устройства в полноэкранном режиме.
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- Класс MDM_AssignedAccess
- MDM_AssignedAccess класс, описание
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492966"
---
# <a name="mdm_assignedaccess-class"></a><span data-ttu-id="7efa0-105">\_Класс MDM ассигнедакцесс</span><span class="sxs-lookup"><span data-stu-id="7efa0-105">MDM\_AssignedAccess class</span></span>

<span data-ttu-id="7efa0-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="7efa0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7efa0-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="7efa0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7efa0-108">Класс **MDM \_ ассигнедакцесс** используется для настройки запуска устройства в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="7efa0-108">The **MDM\_AssignedAccess** class is used to set the device to run in kiosk mode.</span></span> <span data-ttu-id="7efa0-109">После выполнения класса следующее имя входа пользователя, связанное с режимом киоска, переводит устройство в полноэкранный режим, запуская приложение, указанное в пакете подготовки.</span><span class="sxs-lookup"><span data-stu-id="7efa0-109">Once the class has been executed, then the next user login that is associated with the kiosk mode puts the device in the kiosk mode running the application specified in the provisioning package.</span></span>

<span data-ttu-id="7efa0-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7efa0-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7efa0-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7efa0-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a><span data-ttu-id="7efa0-112">Члены</span><span class="sxs-lookup"><span data-stu-id="7efa0-112">Members</span></span>

<span data-ttu-id="7efa0-113">Класс **MDM \_ ассигнедакцесс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7efa0-113">The **MDM\_AssignedAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="7efa0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7efa0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7efa0-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7efa0-115">Properties</span></span>

<span data-ttu-id="7efa0-116">Класс **MDM \_ ассигнедакцесс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7efa0-116">The **MDM\_AssignedAccess** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7efa0-117">Конфигурация</span><span class="sxs-lookup"><span data-stu-id="7efa0-117">Configuration</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efa0-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7efa0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efa0-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7efa0-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7efa0-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7efa0-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efa0-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7efa0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efa0-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7efa0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efa0-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7efa0-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7efa0-124">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="7efa0-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="7efa0-125">Для этого класса строка имеет значение "Ассигнедакцесс".</span><span class="sxs-lookup"><span data-stu-id="7efa0-125">For this class, the string is "AssignedAccess".</span></span>

</dd> <dt>

[<span data-ttu-id="7efa0-126">киоскмодеапп</span><span class="sxs-lookup"><span data-stu-id="7efa0-126">KioskModeApp</span></span>](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efa0-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7efa0-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efa0-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7efa0-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7efa0-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7efa0-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efa0-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7efa0-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7efa0-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7efa0-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7efa0-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7efa0-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7efa0-133">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="7efa0-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="7efa0-134">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="7efa0-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7efa0-135">Требования</span><span class="sxs-lookup"><span data-stu-id="7efa0-135">Requirements</span></span>



| <span data-ttu-id="7efa0-136">Требование</span><span class="sxs-lookup"><span data-stu-id="7efa0-136">Requirement</span></span> | <span data-ttu-id="7efa0-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7efa0-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7efa0-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7efa0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7efa0-139">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7efa0-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7efa0-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7efa0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7efa0-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7efa0-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7efa0-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7efa0-142">Namespace</span></span><br/>                | <span data-ttu-id="7efa0-143">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="7efa0-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7efa0-144">MOF</span><span class="sxs-lookup"><span data-stu-id="7efa0-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7efa0-145"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7efa0-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7efa0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="7efa0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7efa0-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7efa0-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7efa0-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7efa0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efa0-149">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="7efa0-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

