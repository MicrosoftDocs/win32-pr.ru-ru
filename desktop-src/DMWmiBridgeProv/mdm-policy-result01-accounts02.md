---
title: Класс MDM_Policy_Result01_Accounts02
description: '\_Класс политики MDM \_ Result01 \_ Accounts02 представляет политики, связанные с учетными записями.'
ms.assetid: 581d63de-6ea8-4c4a-8b94-06228ed07371
keywords:
- Класс MDM_Policy_Result01_Accounts02
- MDM_Policy_Result01_Accounts02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Accounts02
- MDM_Policy_Result01_Accounts02.InstanceID
- MDM_Policy_Result01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c240f9cd4d3703122c0ea051f35ec8326e2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802399"
---
# <a name="mdm_policy_result01_accounts02-class"></a><span data-ttu-id="29a8a-105">\_Класс политики MDM \_ Result01 \_ Accounts02</span><span class="sxs-lookup"><span data-stu-id="29a8a-105">MDM\_Policy\_Result01\_Accounts02 class</span></span>

<span data-ttu-id="29a8a-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="29a8a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="29a8a-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="29a8a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="29a8a-108">Класс **\_ политики MDM \_ Result01 \_ Accounts02** представляет политики, связанные с учетными записями.</span><span class="sxs-lookup"><span data-stu-id="29a8a-108">The **MDM\_Policy\_Result01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="29a8a-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="29a8a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a8a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29a8a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="29a8a-111">Члены</span><span class="sxs-lookup"><span data-stu-id="29a8a-111">Members</span></span>

<span data-ttu-id="29a8a-112">Класс **\_ политики MDM \_ Result01 \_ Accounts02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="29a8a-112">The **MDM\_Policy\_Result01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="29a8a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="29a8a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29a8a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="29a8a-114">Properties</span></span>

<span data-ttu-id="29a8a-115">Класс **\_ политики MDM \_ Result01 \_ Accounts02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="29a8a-115">The **MDM\_Policy\_Result01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="29a8a-116">алловаддингнонмикрософтаккаунтсмануалли</span><span class="sxs-lookup"><span data-stu-id="29a8a-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a8a-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="29a8a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="29a8a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29a8a-119">AllowMicrosoftAccountConnection</span><span class="sxs-lookup"><span data-stu-id="29a8a-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a8a-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="29a8a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="29a8a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="29a8a-122">алловмикрософтаккаунтсигнинассистант</span><span class="sxs-lookup"><span data-stu-id="29a8a-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a8a-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="29a8a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="29a8a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29a8a-125">DomainNamesForEmailSync</span><span class="sxs-lookup"><span data-stu-id="29a8a-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a8a-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="29a8a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="29a8a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="29a8a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="29a8a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a8a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="29a8a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="29a8a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="29a8a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="29a8a-132">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="29a8a-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="29a8a-133">Для этого класса строка имеет значение Accounts.</span><span class="sxs-lookup"><span data-stu-id="29a8a-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="29a8a-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="29a8a-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="29a8a-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="29a8a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="29a8a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="29a8a-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="29a8a-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="29a8a-138">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="29a8a-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="29a8a-139">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="29a8a-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29a8a-140">Требования</span><span class="sxs-lookup"><span data-stu-id="29a8a-140">Requirements</span></span>



| <span data-ttu-id="29a8a-141">Требование</span><span class="sxs-lookup"><span data-stu-id="29a8a-141">Requirement</span></span> | <span data-ttu-id="29a8a-142">Значение</span><span class="sxs-lookup"><span data-stu-id="29a8a-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a8a-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29a8a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="29a8a-144">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="29a8a-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="29a8a-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29a8a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="29a8a-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="29a8a-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="29a8a-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="29a8a-147">Namespace</span></span><br/>                | <span data-ttu-id="29a8a-148">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="29a8a-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="29a8a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="29a8a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29a8a-150"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29a8a-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="29a8a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="29a8a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29a8a-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29a8a-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29a8a-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29a8a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a8a-154">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="29a8a-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

