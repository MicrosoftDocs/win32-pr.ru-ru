---
title: Класс MDM_Update_PendingRebootUpdates01_01
description: Класс MDM \_ Update \_ PendingRebootUpdates01 \_ 01 используется для управления обновлениями, ожидающими при перезагрузке.
ms.assetid: 752cdaaa-7883-43d4-be7d-7da9ad15d041
keywords:
- Класс MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01.InstanceID
- MDM_Update_PendingRebootUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca640a4de00ea9eb115b999129a16dd0bf930cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137258"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a><span data-ttu-id="92173-105">\_Класс MDM обновления \_ PendingRebootUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="92173-105">MDM\_Update\_PendingRebootUpdates01\_01 class</span></span>

<span data-ttu-id="92173-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="92173-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="92173-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="92173-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="92173-108">Класс **MDM \_ Update \_ PendingRebootUpdates01 \_ 01** используется для управления обновлениями, ожидающими при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="92173-108">The **MDM\_Update\_PendingRebootUpdates01\_01** class is used to manage updates that are pending on reboot.</span></span>

<span data-ttu-id="92173-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="92173-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92173-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92173-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_PendingRebootUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime InstalledTime;
};
```

## <a name="members"></a><span data-ttu-id="92173-111">Члены</span><span class="sxs-lookup"><span data-stu-id="92173-111">Members</span></span>

<span data-ttu-id="92173-112">Класс **MDM \_ Update \_ PendingRebootUpdates01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="92173-112">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="92173-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="92173-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="92173-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="92173-114">Properties</span></span>

<span data-ttu-id="92173-115">Класс **MDM \_ Update \_ PendingRebootUpdates01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="92173-115">The **MDM\_Update\_PendingRebootUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="92173-116">инсталледтиме</span><span class="sxs-lookup"><span data-stu-id="92173-116">InstalledTime</span></span>](/windows/client-management/mdm/update-csp#pendingrebootupdates-pending-reboot-update-guid-installedtime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="92173-117">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92173-117">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92173-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="92173-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="92173-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="92173-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92173-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92173-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92173-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92173-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92173-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92173-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="92173-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="92173-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="92173-124">Для этого класса строка представляет собой идентификатор GUID обновления, ожидающего перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="92173-124">For this class, the string is the GUID of the update that is pending reboot.</span></span>

</dd> <dt>

<span data-ttu-id="92173-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="92173-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92173-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="92173-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92173-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="92173-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92173-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="92173-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="92173-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="92173-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="92173-130">Для этого класса строка имеет значение "./вендор/мсфт/упдате/пендингребутупдатес"</span><span class="sxs-lookup"><span data-stu-id="92173-130">For this class, the string is "./Vendor/MSFT/Update/PendingRebootUpdates"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92173-131">Требования</span><span class="sxs-lookup"><span data-stu-id="92173-131">Requirements</span></span>



| <span data-ttu-id="92173-132">Требование</span><span class="sxs-lookup"><span data-stu-id="92173-132">Requirement</span></span> | <span data-ttu-id="92173-133">Значение</span><span class="sxs-lookup"><span data-stu-id="92173-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92173-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92173-134">Minimum supported client</span></span><br/> | <span data-ttu-id="92173-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="92173-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="92173-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92173-136">Minimum supported server</span></span><br/> | <span data-ttu-id="92173-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="92173-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="92173-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92173-138">Namespace</span></span><br/>                | <span data-ttu-id="92173-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="92173-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="92173-140">MOF</span><span class="sxs-lookup"><span data-stu-id="92173-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92173-141"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92173-141"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="92173-142">DLL</span><span class="sxs-lookup"><span data-stu-id="92173-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92173-143"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92173-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

