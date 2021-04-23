---
title: Класс MDM_Firewall_App04
description: '\_ \_ Класс APP04 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.'
ms.assetid: d7844d89-97d3-43b4-85af-c9464d475167
keywords:
- Класс MDM_Firewall_App04
- MDM_Firewall_App04 класс, описание
topic_type:
- apiref
api_name:
- MDM_Firewall_App04
- MDM_Firewall_App04.InstanceID
- MDM_Firewall_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a8558fb2834ba9b0143d644cf4922aa9a710d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135570"
---
# <a name="mdm_firewall_app04-class"></a><span data-ttu-id="443c5-105">\_ \_ Класс APP04 брандмауэра MDM</span><span class="sxs-lookup"><span data-stu-id="443c5-105">MDM\_Firewall\_App04 class</span></span>

<span data-ttu-id="443c5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="443c5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="443c5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="443c5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="443c5-108">\_ \_ Класс APP04 брандмауэра MDM используется для настройки параметров брандмауэра защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="443c5-108">The MDM\_Firewall\_App04 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="443c5-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="443c5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="443c5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="443c5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_App04
{
  string InstanceID;
  string ParentID;
  string PackageFamilyName;
  string FilePath;
  string Fqbn;
  string ServiceName;
};
```

## <a name="members"></a><span data-ttu-id="443c5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="443c5-111">Members</span></span>

<span data-ttu-id="443c5-112">Класс **\_ \_ App04 брандмауэра MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="443c5-112">The **MDM\_Firewall\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="443c5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="443c5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="443c5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="443c5-114">Properties</span></span>

<span data-ttu-id="443c5-115">Класс **\_ \_ App04 брандмауэра MDM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="443c5-115">The **MDM\_Firewall\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="443c5-116">Равно</span><span class="sxs-lookup"><span data-stu-id="443c5-116">FilePath</span></span>](/windows/client-management/mdm/firewall-csp#filepath)
</dt> <dd> <dl> <dt>

<span data-ttu-id="443c5-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443c5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443c5-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="443c5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="443c5-119">фкбн</span><span class="sxs-lookup"><span data-stu-id="443c5-119">Fqbn</span></span>](/windows/client-management/mdm/firewall-csp#fqbn)
</dt> <dd> <dl> <dt>

<span data-ttu-id="443c5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443c5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443c5-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="443c5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="443c5-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="443c5-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="443c5-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443c5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443c5-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="443c5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="443c5-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="443c5-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="443c5-126">паккажефамилинаме</span><span class="sxs-lookup"><span data-stu-id="443c5-126">PackageFamilyName</span></span>](/windows/client-management/mdm/firewall-csp#packagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="443c5-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443c5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443c5-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="443c5-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="443c5-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="443c5-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="443c5-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443c5-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443c5-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="443c5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="443c5-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="443c5-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="443c5-133">Служба</span><span class="sxs-lookup"><span data-stu-id="443c5-133">ServiceName</span></span>](/windows/client-management/mdm/firewall-csp#servicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="443c5-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="443c5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="443c5-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="443c5-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="443c5-136">Требования</span><span class="sxs-lookup"><span data-stu-id="443c5-136">Requirements</span></span>



| <span data-ttu-id="443c5-137">Требование</span><span class="sxs-lookup"><span data-stu-id="443c5-137">Requirement</span></span> | <span data-ttu-id="443c5-138">Значение</span><span class="sxs-lookup"><span data-stu-id="443c5-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="443c5-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="443c5-139">Minimum supported client</span></span><br/> | <span data-ttu-id="443c5-140">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="443c5-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="443c5-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="443c5-141">Minimum supported server</span></span><br/> | <span data-ttu-id="443c5-142">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="443c5-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="443c5-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="443c5-143">Namespace</span></span><br/>                | <span data-ttu-id="443c5-144">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="443c5-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="443c5-145">MOF</span><span class="sxs-lookup"><span data-stu-id="443c5-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="443c5-146"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="443c5-146"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="443c5-147">DLL</span><span class="sxs-lookup"><span data-stu-id="443c5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="443c5-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="443c5-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

