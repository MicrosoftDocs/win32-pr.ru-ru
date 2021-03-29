---
title: Класс MDM_Policy_Result01_BitLocker02
description: '\_Класс политики MDM \_ Result01 \_ Bitlocker02 представляет доступные политики BitLocker.'
ms.assetid: 5b20a129-65a8-4ec1-b938-57ddaca46ac3
keywords:
- Класс MDM_Policy_Result01_BitLocker02
- MDM_Policy_Result01_BitLocker02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_BitLocker02
- MDM_Policy_Result01_BitLocker02.InstanceID
- MDM_Policy_Result01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b063ab67411d8be7fc4c819934b63c0af0096ec5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492963"
---
# <a name="mdm_policy_result01_bitlocker02-class"></a><span data-ttu-id="f5393-105">\_Класс политики MDM \_ Result01 \_ BitLocker02</span><span class="sxs-lookup"><span data-stu-id="f5393-105">MDM\_Policy\_Result01\_BitLocker02 class</span></span>

<span data-ttu-id="f5393-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f5393-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f5393-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f5393-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f5393-108">Класс **\_ политики MDM \_ Result01 \_ Bitlocker02** представляет доступные политики BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f5393-108">The **MDM\_Policy\_Result01\_Bitlocker02** class represents the BitLocker policies available.</span></span>

<span data-ttu-id="f5393-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f5393-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5393-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5393-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a><span data-ttu-id="f5393-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f5393-111">Members</span></span>

<span data-ttu-id="f5393-112">Класс **\_ политики MDM \_ Result01 \_ BitLocker02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f5393-112">The **MDM\_Policy\_Result01\_BitLocker02** class has these types of members:</span></span>

-   [<span data-ttu-id="f5393-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5393-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5393-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5393-114">Properties</span></span>

<span data-ttu-id="f5393-115">Класс **\_ политики MDM \_ Result01 \_ BitLocker02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f5393-115">The **MDM\_Policy\_Result01\_BitLocker02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f5393-116">EncryptionMethod</span><span class="sxs-lookup"><span data-stu-id="f5393-116">EncryptionMethod</span></span>](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5393-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f5393-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5393-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f5393-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f5393-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f5393-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5393-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5393-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5393-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5393-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5393-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5393-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5393-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f5393-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="f5393-124">Для этого класса строка имеет значение "BitLocker".</span><span class="sxs-lookup"><span data-stu-id="f5393-124">For this class, the string is "BitLocker"</span></span>

</dd> <dt>

<span data-ttu-id="f5393-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f5393-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5393-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5393-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5393-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5393-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5393-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5393-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5393-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f5393-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="f5393-130">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="f5393-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5393-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f5393-131">Requirements</span></span>



| <span data-ttu-id="f5393-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f5393-132">Requirement</span></span> | <span data-ttu-id="f5393-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f5393-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5393-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5393-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f5393-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f5393-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5393-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5393-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f5393-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5393-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f5393-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5393-138">Namespace</span></span><br/>                | <span data-ttu-id="f5393-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f5393-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f5393-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f5393-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5393-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5393-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5393-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f5393-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5393-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5393-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5393-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5393-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5393-145">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="f5393-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

