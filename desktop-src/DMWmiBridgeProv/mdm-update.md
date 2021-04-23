---
title: Класс MDM_Update
description: '\_Класс обновления MDM используется для управления развертыванием новых обновлений.'
ms.assetid: 503884fd-190c-482d-b600-1a15363891f3
keywords:
- Класс MDM_Update
- MDM_Update класс, описание
topic_type:
- apiref
api_name:
- MDM_Update
- MDM_Update.InstanceID
- MDM_Update.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2735b5eaaef4abc468586cb7608be7969a1eab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891765"
---
# <a name="mdm_update-class"></a><span data-ttu-id="4e615-105">\_Класс обновления MDM</span><span class="sxs-lookup"><span data-stu-id="4e615-105">MDM\_Update class</span></span>

<span data-ttu-id="4e615-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4e615-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4e615-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4e615-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4e615-108">Класс **\_ обновления MDM** используется для управления развертыванием новых обновлений.</span><span class="sxs-lookup"><span data-stu-id="4e615-108">The **MDM\_Update** class is used to manage and control the rollout of new updates.</span></span>

<span data-ttu-id="4e615-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4e615-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e615-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e615-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update
{
  string   InstanceID;
  string   ParentID;
  datetime LastSuccessfulScanTime;
  sint32   DeferUpgrade;
};
```

## <a name="members"></a><span data-ttu-id="4e615-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4e615-111">Members</span></span>

<span data-ttu-id="4e615-112">Класс **\_ обновления MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4e615-112">The **MDM\_Update** class has these types of members:</span></span>

-   [<span data-ttu-id="4e615-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e615-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e615-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e615-114">Properties</span></span>

<span data-ttu-id="4e615-115">Класс **\_ обновления MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="4e615-115">The **MDM\_Update** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4e615-116">DeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="4e615-116">DeferUpgrade</span></span>](/windows/client-management/mdm/update-csp#deferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e615-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e615-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e615-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e615-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4e615-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4e615-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e615-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4e615-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e615-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4e615-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e615-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e615-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e615-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="4e615-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="4e615-124">Для этого класса строка имеет значение "Update".</span><span class="sxs-lookup"><span data-stu-id="4e615-124">For this class, the string is "Update".</span></span>

</dd> <dt>

[<span data-ttu-id="4e615-125">ластсукцессфулскантиме</span><span class="sxs-lookup"><span data-stu-id="4e615-125">LastSuccessfulScanTime</span></span>](/windows/client-management/mdm/update-csp#lastsuccessfulscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e615-126">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e615-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e615-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e615-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4e615-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4e615-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e615-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4e615-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e615-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4e615-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e615-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e615-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e615-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="4e615-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="4e615-133">Для этого класса строка имеет значение "./вендор/мсфт/"</span><span class="sxs-lookup"><span data-stu-id="4e615-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e615-134">Требования</span><span class="sxs-lookup"><span data-stu-id="4e615-134">Requirements</span></span>



| <span data-ttu-id="4e615-135">Требование</span><span class="sxs-lookup"><span data-stu-id="4e615-135">Requirement</span></span> | <span data-ttu-id="4e615-136">Значение</span><span class="sxs-lookup"><span data-stu-id="4e615-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e615-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e615-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4e615-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4e615-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4e615-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e615-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4e615-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e615-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="4e615-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e615-141">Namespace</span></span><br/>                | <span data-ttu-id="4e615-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4e615-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="4e615-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4e615-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e615-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e615-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="4e615-145">DLL</span><span class="sxs-lookup"><span data-stu-id="4e615-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e615-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e615-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

