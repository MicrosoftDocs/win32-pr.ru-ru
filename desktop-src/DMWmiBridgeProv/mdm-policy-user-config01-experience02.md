---
title: Класс MDM_Policy_User_Config01_Experience02
description: '\_Класс политики MDM \_ user \_ Config01 \_ Experience02 представляет доступные политики взаимодействия.'
ms.assetid: 61a5f093-812a-4fcb-940d-d5f0de7f8c5f
keywords:
- Класс MDM_Policy_User_Config01_Experience02
- MDM_Policy_User_Config01_Experience02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Experience02
- MDM_Policy_User_Config01_Experience02.InstanceID
- MDM_Policy_User_Config01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a982728a3b2f2a899cdbdbd6239a29c5310a258e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491736"
---
# <a name="mdm_policy_user_config01_experience02-class"></a><span data-ttu-id="3dcfd-105">\_Класс политики MDM \_ user \_ Config01 \_ Experience02</span><span class="sxs-lookup"><span data-stu-id="3dcfd-105">MDM\_Policy\_User\_Config01\_Experience02 class</span></span>

<span data-ttu-id="3dcfd-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="3dcfd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3dcfd-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="3dcfd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3dcfd-108">Класс **\_ политики MDM \_ user \_ Config01 \_ Experience02** представляет доступные политики взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="3dcfd-108">The **MDM\_Policy\_User\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="3dcfd-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3dcfd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dcfd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dcfd-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a><span data-ttu-id="3dcfd-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3dcfd-111">Members</span></span>

<span data-ttu-id="3dcfd-112">Класс **\_ \_ user \_ Config01 \_ Experience02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3dcfd-112">The **MDM\_Policy\_User\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="3dcfd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dcfd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3dcfd-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dcfd-114">Properties</span></span>

<span data-ttu-id="3dcfd-115">Класс **\_ \_ user \_ Config01 \_ Experience02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="3dcfd-115">The **MDM\_Policy\_User\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3dcfd-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="3dcfd-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dcfd-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3dcfd-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="3dcfd-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dcfd-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3dcfd-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="3dcfd-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dcfd-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3dcfd-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="3dcfd-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dcfd-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3dcfd-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="3dcfd-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dcfd-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3dcfd-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="3dcfd-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dcfd-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3dcfd-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="3dcfd-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dcfd-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3dcfd-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3dcfd-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3dcfd-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3dcfd-141">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="3dcfd-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="3dcfd-142">Для этого класса строка имеет значение "Experience".</span><span class="sxs-lookup"><span data-stu-id="3dcfd-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="3dcfd-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dcfd-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3dcfd-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3dcfd-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dcfd-146">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3dcfd-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3dcfd-147">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="3dcfd-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="3dcfd-148">Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="3dcfd-148">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3dcfd-149">Требования</span><span class="sxs-lookup"><span data-stu-id="3dcfd-149">Requirements</span></span>



| <span data-ttu-id="3dcfd-150">Требование</span><span class="sxs-lookup"><span data-stu-id="3dcfd-150">Requirement</span></span> | <span data-ttu-id="3dcfd-151">Значение</span><span class="sxs-lookup"><span data-stu-id="3dcfd-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcfd-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dcfd-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3dcfd-153">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3dcfd-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3dcfd-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dcfd-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3dcfd-155">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3dcfd-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="3dcfd-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3dcfd-156">Namespace</span></span><br/>                | <span data-ttu-id="3dcfd-157">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="3dcfd-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="3dcfd-158">MOF</span><span class="sxs-lookup"><span data-stu-id="3dcfd-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dcfd-159"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dcfd-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="3dcfd-160">DLL</span><span class="sxs-lookup"><span data-stu-id="3dcfd-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dcfd-161"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dcfd-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

