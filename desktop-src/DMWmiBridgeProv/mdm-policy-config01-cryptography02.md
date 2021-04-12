---
title: Класс MDM_Policy_Config01_Cryptography02
description: '\_Класс политики MDM \_ Config01 \_ Cryptography02 представляет политики, связанные с шифрованием.'
ms.assetid: e1e06dbd-507e-4da5-bcd5-4d551bd99302
keywords:
- Класс MDM_Policy_Config01_Cryptography02
- MDM_Policy_Config01_Cryptography02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cryptography02
- MDM_Policy_Config01_Cryptography02.InstanceID
- MDM_Policy_Config01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f13a5a04e3d312d8ba262359847719652ecc4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489912"
---
# <a name="mdm_policy_config01_cryptography02-class"></a><span data-ttu-id="c0c81-105">\_Класс политики MDM \_ Config01 \_ Cryptography02</span><span class="sxs-lookup"><span data-stu-id="c0c81-105">MDM\_Policy\_Config01\_Cryptography02 class</span></span>

<span data-ttu-id="c0c81-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="c0c81-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c0c81-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="c0c81-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c0c81-108">Класс **\_ политики MDM \_ Config01 \_ Cryptography02** представляет политики, связанные с шифрованием.</span><span class="sxs-lookup"><span data-stu-id="c0c81-108">The **MDM\_Policy\_Config01\_Cryptography02** class represents policies related to cryptography.</span></span>

<span data-ttu-id="c0c81-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c0c81-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c81-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0c81-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a><span data-ttu-id="c0c81-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c0c81-111">Members</span></span>

<span data-ttu-id="c0c81-112">Класс **\_ политики MDM \_ Config01 \_ Cryptography02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0c81-112">The **MDM\_Policy\_Config01\_Cryptography02** class has these types of members:</span></span>

-   [<span data-ttu-id="c0c81-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0c81-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0c81-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0c81-114">Properties</span></span>

<span data-ttu-id="c0c81-115">Класс **\_ политики MDM \_ Config01 \_ Cryptography02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0c81-115">The **MDM\_Policy\_Config01\_Cryptography02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c0c81-116">AllowFipsAlgorithmPolicy</span><span class="sxs-lookup"><span data-stu-id="c0c81-116">AllowFipsAlgorithmPolicy</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0c81-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c0c81-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0c81-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0c81-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c0c81-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c0c81-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0c81-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0c81-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0c81-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0c81-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0c81-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0c81-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0c81-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="c0c81-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="c0c81-124">Для этого класса строка имеет значение "Cryptography"</span><span class="sxs-lookup"><span data-stu-id="c0c81-124">For this class, the string is "Cryptography"</span></span>

</dd> <dt>

<span data-ttu-id="c0c81-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c0c81-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0c81-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0c81-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0c81-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0c81-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0c81-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0c81-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0c81-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="c0c81-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="c0c81-130">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="c0c81-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="c0c81-131">тлсЦиферсуитес</span><span class="sxs-lookup"><span data-stu-id="c0c81-131">TLSCipherSuites</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0c81-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0c81-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0c81-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c0c81-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0c81-134">Требования</span><span class="sxs-lookup"><span data-stu-id="c0c81-134">Requirements</span></span>



| <span data-ttu-id="c0c81-135">Требование</span><span class="sxs-lookup"><span data-stu-id="c0c81-135">Requirement</span></span> | <span data-ttu-id="c0c81-136">Значение</span><span class="sxs-lookup"><span data-stu-id="c0c81-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0c81-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0c81-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c0c81-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c0c81-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0c81-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0c81-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c0c81-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0c81-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c0c81-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0c81-141">Namespace</span></span><br/>                | <span data-ttu-id="c0c81-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="c0c81-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c0c81-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c0c81-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0c81-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0c81-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0c81-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c0c81-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0c81-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0c81-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0c81-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0c81-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c81-148">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="c0c81-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

