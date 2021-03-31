---
title: Класс MDM_Reboot
description: Ребуткласс MDM \_ используется для настройки параметров перезагрузки.
ms.assetid: 876ba854-1c26-49cf-915d-194be9f9c1d4
keywords:
- Класс MDM_Reboot
- MDM_Reboot класс, описание
topic_type:
- apiref
api_name:
- MDM_Reboot
- MDM_Reboot.InstanceID
- MDM_Reboot.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e078dfef883db5aad67e7ee834ceca4bd0a942
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071160"
---
# <a name="mdm_reboot-class"></a><span data-ttu-id="f6c05-105">\_Класс перезагрузки MDM</span><span class="sxs-lookup"><span data-stu-id="f6c05-105">MDM\_Reboot class</span></span>

<span data-ttu-id="f6c05-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f6c05-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f6c05-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f6c05-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f6c05-108">Класс **\_ перезагрузки MDM** используется для настройки параметров перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="f6c05-108">The **MDM\_Reboot** class is used to configure reboot settings.</span></span>

<span data-ttu-id="f6c05-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f6c05-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c05-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6c05-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="f6c05-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f6c05-111">Members</span></span>

<span data-ttu-id="f6c05-112">Класс **\_ перезагрузки MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f6c05-112">The **MDM\_Reboot** class has these types of members:</span></span>

-   [<span data-ttu-id="f6c05-113">Методы</span><span class="sxs-lookup"><span data-stu-id="f6c05-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="f6c05-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f6c05-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f6c05-115">Методы</span><span class="sxs-lookup"><span data-stu-id="f6c05-115">Methods</span></span>

<span data-ttu-id="f6c05-116">Класс **\_ перезагрузки MDM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f6c05-116">The **MDM\_Reboot** class has these methods.</span></span>



| <span data-ttu-id="f6c05-117">Метод</span><span class="sxs-lookup"><span data-stu-id="f6c05-117">Method</span></span>                                                | <span data-ttu-id="f6c05-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f6c05-118">Description</span></span>                                             |
|:------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="f6c05-119">**ребутновмесод**</span><span class="sxs-lookup"><span data-stu-id="f6c05-119">**RebootNowMethod**</span></span>](mdm-reboot-rebootnowmethod.md) | <span data-ttu-id="f6c05-120">Этот метод выполняет перезагрузку устройства.</span><span class="sxs-lookup"><span data-stu-id="f6c05-120">This method executes a reboot of the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f6c05-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="f6c05-121">Properties</span></span>

<span data-ttu-id="f6c05-122">Класс **\_ перезагрузки MDM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f6c05-122">The **MDM\_Reboot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6c05-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6c05-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6c05-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f6c05-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6c05-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6c05-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6c05-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6c05-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6c05-127">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f6c05-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="f6c05-128">Для этого класса строка имеет значение "reboot".</span><span class="sxs-lookup"><span data-stu-id="f6c05-128">For this class, the string is "Reboot".</span></span>

</dd> <dt>

<span data-ttu-id="f6c05-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f6c05-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6c05-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f6c05-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6c05-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f6c05-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6c05-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6c05-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f6c05-133">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f6c05-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="f6c05-134">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="f6c05-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6c05-135">Требования</span><span class="sxs-lookup"><span data-stu-id="f6c05-135">Requirements</span></span>



| <span data-ttu-id="f6c05-136">Требование</span><span class="sxs-lookup"><span data-stu-id="f6c05-136">Requirement</span></span> | <span data-ttu-id="f6c05-137">Значение</span><span class="sxs-lookup"><span data-stu-id="f6c05-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c05-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6c05-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c05-139">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f6c05-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f6c05-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6c05-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c05-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6c05-141">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="f6c05-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f6c05-142">Namespace</span></span><br/>                | <span data-ttu-id="f6c05-143">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f6c05-143">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="f6c05-144">MOF</span><span class="sxs-lookup"><span data-stu-id="f6c05-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6c05-145"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6c05-145"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="f6c05-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f6c05-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6c05-147"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6c05-147"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

