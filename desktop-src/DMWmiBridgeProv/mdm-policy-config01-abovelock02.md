---
title: Класс MDM_Policy_Config01_AboveLock02
description: '\_Класс политики MDM \_ Config01 \_ AboveLock02 представляет политики, которые определяют действия, разрешенные над экраном блокировки устройства.'
ms.assetid: ad76e424-e5b6-46ba-a6a7-5dc00f983918
keywords:
- Класс MDM_Policy_Config01_AboveLock02
- MDM_Policy_Config01_AboveLock02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_AboveLock02
- MDM_Policy_Config01_AboveLock02.InstanceID
- MDM_Policy_Config01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703971a10fe927c391831a9db65d270291b56e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654460"
---
# <a name="mdm_policy_config01_abovelock02-class"></a><span data-ttu-id="7ead2-105">\_Класс политики MDM \_ Config01 \_ AboveLock02</span><span class="sxs-lookup"><span data-stu-id="7ead2-105">MDM\_Policy\_Config01\_AboveLock02 class</span></span>

<span data-ttu-id="7ead2-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="7ead2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ead2-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="7ead2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ead2-108">Класс **\_ политики MDM \_ Config01 \_ AboveLock02** представляет политики, которые определяют действия, разрешенные над экраном блокировки устройства.</span><span class="sxs-lookup"><span data-stu-id="7ead2-108">The **MDM\_Policy\_Config01\_AboveLock02** class represents policies that determine actions that are allowed above the Device Lock screen.</span></span>

<span data-ttu-id="7ead2-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7ead2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ead2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ead2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a><span data-ttu-id="7ead2-111">Члены</span><span class="sxs-lookup"><span data-stu-id="7ead2-111">Members</span></span>

<span data-ttu-id="7ead2-112">Класс **\_ политики MDM \_ Config01 \_ AboveLock02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7ead2-112">The **MDM\_Policy\_Config01\_AboveLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="7ead2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ead2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ead2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ead2-114">Properties</span></span>

<span data-ttu-id="7ead2-115">Класс **\_ политики MDM \_ Config01 \_ AboveLock02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7ead2-115">The **MDM\_Policy\_Config01\_AboveLock02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7ead2-116">алловкортанаабовелокк</span><span class="sxs-lookup"><span data-stu-id="7ead2-116">AllowCortanaAboveLock</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead2-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7ead2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ead2-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7ead2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ead2-119">AllowToasts</span><span class="sxs-lookup"><span data-stu-id="7ead2-119">AllowToasts</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead2-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7ead2-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ead2-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7ead2-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7ead2-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ead2-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead2-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ead2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead2-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ead2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead2-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ead2-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ead2-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="7ead2-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="7ead2-127">Для этого класса строка имеет значение "Абовелокк".</span><span class="sxs-lookup"><span data-stu-id="7ead2-127">For this class, the string is "AboveLock".</span></span>

</dd> <dt>

<span data-ttu-id="7ead2-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7ead2-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ead2-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7ead2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ead2-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ead2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ead2-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ead2-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7ead2-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="7ead2-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="7ead2-133">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="7ead2-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ead2-134">Требования</span><span class="sxs-lookup"><span data-stu-id="7ead2-134">Requirements</span></span>



| <span data-ttu-id="7ead2-135">Требование</span><span class="sxs-lookup"><span data-stu-id="7ead2-135">Requirement</span></span> | <span data-ttu-id="7ead2-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7ead2-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ead2-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ead2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7ead2-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7ead2-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ead2-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ead2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7ead2-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7ead2-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7ead2-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7ead2-141">Namespace</span></span><br/>                | <span data-ttu-id="7ead2-142">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="7ead2-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="7ead2-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7ead2-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ead2-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ead2-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ead2-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7ead2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ead2-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ead2-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ead2-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ead2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ead2-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="7ead2-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

