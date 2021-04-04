---
title: Класс MDM_PassportForWork_PINComplexity03
description: Класс MDM \_ пасспортфорворк \_ PINComplexity03 определяет сложность ПИН-кода для учетных данных входа для Windows Hello для бизнеса.
ms.assetid: 83dcf859-03da-4508-b809-bafd24dc8bd4
keywords:
- Класс MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03 класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork_PINComplexity03
- MDM_PassportForWork_PINComplexity03.InstanceID
- MDM_PassportForWork_PINComplexity03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a9d01cd152935a1daa0a9b0721ea27129e21934
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988462"
---
# <a name="mdm_passportforwork_pincomplexity03-class"></a><span data-ttu-id="523f3-105">\_Класс MDM пасспортфорворк \_ PINComplexity03</span><span class="sxs-lookup"><span data-stu-id="523f3-105">MDM\_PassportForWork\_PINComplexity03 class</span></span>

<span data-ttu-id="523f3-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="523f3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="523f3-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="523f3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="523f3-108">Класс **MDM \_ пасспортфорворк \_ PINComplexity03** определяет сложность ПИН-кода для учетных данных входа для Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="523f3-108">The **MDM\_PassportForWork\_PINComplexity03** class defines the PIN complexity for the logon credentials for Windows Hello for Business.</span></span>

<span data-ttu-id="523f3-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="523f3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="523f3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="523f3-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_PINComplexity03
{
  string InstanceID;
  string ParentID;
  sint32 MinimumPINLength;
  sint32 MaximumPINLength;
  sint32 UppercaseLetters;
  sint32 LowercaseLetters;
  sint32 SpecialCharacters;
  sint32 Digits;
  sint32 History;
  sint32 Expiration;
};
```

## <a name="members"></a><span data-ttu-id="523f3-111">Члены</span><span class="sxs-lookup"><span data-stu-id="523f3-111">Members</span></span>

<span data-ttu-id="523f3-112">Класс **MDM \_ пасспортфорворк \_ PINComplexity03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="523f3-112">The **MDM\_PassportForWork\_PINComplexity03** class has these types of members:</span></span>

-   [<span data-ttu-id="523f3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="523f3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="523f3-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="523f3-114">Properties</span></span>

<span data-ttu-id="523f3-115">Класс **MDM \_ пасспортфорворк \_ PINComplexity03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="523f3-115">The **MDM\_PassportForWork\_PINComplexity03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="523f3-116">Четырехзначным</span><span class="sxs-lookup"><span data-stu-id="523f3-116">Digits</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-digits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="523f3-119">Истечение срока</span><span class="sxs-lookup"><span data-stu-id="523f3-119">Expiration</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-expiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="523f3-122">Журнал</span><span class="sxs-lookup"><span data-stu-id="523f3-122">History</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-history)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="523f3-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="523f3-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="523f3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="523f3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="523f3-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="523f3-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="523f3-129">Корневой узел для политик закрепления.</span><span class="sxs-lookup"><span data-stu-id="523f3-129">Root node for PIN policies.</span></span>

</dd> <dt>

[<span data-ttu-id="523f3-130">ловеркаселеттерс</span><span class="sxs-lookup"><span data-stu-id="523f3-130">LowercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-lowercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="523f3-133">максимумпинленгс</span><span class="sxs-lookup"><span data-stu-id="523f3-133">MaximumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-maximumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-134">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="523f3-136">минимумпинленгс</span><span class="sxs-lookup"><span data-stu-id="523f3-136">MinimumPINLength</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-minimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-137">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-137">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="523f3-139">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="523f3-139">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="523f3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="523f3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="523f3-142">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="523f3-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="523f3-143">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="523f3-143">Describes the full path to the parent node.</span></span> <span data-ttu-id="523f3-144">Для этого класса строка имеет значение "./вендор/мсфт/пасспортфорворк/*TenantID*/полиЦиес"</span><span class="sxs-lookup"><span data-stu-id="523f3-144">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*/Policies"</span></span>

</dd> <dt>

[<span data-ttu-id="523f3-145">спеЦиалчарактерс</span><span class="sxs-lookup"><span data-stu-id="523f3-145">SpecialCharacters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-specialcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-146">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="523f3-148">упперкаселеттерс</span><span class="sxs-lookup"><span data-stu-id="523f3-148">UppercaseLetters</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-pincomplexity-uppercaseletters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="523f3-149">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="523f3-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="523f3-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="523f3-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="523f3-151">Требования</span><span class="sxs-lookup"><span data-stu-id="523f3-151">Requirements</span></span>



| <span data-ttu-id="523f3-152">Требование</span><span class="sxs-lookup"><span data-stu-id="523f3-152">Requirement</span></span> | <span data-ttu-id="523f3-153">Значение</span><span class="sxs-lookup"><span data-stu-id="523f3-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="523f3-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="523f3-154">Minimum supported client</span></span><br/> | <span data-ttu-id="523f3-155">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="523f3-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="523f3-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="523f3-156">Minimum supported server</span></span><br/> | <span data-ttu-id="523f3-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="523f3-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="523f3-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="523f3-158">Namespace</span></span><br/>                | <span data-ttu-id="523f3-159">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="523f3-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="523f3-160">MOF</span><span class="sxs-lookup"><span data-stu-id="523f3-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="523f3-161"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="523f3-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="523f3-162">DLL</span><span class="sxs-lookup"><span data-stu-id="523f3-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="523f3-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="523f3-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="523f3-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="523f3-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523f3-165">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="523f3-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

