---
title: Класс MDM_Policy_Config01_BitLocker02
description: '\_Класс политики MDM \_ Config01 \_ Bitlocker02 представляет доступные политики BitLocker.'
ms.assetid: 885df93f-41f5-4cf7-8bce-9b253b190e17
keywords:
- Класс MDM_Policy_Config01_BitLocker02
- MDM_Policy_Config01_BitLocker02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_BitLocker02
- MDM_Policy_Config01_BitLocker02.InstanceID
- MDM_Policy_Config01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 005c16365dfc227aff4c854e77b2a733a3c4ac70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071433"
---
# <a name="mdm_policy_config01_bitlocker02-class"></a><span data-ttu-id="3a4d6-105">\_Класс политики MDM \_ Config01 \_ BitLocker02</span><span class="sxs-lookup"><span data-stu-id="3a4d6-105">MDM\_Policy\_Config01\_BitLocker02 class</span></span>

<span data-ttu-id="3a4d6-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3a4d6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3a4d6-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3a4d6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3a4d6-108">Класс **\_ политики MDM \_ Config01 \_ Bitlocker02** представляет доступные политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a4d6-108">The **MDM\_Policy\_Config01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="3a4d6-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3a4d6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a4d6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a4d6-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="3a4d6-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3a4d6-111">Members</span></span>

<span data-ttu-id="3a4d6-112">Класс **\_ политики MDM \_ Config01 \_ BitLocker02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3a4d6-112">The **MDM\_Policy\_Config01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="3a4d6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a4d6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a4d6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a4d6-114">Properties</span></span>

<span data-ttu-id="3a4d6-115">Класс **\_ политики MDM \_ Config01 \_ BitLocker02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3a4d6-115">The **MDM\_Policy\_Config01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3a4d6-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="3a4d6-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d6-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3a4d6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d6-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3a4d6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a4d6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a4d6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d6-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a4d6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d6-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a4d6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a4d6-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3a4d6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3a4d6-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="3a4d6-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="3a4d6-124">Для этого класса строка имеет значение "BitLocker".</span><span class="sxs-lookup"><span data-stu-id="3a4d6-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="3a4d6-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3a4d6-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a4d6-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a4d6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a4d6-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a4d6-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a4d6-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3a4d6-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3a4d6-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3a4d6-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="3a4d6-130">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="3a4d6-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a4d6-131">Требования</span><span class="sxs-lookup"><span data-stu-id="3a4d6-131">Requirements</span></span>



| <span data-ttu-id="3a4d6-132">Требование</span><span class="sxs-lookup"><span data-stu-id="3a4d6-132">Requirement</span></span> | <span data-ttu-id="3a4d6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3a4d6-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4d6-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a4d6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4d6-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3a4d6-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a4d6-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a4d6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4d6-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a4d6-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3a4d6-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a4d6-138">Namespace</span></span><br/>                | <span data-ttu-id="3a4d6-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3a4d6-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3a4d6-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3a4d6-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a4d6-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a4d6-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a4d6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3a4d6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a4d6-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a4d6-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4d6-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a4d6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4d6-145">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="3a4d6-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

