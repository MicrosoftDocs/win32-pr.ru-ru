---
title: Класс MDM_Update_InstallableUpdates01_01
description: Класс MDM \_ Update \_ InstallableUpdates01 \_ 01 используется для управления развертыванием утвержденных обновлений.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- Класс MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bcb9dd3ec026e6894d4ba7155cc41f12bc01e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891477"
---
# <a name="mdm_update_installableupdates01_01-class"></a><span data-ttu-id="8d324-105">\_Класс MDM обновления \_ InstallableUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="8d324-105">MDM\_Update\_InstallableUpdates01\_01 class</span></span>

<span data-ttu-id="8d324-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8d324-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8d324-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8d324-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8d324-108">Класс **MDM \_ Update \_ InstallableUpdates01 \_ 01** используется для управления развертыванием утвержденных обновлений.</span><span class="sxs-lookup"><span data-stu-id="8d324-108">The **MDM\_Update\_InstallableUpdates01\_01** class is used to manage and control the rollout of approved updates.</span></span>

<span data-ttu-id="8d324-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8d324-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d324-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d324-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a><span data-ttu-id="8d324-111">Члены</span><span class="sxs-lookup"><span data-stu-id="8d324-111">Members</span></span>

<span data-ttu-id="8d324-112">Класс **MDM \_ Update \_ InstallableUpdates01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8d324-112">The **MDM\_Update\_InstallableUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="8d324-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d324-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d324-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d324-114">Properties</span></span>

<span data-ttu-id="8d324-115">Класс **MDM \_ Update \_ InstallableUpdates01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="8d324-115">The **MDM\_Update\_InstallableUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d324-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8d324-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d324-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d324-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d324-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d324-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d324-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8d324-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8d324-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="8d324-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="8d324-121">Для этого класса строка является идентификатором GUID утвержденного обновления.</span><span class="sxs-lookup"><span data-stu-id="8d324-121">For this class, the string is the GUID of the approved update.</span></span>

</dd> <dt>

<span data-ttu-id="8d324-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8d324-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d324-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8d324-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8d324-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d324-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d324-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8d324-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8d324-126">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="8d324-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="8d324-127">Для этого класса строка имеет значение "./вендор/мсфт/упдате/инсталлаблеупдатес"</span><span class="sxs-lookup"><span data-stu-id="8d324-127">For this class, the string is "./Vendor/MSFT/Update/InstallableUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="8d324-128">RevisionNumber</span><span class="sxs-lookup"><span data-stu-id="8d324-128">RevisionNumber</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d324-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8d324-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d324-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8d324-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8d324-131">Тип</span><span class="sxs-lookup"><span data-stu-id="8d324-131">Type</span></span>](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d324-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8d324-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8d324-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8d324-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8d324-134">Требования</span><span class="sxs-lookup"><span data-stu-id="8d324-134">Requirements</span></span>



| <span data-ttu-id="8d324-135">Требование</span><span class="sxs-lookup"><span data-stu-id="8d324-135">Requirement</span></span> | <span data-ttu-id="8d324-136">Значение</span><span class="sxs-lookup"><span data-stu-id="8d324-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d324-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d324-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8d324-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8d324-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8d324-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d324-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8d324-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8d324-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="8d324-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8d324-141">Namespace</span></span><br/>                | <span data-ttu-id="8d324-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="8d324-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="8d324-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8d324-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d324-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d324-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="8d324-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8d324-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d324-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d324-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

