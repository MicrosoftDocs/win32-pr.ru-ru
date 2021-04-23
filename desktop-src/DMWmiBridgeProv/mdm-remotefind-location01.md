---
title: Класс MDM_RemoteFind_Location01
description: Класс MDM \_ ремотефинд \_ Location01 извлекает сведения о расположении для конкретного устройства.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- Класс MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01 класс, описание
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56e1b46a7b4a0c3439f78f38a5fb6cd5b865275c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489180"
---
# <a name="mdm_remotefind_location01-class"></a><span data-ttu-id="3b3b0-105">\_Класс MDM ремотефинд \_ Location01</span><span class="sxs-lookup"><span data-stu-id="3b3b0-105">MDM\_RemoteFind\_Location01 class</span></span>

<span data-ttu-id="3b3b0-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3b3b0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b3b0-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3b3b0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b3b0-108">Класс **MDM \_ ремотефинд \_ Location01** извлекает сведения о расположении для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="3b3b0-108">The **MDM\_RemoteFind\_Location01** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="3b3b0-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3b3b0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b3b0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b3b0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a><span data-ttu-id="3b3b0-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3b3b0-111">Members</span></span>

<span data-ttu-id="3b3b0-112">Класс **MDM \_ ремотефинд \_ Location01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3b3b0-112">The **MDM\_RemoteFind\_Location01** class has these types of members:</span></span>

-   [<span data-ttu-id="3b3b0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3b3b0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b3b0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3b3b0-114">Properties</span></span>

<span data-ttu-id="3b3b0-115">Класс **MDM \_ ремотефинд \_ Location01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3b3b0-115">The **MDM\_RemoteFind\_Location01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3b3b0-116">Точность</span><span class="sxs-lookup"><span data-stu-id="3b3b0-116">Accuracy</span></span>](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b3b0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b3b0-119">Age</span><span class="sxs-lookup"><span data-stu-id="3b3b0-119">Age</span></span>](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-120">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-120">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b3b0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b3b0-122">Высота над уровнем моря</span><span class="sxs-lookup"><span data-stu-id="3b3b0-122">Altitude</span></span>](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-123">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-123">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b3b0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b3b0-125">алтитудеаккураци</span><span class="sxs-lookup"><span data-stu-id="3b3b0-125">AltitudeAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b3b0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b3b0-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b3b0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b3b0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b3b0-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="3b3b0-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="3b3b0-133">Для этого класса строка имеет значение Location.</span><span class="sxs-lookup"><span data-stu-id="3b3b0-133">For this class, the string is "Location".</span></span>

</dd> <dt>

[<span data-ttu-id="3b3b0-134">Широта</span><span class="sxs-lookup"><span data-stu-id="3b3b0-134">Latitude</span></span>](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-135">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-135">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b3b0-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b3b0-137">Долгот</span><span class="sxs-lookup"><span data-stu-id="3b3b0-137">Longitude</span></span>](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-138">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-138">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3b3b0-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b3b0-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b3b0-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3b3b0-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b3b0-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b3b0-143">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b3b0-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3b3b0-144">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3b3b0-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="3b3b0-145">Для этого класса строка имеет значение "./вендор/мсфт/ремотефинд"</span><span class="sxs-lookup"><span data-stu-id="3b3b0-145">For this class, the string is "./Vendor/MSFT/RemoteFind"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b3b0-146">Требования</span><span class="sxs-lookup"><span data-stu-id="3b3b0-146">Requirements</span></span>



| <span data-ttu-id="3b3b0-147">Требование</span><span class="sxs-lookup"><span data-stu-id="3b3b0-147">Requirement</span></span> | <span data-ttu-id="3b3b0-148">Значение</span><span class="sxs-lookup"><span data-stu-id="3b3b0-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b3b0-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b3b0-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3b3b0-150">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3b3b0-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3b3b0-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b3b0-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3b3b0-152">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3b3b0-152">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="3b3b0-153">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3b3b0-153">Namespace</span></span><br/>                | <span data-ttu-id="3b3b0-154">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3b3b0-154">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="3b3b0-155">MOF</span><span class="sxs-lookup"><span data-stu-id="3b3b0-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b3b0-156"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b3b0-156"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b3b0-157">DLL</span><span class="sxs-lookup"><span data-stu-id="3b3b0-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b3b0-158"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b3b0-158"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3b3b0-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b3b0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b3b0-160">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="3b3b0-160">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

