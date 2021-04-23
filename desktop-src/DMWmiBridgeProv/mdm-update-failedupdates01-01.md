---
title: Класс MDM_Update_FailedUpdates01_01
description: Класс MDM \_ Update \_ FailedUpdates01 \_ 01 используется для управления неудачными обновлениями.
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- Класс MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ba8d42d97b15cd195e87f536abad9610492e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489165"
---
# <a name="mdm_update_failedupdates01_01-class"></a><span data-ttu-id="3bc5b-105">\_Класс MDM обновления \_ FailedUpdates01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="3bc5b-105">MDM\_Update\_FailedUpdates01\_01 class</span></span>

<span data-ttu-id="3bc5b-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3bc5b-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3bc5b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3bc5b-108">Класс **MDM \_ Update \_ FailedUpdates01 \_ 01** используется для управления неудачными обновлениями.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-108">The **MDM\_Update\_FailedUpdates01\_01** class is used to manage failed updates.</span></span>

<span data-ttu-id="3bc5b-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bc5b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3bc5b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a><span data-ttu-id="3bc5b-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3bc5b-111">Members</span></span>

<span data-ttu-id="3bc5b-112">Класс **MDM \_ Update \_ FailedUpdates01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3bc5b-112">The **MDM\_Update\_FailedUpdates01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="3bc5b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3bc5b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bc5b-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3bc5b-114">Properties</span></span>

<span data-ttu-id="3bc5b-115">Класс **MDM \_ Update \_ FailedUpdates01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-115">The **MDM\_Update\_FailedUpdates01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3bc5b-116">Состав</span><span class="sxs-lookup"><span data-stu-id="3bc5b-116">HResult</span></span>](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bc5b-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3bc5b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3bc5b-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3bc5b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3bc5b-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3bc5b-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bc5b-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3bc5b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bc5b-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3bc5b-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bc5b-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3bc5b-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3bc5b-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="3bc5b-124">Для этого класса строка является идентификатором GUID неудачного обновления.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-124">For this class, the string is the GUID of the failed update.</span></span>

</dd> <dt>

<span data-ttu-id="3bc5b-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3bc5b-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bc5b-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3bc5b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3bc5b-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3bc5b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bc5b-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3bc5b-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3bc5b-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3bc5b-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="3bc5b-130">Для этого класса строка имеет значение "./вендор/мсфт/упдате/фаиледупдатес"</span><span class="sxs-lookup"><span data-stu-id="3bc5b-130">For this class, the string is "./Vendor/MSFT/Update/FailedUpdates"</span></span>

</dd> <dt>

[<span data-ttu-id="3bc5b-131">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3bc5b-131">**State**</span></span>](/windows/client-management/mdm/update-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bc5b-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3bc5b-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3bc5b-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3bc5b-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bc5b-134">Требования</span><span class="sxs-lookup"><span data-stu-id="3bc5b-134">Requirements</span></span>



| <span data-ttu-id="3bc5b-135">Требование</span><span class="sxs-lookup"><span data-stu-id="3bc5b-135">Requirement</span></span> | <span data-ttu-id="3bc5b-136">Значение</span><span class="sxs-lookup"><span data-stu-id="3bc5b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bc5b-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3bc5b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3bc5b-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3bc5b-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3bc5b-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3bc5b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3bc5b-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3bc5b-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="3bc5b-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3bc5b-141">Namespace</span></span><br/>                | <span data-ttu-id="3bc5b-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3bc5b-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="3bc5b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="3bc5b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bc5b-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bc5b-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="3bc5b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3bc5b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bc5b-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bc5b-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

