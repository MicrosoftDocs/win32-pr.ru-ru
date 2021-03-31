---
title: Класс MDM_Policy_Result01_Search02
description: '\_Класс политики MDM \_ Result01 \_ Search02 представляет доступные политики поиска.'
ms.assetid: 3025753f-a3cc-430c-bc73-438085ef5c51
keywords:
- Класс MDM_Policy_Result01_Search02
- MDM_Policy_Result01_Search02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Search02
- MDM_Policy_Result01_Search02.InstanceID
- MDM_Policy_Result01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a0e25e7f5aa47abcc2b39d9a30a764c5dc9c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071322"
---
# <a name="mdm_policy_result01_search02-class"></a><span data-ttu-id="03b7f-105">\_Класс политики MDM \_ Result01 \_ Search02</span><span class="sxs-lookup"><span data-stu-id="03b7f-105">MDM\_Policy\_Result01\_Search02 class</span></span>

<span data-ttu-id="03b7f-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="03b7f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="03b7f-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="03b7f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="03b7f-108">Класс **\_ политики MDM \_ Result01 \_ Search02** представляет доступные политики поиска.</span><span class="sxs-lookup"><span data-stu-id="03b7f-108">The **MDM\_Policy\_Result01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="03b7f-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="03b7f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03b7f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03b7f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Search02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCloudSearch;
  sint32 AllowSearchToUseLocation;
  sint32 AllowStoringImagesFromVisionSearch;
  sint32 AlwaysUseAutoLangDetection;
  sint32 PreventRemoteQueries;
  sint32 PreventIndexingLowDiskSpaceMB;
  sint32 DisableRemovableDriveIndexing;
  sint32 DisableBackoff;
  sint32 AllowUsingDiacritics;
  sint32 AllowWindowsIndexer;
  sint32 AllowIndexingEncryptedStoresOrItems;
};
```

## <a name="members"></a><span data-ttu-id="03b7f-111">Члены</span><span class="sxs-lookup"><span data-stu-id="03b7f-111">Members</span></span>

<span data-ttu-id="03b7f-112">Класс **\_ политики MDM \_ Result01 \_ Search02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="03b7f-112">The **MDM\_Policy\_Result01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="03b7f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="03b7f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03b7f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="03b7f-114">Properties</span></span>

<span data-ttu-id="03b7f-115">Класс **\_ политики MDM \_ Result01 \_ Search02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="03b7f-115">The **MDM\_Policy\_Result01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="03b7f-116">алловклаудсеарч</span><span class="sxs-lookup"><span data-stu-id="03b7f-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-119">AllowIndexingEncryptedStoresOrItems</span><span class="sxs-lookup"><span data-stu-id="03b7f-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-122">AllowSearchToUseLocation</span><span class="sxs-lookup"><span data-stu-id="03b7f-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-125">алловсторингимажесфромвисионсеарч</span><span class="sxs-lookup"><span data-stu-id="03b7f-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-128">AllowUsingDiacritics</span><span class="sxs-lookup"><span data-stu-id="03b7f-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-131">AllowWindowsIndexer</span><span class="sxs-lookup"><span data-stu-id="03b7f-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-134">AlwaysUseAutoLangDetection</span><span class="sxs-lookup"><span data-stu-id="03b7f-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-137">DisableBackoff</span><span class="sxs-lookup"><span data-stu-id="03b7f-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-140">DisableRemovableDriveIndexing</span><span class="sxs-lookup"><span data-stu-id="03b7f-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="03b7f-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="03b7f-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03b7f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03b7f-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="03b7f-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="03b7f-147">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="03b7f-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="03b7f-148">Для этого класса строка имеет значение "Search".</span><span class="sxs-lookup"><span data-stu-id="03b7f-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="03b7f-149">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="03b7f-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="03b7f-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="03b7f-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="03b7f-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="03b7f-153">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="03b7f-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="03b7f-154">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="03b7f-154">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="03b7f-155">PreventIndexingLowDiskSpaceMB</span><span class="sxs-lookup"><span data-stu-id="03b7f-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="03b7f-158">PreventRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="03b7f-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03b7f-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="03b7f-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="03b7f-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="03b7f-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03b7f-161">Требования</span><span class="sxs-lookup"><span data-stu-id="03b7f-161">Requirements</span></span>



| <span data-ttu-id="03b7f-162">Требование</span><span class="sxs-lookup"><span data-stu-id="03b7f-162">Requirement</span></span> | <span data-ttu-id="03b7f-163">Значение</span><span class="sxs-lookup"><span data-stu-id="03b7f-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b7f-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03b7f-164">Minimum supported client</span></span><br/> | <span data-ttu-id="03b7f-165">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="03b7f-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03b7f-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03b7f-166">Minimum supported server</span></span><br/> | <span data-ttu-id="03b7f-167">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="03b7f-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="03b7f-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03b7f-168">Namespace</span></span><br/>                | <span data-ttu-id="03b7f-169">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="03b7f-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="03b7f-170">MOF</span><span class="sxs-lookup"><span data-stu-id="03b7f-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03b7f-171"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03b7f-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="03b7f-172">DLL</span><span class="sxs-lookup"><span data-stu-id="03b7f-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03b7f-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03b7f-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03b7f-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03b7f-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b7f-175">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="03b7f-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

