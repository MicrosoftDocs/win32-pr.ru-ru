---
title: Класс MDM_Policy_Result01_TextInput02
description: '\_Класс политики MDM \_ Result01 \_ TextInput02 представляет доступные входные политики текста.'
ms.assetid: d0ab2d69-6d43-410e-936a-cb87a521d5f3
keywords:
- Класс MDM_Policy_Result01_TextInput02
- MDM_Policy_Result01_TextInput02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_TextInput02
- MDM_Policy_Result01_TextInput02.InstanceID
- MDM_Policy_Result01_TextInput02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a0c02c2afe70f3e7122de0c3d888c42ac179317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490155"
---
# <a name="mdm_policy_result01_textinput02-class"></a><span data-ttu-id="bc3fe-105">\_Класс политики MDM \_ Result01 \_ TextInput02</span><span class="sxs-lookup"><span data-stu-id="bc3fe-105">MDM\_Policy\_Result01\_TextInput02 class</span></span>

<span data-ttu-id="bc3fe-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bc3fe-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="bc3fe-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bc3fe-108">Класс **\_ политики MDM \_ Result01 \_ TextInput02** представляет доступные входные политики текста.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-108">The **MDM\_Policy\_Result01\_TextInput02** class represents the text input policies available.</span></span>

<span data-ttu-id="bc3fe-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3fe-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc3fe-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_TextInput02
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

## <a name="members"></a><span data-ttu-id="bc3fe-111">Члены</span><span class="sxs-lookup"><span data-stu-id="bc3fe-111">Members</span></span>

<span data-ttu-id="bc3fe-112">Класс **\_ политики MDM \_ Result01 \_ TextInput02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bc3fe-112">The **MDM\_Policy\_Result01\_TextInput02** class has these types of members:</span></span>

-   [<span data-ttu-id="bc3fe-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc3fe-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc3fe-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="bc3fe-114">Properties</span></span>

<span data-ttu-id="bc3fe-115">Класс **\_ политики MDM \_ Result01 \_ TextInput02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-115">The **MDM\_Policy\_Result01\_TextInput02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bc3fe-116">AllowIMELogging</span><span class="sxs-lookup"><span data-stu-id="bc3fe-116">AllowIMELogging</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimelogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-119">AllowIMENetworkAccess</span><span class="sxs-lookup"><span data-stu-id="bc3fe-119">AllowIMENetworkAccess</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowimenetworkaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-122">AllowInputPanel</span><span class="sxs-lookup"><span data-stu-id="bc3fe-122">AllowInputPanel</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowinputpanel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-125">AllowJapaneseIMESurrogatePairCharacters</span><span class="sxs-lookup"><span data-stu-id="bc3fe-125">AllowJapaneseIMESurrogatePairCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseimesurrogatepaircharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-128">AllowJapaneseIVSCharacters</span><span class="sxs-lookup"><span data-stu-id="bc3fe-128">AllowJapaneseIVSCharacters</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseivscharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-131">AllowJapaneseNonPublishingStandardGlyph</span><span class="sxs-lookup"><span data-stu-id="bc3fe-131">AllowJapaneseNonPublishingStandardGlyph</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapanesenonpublishingstandardglyph)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-134">AllowJapaneseUserDictionary</span><span class="sxs-lookup"><span data-stu-id="bc3fe-134">AllowJapaneseUserDictionary</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowjapaneseuserdictionary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-137">AllowKeyboardTextSuggestions</span><span class="sxs-lookup"><span data-stu-id="bc3fe-137">AllowKeyboardTextSuggestions</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowkeyboardtextsuggestions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-140">AllowLanguageFeaturesUninstall</span><span class="sxs-lookup"><span data-stu-id="bc3fe-140">AllowLanguageFeaturesUninstall</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-allowlanguagefeaturesuninstall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-143">ExcludeJapaneseIMEExceptJIS0208</span><span class="sxs-lookup"><span data-stu-id="bc3fe-143">ExcludeJapaneseIMEExceptJIS0208</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span><span class="sxs-lookup"><span data-stu-id="bc3fe-146">ExcludeJapaneseIMEExceptJIS0208andEUDC</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptjis0208andeudc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bc3fe-149">ExcludeJapaneseIMEExceptShiftJIS</span><span class="sxs-lookup"><span data-stu-id="bc3fe-149">ExcludeJapaneseIMEExceptShiftJIS</span></span>](/windows/client-management/mdm/policy-csp-textinput#textinput-excludejapaneseimeexceptshiftjis)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bc3fe-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bc3fe-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc3fe-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-155">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc3fe-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc3fe-156">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="bc3fe-157">Для этого класса строка имеет значение "TextInput"</span><span class="sxs-lookup"><span data-stu-id="bc3fe-157">For this class, the string is "TextInput"</span></span>

</dd> <dt>

<span data-ttu-id="bc3fe-158">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-158">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc3fe-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bc3fe-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc3fe-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc3fe-161">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bc3fe-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bc3fe-162">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="bc3fe-162">Describes the full path to the parent node.</span></span> <span data-ttu-id="bc3fe-163">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="bc3fe-163">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc3fe-164">Требования</span><span class="sxs-lookup"><span data-stu-id="bc3fe-164">Requirements</span></span>



| <span data-ttu-id="bc3fe-165">Требование</span><span class="sxs-lookup"><span data-stu-id="bc3fe-165">Requirement</span></span> | <span data-ttu-id="bc3fe-166">Значение</span><span class="sxs-lookup"><span data-stu-id="bc3fe-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3fe-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc3fe-167">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3fe-168">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bc3fe-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bc3fe-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc3fe-169">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3fe-170">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bc3fe-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bc3fe-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bc3fe-171">Namespace</span></span><br/>                | <span data-ttu-id="bc3fe-172">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="bc3fe-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="bc3fe-173">MOF</span><span class="sxs-lookup"><span data-stu-id="bc3fe-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc3fe-174"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc3fe-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc3fe-175">DLL</span><span class="sxs-lookup"><span data-stu-id="bc3fe-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc3fe-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc3fe-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc3fe-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc3fe-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3fe-178">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="bc3fe-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

