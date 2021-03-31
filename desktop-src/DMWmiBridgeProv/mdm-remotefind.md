---
title: Класс MDM_RemoteFind
description: '\_Класс РЕМОТЕФИНД MDM извлекает сведения о расположении для конкретного устройства.'
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- Класс MDM_RemoteFind
- MDM_RemoteFind класс, описание
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801205"
---
# <a name="mdm_remotefind-class"></a><span data-ttu-id="c7f1c-105">\_Класс MDM ремотефинд</span><span class="sxs-lookup"><span data-stu-id="c7f1c-105">MDM\_RemoteFind class</span></span>

<span data-ttu-id="c7f1c-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c7f1c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c7f1c-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c7f1c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c7f1c-108">Класс **\_ ремотефинд MDM** извлекает сведения о расположении для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="c7f1c-108">The **MDM\_RemoteFind** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="c7f1c-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c7f1c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7f1c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7f1c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a><span data-ttu-id="c7f1c-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c7f1c-111">Members</span></span>

<span data-ttu-id="c7f1c-112">Класс **MDM \_ ремотефинд** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c7f1c-112">The **MDM\_RemoteFind** class has these types of members:</span></span>

-   [<span data-ttu-id="c7f1c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7f1c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7f1c-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c7f1c-114">Properties</span></span>

<span data-ttu-id="c7f1c-115">Класс **MDM \_ ремотефинд** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c7f1c-115">The **MDM\_RemoteFind** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c7f1c-116">десиредаккураци</span><span class="sxs-lookup"><span data-stu-id="c7f1c-116">DesiredAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f1c-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f1c-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c7f1c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7f1c-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f1c-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f1c-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7f1c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f1c-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c7f1c-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c7f1c-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="c7f1c-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="c7f1c-124">Для этого класса строка имеет значение "Ремотефинд".</span><span class="sxs-lookup"><span data-stu-id="c7f1c-124">For this class, the string is "RemoteFind".</span></span>

</dd> <dt>

[<span data-ttu-id="c7f1c-125">Максимальная длина</span><span class="sxs-lookup"><span data-stu-id="c7f1c-125">MaximumAge</span></span>](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f1c-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f1c-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c7f1c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c7f1c-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f1c-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c7f1c-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c7f1c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c7f1c-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c7f1c-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c7f1c-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="c7f1c-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="c7f1c-133">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="c7f1c-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="c7f1c-134">Timeout</span><span class="sxs-lookup"><span data-stu-id="c7f1c-134">Timeout</span></span>](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c7f1c-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c7f1c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c7f1c-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c7f1c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7f1c-137">Требования</span><span class="sxs-lookup"><span data-stu-id="c7f1c-137">Requirements</span></span>



| <span data-ttu-id="c7f1c-138">Требование</span><span class="sxs-lookup"><span data-stu-id="c7f1c-138">Requirement</span></span> | <span data-ttu-id="c7f1c-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c7f1c-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7f1c-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7f1c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c7f1c-141">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c7f1c-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c7f1c-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7f1c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c7f1c-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c7f1c-143">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="c7f1c-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c7f1c-144">Namespace</span></span><br/>                | <span data-ttu-id="c7f1c-145">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c7f1c-145">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                              |
| <span data-ttu-id="c7f1c-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c7f1c-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7f1c-147"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7f1c-147"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7f1c-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c7f1c-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7f1c-149"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7f1c-149"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c7f1c-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7f1c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7f1c-151">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="c7f1c-151">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

