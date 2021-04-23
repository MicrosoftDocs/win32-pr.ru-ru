---
title: Класс MDM_Policy_Result01_AboveLock02
description: '\_Класс политики MDM \_ Result01 \_ AboveLock02 представляет политики, которые определяют действия, разрешенные над экраном блокировки устройства.'
ms.assetid: 0b6d4083-2484-450b-9261-5ef339db4707
keywords:
- Класс MDM_Policy_Result01_AboveLock02
- MDM_Policy_Result01_AboveLock02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AboveLock02
- MDM_Policy_Result01_AboveLock02.InstanceID
- MDM_Policy_Result01_AboveLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530ed3c4afd3b6e888ee77d0963881c2b4d5ef93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988717"
---
# <a name="mdm_policy_result01_abovelock02-class"></a><span data-ttu-id="d8942-105">\_Класс политики MDM \_ Result01 \_ AboveLock02</span><span class="sxs-lookup"><span data-stu-id="d8942-105">MDM\_Policy\_Result01\_AboveLock02 class</span></span>

<span data-ttu-id="d8942-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="d8942-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d8942-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="d8942-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d8942-108">Класс **\_ политики MDM \_ Result01 \_ AboveLock02** представляет политики, которые определяют действия, разрешенные над экраном блокировки устройства.</span><span class="sxs-lookup"><span data-stu-id="d8942-108">The **MDM\_Policy\_Result01\_AboveLock02** class represents policies that determine actions that are allowed above the Device Lock screen.</span></span>

<span data-ttu-id="d8942-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d8942-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8942-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d8942-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AboveLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowToasts;
  sint32 AllowCortanaAboveLock;
};
```

## <a name="members"></a><span data-ttu-id="d8942-111">Члены</span><span class="sxs-lookup"><span data-stu-id="d8942-111">Members</span></span>

<span data-ttu-id="d8942-112">Класс **\_ политики MDM \_ Result01 \_ AboveLock02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d8942-112">The **MDM\_Policy\_Result01\_AboveLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="d8942-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d8942-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d8942-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="d8942-114">Properties</span></span>

<span data-ttu-id="d8942-115">Класс **\_ политики MDM \_ Result01 \_ AboveLock02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d8942-115">The **MDM\_Policy\_Result01\_AboveLock02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d8942-116">алловкортанаабовелокк</span><span class="sxs-lookup"><span data-stu-id="d8942-116">AllowCortanaAboveLock</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowcortanaabovelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8942-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d8942-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8942-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d8942-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d8942-119">AllowToasts</span><span class="sxs-lookup"><span data-stu-id="d8942-119">AllowToasts</span></span>](/windows/client-management/mdm/policy-csp-abovelock#abovelock-allowtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8942-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d8942-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d8942-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d8942-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d8942-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d8942-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8942-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8942-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8942-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8942-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8942-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8942-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8942-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="d8942-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="d8942-127">Для этого класса строка имеет значение "Абовелокк".</span><span class="sxs-lookup"><span data-stu-id="d8942-127">For this class, the string is "AboveLock".</span></span>

</dd> <dt>

<span data-ttu-id="d8942-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d8942-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8942-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d8942-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d8942-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d8942-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d8942-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d8942-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d8942-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="d8942-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="d8942-133">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="d8942-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8942-134">Требования</span><span class="sxs-lookup"><span data-stu-id="d8942-134">Requirements</span></span>



| <span data-ttu-id="d8942-135">Требование</span><span class="sxs-lookup"><span data-stu-id="d8942-135">Requirement</span></span> | <span data-ttu-id="d8942-136">Значение</span><span class="sxs-lookup"><span data-stu-id="d8942-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8942-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8942-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d8942-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d8942-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8942-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8942-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d8942-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d8942-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d8942-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d8942-141">Namespace</span></span><br/>                | <span data-ttu-id="d8942-142">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="d8942-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="d8942-143">MOF</span><span class="sxs-lookup"><span data-stu-id="d8942-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8942-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8942-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8942-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d8942-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8942-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8942-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8942-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8942-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8942-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="d8942-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

