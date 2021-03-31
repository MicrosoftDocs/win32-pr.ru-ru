---
title: Класс MDM_Policy_Config01_TextInput02
description: '\_Класс политики MDM \_ Config01 \_ TextInput02 представляет доступные входные политики текста.'
ms.assetid: e5a8d331-40ec-49f2-aedd-5941fe59092f
keywords:
- Класс MDM_Policy_Config01_TextInput02
- MDM_Policy_Config01_TextInput02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_TextInput02
- MDM_Policy_Config01_TextInput02.InstanceID
- MDM_Policy_Config01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f79d750973edf501ca292d042e04bf4dc27ef42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490812"
---
# <a name="mdm_policy_config01_textinput02-class"></a><span data-ttu-id="4e1b0-105">\_Класс политики MDM \_ Config01 \_ TextInput02</span><span class="sxs-lookup"><span data-stu-id="4e1b0-105">MDM\_Policy\_Config01\_TextInput02 class</span></span>

<span data-ttu-id="4e1b0-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4e1b0-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4e1b0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4e1b0-108">Класс **\_ политики MDM \_ Config01 \_ TextInput02** представляет доступные входные политики текста.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-108">The **MDM\_Policy\_Config01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="4e1b0-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1b0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e1b0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_TextInput02
{
  string InstanceID;
  string ParentID;
  sint32 AllowIMENetworkAccess;
  sint32 AllowIMELogging;
  sint32 AllowJapaneseNonPublishingStandardGlyph;
  sint32 AllowJapaneseIVSCharacters;
  sint32 AllowJapaneseUserDictionary;
  sint32 AllowKeyboardTextSuggestions;
  sint32 AllowJapaneseIMESurrogatePairCharacters;
  sint32 ExcludeJapaneseIMEExceptShiftJIS;
  sint32 ExcludeJapaneseIMEExceptJIS0208;
  sint32 ExcludeJapaneseIMEExceptJIS0208andEUDC;
  sint32 AllowLanguageFeaturesUninstall;
  sint32 AllowInputPanel;
};
```

## <a name="members"></a><span data-ttu-id="4e1b0-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4e1b0-111">Members</span></span>

<span data-ttu-id="4e1b0-112">Класс **\_ политики MDM \_ Config01 \_ TextInput02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4e1b0-112">The **MDM\_Policy\_Config01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="4e1b0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e1b0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e1b0-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4e1b0-114">Properties</span></span>

<span data-ttu-id="4e1b0-115">Класс **\_ политики MDM \_ Config01 \_ TextInput02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-115">The **MDM\_Policy\_Config01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4e1b0-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="4e1b0-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-119">AllowIMENetworkAccess</span><span class="sxs-lookup"><span data-stu-id="4e1b0-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-122">AllowInputPanel</span><span class="sxs-lookup"><span data-stu-id="4e1b0-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-125">AllowJapaneseIMESurrogatePairCharacters</span><span class="sxs-lookup"><span data-stu-id="4e1b0-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-128">AllowJapaneseIVSCharacters</span><span class="sxs-lookup"><span data-stu-id="4e1b0-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-131">AllowJapaneseNonPublishingStandardGlyph</span><span class="sxs-lookup"><span data-stu-id="4e1b0-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-134">AllowJapaneseUserDictionary</span><span class="sxs-lookup"><span data-stu-id="4e1b0-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-137">AllowKeyboardTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="4e1b0-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-140">AllowLanguageFeaturesUninstall</span><span class="sxs-lookup"><span data-stu-id="4e1b0-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-143">ExcludeJapaneseIMEExceptJIS0208</span><span class="sxs-lookup"><span data-stu-id="4e1b0-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span><span class="sxs-lookup"><span data-stu-id="4e1b0-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4e1b0-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="4e1b0-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4e1b0-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4e1b0-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4e1b0-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-155">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e1b0-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e1b0-156">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="4e1b0-157">Для этого класса строка имеет значение "TextInput"</span><span class="sxs-lookup"><span data-stu-id="4e1b0-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="4e1b0-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e1b0-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4e1b0-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4e1b0-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e1b0-161">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4e1b0-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4e1b0-162">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="4e1b0-163">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="4e1b0-163">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e1b0-164">Требования</span><span class="sxs-lookup"><span data-stu-id="4e1b0-164">Requirements</span></span>



| <span data-ttu-id="4e1b0-165">Требование</span><span class="sxs-lookup"><span data-stu-id="4e1b0-165">Requirement</span></span> | <span data-ttu-id="4e1b0-166">Значение</span><span class="sxs-lookup"><span data-stu-id="4e1b0-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1b0-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e1b0-167">Minimum supported client</span></span><br/> | <span data-ttu-id="4e1b0-168">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4e1b0-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e1b0-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e1b0-169">Minimum supported server</span></span><br/> | <span data-ttu-id="4e1b0-170">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e1b0-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4e1b0-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e1b0-171">Namespace</span></span><br/>                | <span data-ttu-id="4e1b0-172">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4e1b0-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="4e1b0-173">MOF</span><span class="sxs-lookup"><span data-stu-id="4e1b0-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e1b0-174"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e1b0-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e1b0-175">DLL</span><span class="sxs-lookup"><span data-stu-id="4e1b0-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e1b0-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e1b0-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1b0-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e1b0-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1b0-178">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="4e1b0-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

