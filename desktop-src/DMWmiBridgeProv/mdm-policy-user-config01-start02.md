---
title: Класс MDM_Policy_User_Config01_Start02
description: '\_ \_ \_ Класс User CONFIG01 Start02 политики MDM \_ представляет доступные политики запуска, заданные для каждого пользователя.'
ms.assetid: bbb64553-4d93-433d-96e4-bfd3f5588138
keywords:
- Класс MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Start02
- MDM_Policy_User_Config01_Start02.InstanceID
- MDM_Policy_User_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b98b25ee0c3118f741d3a52bc9001c6106d86f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415597"
---
# <a name="mdm_policy_user_config01_start02-class"></a><span data-ttu-id="51061-105">\_Класс политики MDM \_ user \_ Config01 \_ Start02</span><span class="sxs-lookup"><span data-stu-id="51061-105">MDM\_Policy\_User\_Config01\_Start02 class</span></span>

<span data-ttu-id="51061-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="51061-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="51061-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="51061-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="51061-108">Класс **\_ \_ user \_ Config01 \_ Start02 политики MDM** представляет доступные политики запуска, заданные для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="51061-108">The **MDM\_Policy\_User\_Config01\_Start02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="51061-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="51061-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51061-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51061-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 HidePeopleBar;
  string StartLayout;
};
```

## <a name="members"></a><span data-ttu-id="51061-111">Члены</span><span class="sxs-lookup"><span data-stu-id="51061-111">Members</span></span>

<span data-ttu-id="51061-112">Класс **\_ \_ user \_ Config01 \_ Start02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="51061-112">The **MDM\_Policy\_User\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="51061-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="51061-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51061-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="51061-114">Properties</span></span>

<span data-ttu-id="51061-115">Класс **\_ \_ user \_ Config01 \_ Start02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="51061-115">The **MDM\_Policy\_User\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="51061-116">HidePeopleBar</span><span class="sxs-lookup"><span data-stu-id="51061-116">HidePeopleBar</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepeoplebar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51061-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="51061-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="51061-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="51061-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="51061-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="51061-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51061-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="51061-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51061-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51061-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51061-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="51061-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="51061-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="51061-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="51061-124">Для этого класса строка имеет значение Start.</span><span class="sxs-lookup"><span data-stu-id="51061-124">For this class, the string is "Start"</span></span>

</dd> <dt>

<span data-ttu-id="51061-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="51061-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51061-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="51061-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51061-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="51061-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51061-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="51061-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="51061-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="51061-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="51061-130">Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="51061-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="51061-131">StartLayout</span><span class="sxs-lookup"><span data-stu-id="51061-131">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="51061-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="51061-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51061-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="51061-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51061-134">Требования</span><span class="sxs-lookup"><span data-stu-id="51061-134">Requirements</span></span>



| <span data-ttu-id="51061-135">Требование</span><span class="sxs-lookup"><span data-stu-id="51061-135">Requirement</span></span> | <span data-ttu-id="51061-136">Значение</span><span class="sxs-lookup"><span data-stu-id="51061-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51061-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51061-137">Minimum supported client</span></span><br/> | <span data-ttu-id="51061-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="51061-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51061-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51061-139">Minimum supported server</span></span><br/> | <span data-ttu-id="51061-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="51061-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="51061-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="51061-141">Namespace</span></span><br/>                | <span data-ttu-id="51061-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="51061-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="51061-143">MOF</span><span class="sxs-lookup"><span data-stu-id="51061-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51061-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51061-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="51061-145">DLL</span><span class="sxs-lookup"><span data-stu-id="51061-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51061-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51061-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51061-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51061-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51061-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="51061-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

