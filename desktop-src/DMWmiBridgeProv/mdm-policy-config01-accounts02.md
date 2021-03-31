---
title: Класс MDM_Policy_Config01_Accounts02
description: '\_Класс политики MDM \_ Config01 \_ Accounts02 представляет политики, связанные с учетными записями.'
ms.assetid: 628a0745-0ac5-4038-8ea8-04344098682d
keywords:
- Класс MDM_Policy_Config01_Accounts02
- MDM_Policy_Config01_Accounts02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Accounts02
- MDM_Policy_Config01_Accounts02.InstanceID
- MDM_Policy_Config01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8833f1477014f3c7c2200e07c242549f5235fbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071437"
---
# <a name="mdm_policy_config01_accounts02-class"></a><span data-ttu-id="73e79-105">\_Класс политики MDM \_ Config01 \_ Accounts02</span><span class="sxs-lookup"><span data-stu-id="73e79-105">MDM\_Policy\_Config01\_Accounts02 class</span></span>

<span data-ttu-id="73e79-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="73e79-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="73e79-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="73e79-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="73e79-108">Класс **\_ политики MDM \_ Config01 \_ Accounts02** представляет политики, связанные с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="73e79-108">The **MDM\_Policy\_Config01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="73e79-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="73e79-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e79-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73e79-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="73e79-111">Члены</span><span class="sxs-lookup"><span data-stu-id="73e79-111">Members</span></span>

<span data-ttu-id="73e79-112">Класс **\_ политики MDM \_ Config01 \_ Accounts02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="73e79-112">The **MDM\_Policy\_Config01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="73e79-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="73e79-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73e79-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="73e79-114">Properties</span></span>

<span data-ttu-id="73e79-115">Класс **\_ политики MDM \_ Config01 \_ Accounts02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="73e79-115">The **MDM\_Policy\_Config01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="73e79-116">алловаддингнонмикрософтаккаунтсмануалли</span><span class="sxs-lookup"><span data-stu-id="73e79-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e79-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="73e79-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="73e79-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="73e79-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="73e79-119">AllowMicrosoftAccountConnection</span><span class="sxs-lookup"><span data-stu-id="73e79-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e79-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="73e79-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="73e79-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="73e79-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="73e79-122">алловмикрософтаккаунтсигнинассистант</span><span class="sxs-lookup"><span data-stu-id="73e79-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e79-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="73e79-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="73e79-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="73e79-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e79-125">DomainNamesForEmailSync</span><span class="sxs-lookup"><span data-stu-id="73e79-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e79-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73e79-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e79-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="73e79-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="73e79-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="73e79-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e79-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73e79-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e79-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73e79-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e79-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73e79-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="73e79-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="73e79-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="73e79-133">Для этого класса строка имеет значение Accounts.</span><span class="sxs-lookup"><span data-stu-id="73e79-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="73e79-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="73e79-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73e79-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="73e79-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73e79-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="73e79-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73e79-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="73e79-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="73e79-138">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="73e79-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="73e79-139">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="73e79-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73e79-140">Требования</span><span class="sxs-lookup"><span data-stu-id="73e79-140">Requirements</span></span>



| <span data-ttu-id="73e79-141">Требование</span><span class="sxs-lookup"><span data-stu-id="73e79-141">Requirement</span></span> | <span data-ttu-id="73e79-142">Значение</span><span class="sxs-lookup"><span data-stu-id="73e79-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e79-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73e79-143">Minimum supported client</span></span><br/> | <span data-ttu-id="73e79-144">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="73e79-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73e79-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73e79-145">Minimum supported server</span></span><br/> | <span data-ttu-id="73e79-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="73e79-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="73e79-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73e79-147">Namespace</span></span><br/>                | <span data-ttu-id="73e79-148">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="73e79-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="73e79-149">MOF</span><span class="sxs-lookup"><span data-stu-id="73e79-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73e79-150"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73e79-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="73e79-151">DLL</span><span class="sxs-lookup"><span data-stu-id="73e79-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73e79-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73e79-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73e79-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73e79-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73e79-154">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="73e79-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

