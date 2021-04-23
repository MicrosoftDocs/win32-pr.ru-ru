---
title: Класс MDM_ActiveSync_User_Options03
description: '\_ \_ Класс OPTIONS03 пользователя MDM ActiveSync \_ определяет параметры, заданные для каждой учетной записи ActiveSync.'
ms.assetid: b325f676-9b83-4212-a228-e2d774515be6
keywords:
- Класс MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03 класс, описание
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Options03
- MDM_ActiveSync_User_Options03.InstanceID
- MDM_ActiveSync_User_Options03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c459e20b519801c622a091060fd6a87ced2807c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135691"
---
# <a name="mdm_activesync_user_options03-class"></a><span data-ttu-id="a83b9-105">\_ \_ Класс OPTIONS03 пользователя MDM ActiveSync \_</span><span class="sxs-lookup"><span data-stu-id="a83b9-105">MDM\_ActiveSync\_User\_Options03 class</span></span>

<span data-ttu-id="a83b9-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a83b9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a83b9-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a83b9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a83b9-108">Класс **\_ \_ \_ Options03 пользователя MDM ActiveSync** определяет параметры, заданные для каждой учетной записи ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="a83b9-108">The **MDM\_ActiveSync\_User\_Options03** class defines the options that are set for each ActiveSync account.</span></span>

<span data-ttu-id="a83b9-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a83b9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a83b9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a83b9-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Options03
{
  string InstanceID;
  string ParentID;
  string UseSSL;
  string Schedule;
  string MailAgeFilter;
  string Logging;
};
```

## <a name="members"></a><span data-ttu-id="a83b9-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a83b9-111">Members</span></span>

<span data-ttu-id="a83b9-112">Класс **\_ \_ \_ Options03 пользователя MDM ActiveSync** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a83b9-112">The **MDM\_ActiveSync\_User\_Options03** class has these types of members:</span></span>

-   [<span data-ttu-id="a83b9-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a83b9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a83b9-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a83b9-114">Properties</span></span>

<span data-ttu-id="a83b9-115">Класс **\_ \_ \_ Options03 пользователя MDM ActiveSync** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a83b9-115">The **MDM\_ActiveSync\_User\_Options03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a83b9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a83b9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b9-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a83b9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a83b9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a83b9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a83b9-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="a83b9-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="a83b9-121">Logging</span><span class="sxs-lookup"><span data-stu-id="a83b9-121">Logging</span></span>](/windows/client-management/mdm/activesync-csp#options-logging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b9-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a83b9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a83b9-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a83b9-124">MailAgeFilter</span><span class="sxs-lookup"><span data-stu-id="a83b9-124">MailAgeFilter</span></span>](/windows/client-management/mdm/activesync-csp#options-mailagefilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b9-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a83b9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a83b9-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a83b9-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a83b9-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b9-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a83b9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a83b9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-130">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a83b9-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a83b9-131">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="a83b9-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="a83b9-132">Для этого класса строка имеет значение "./вендор/мсфт/активесинк/аккаунтс/*GUID*/"</span><span class="sxs-lookup"><span data-stu-id="a83b9-132">For this class, the string is "./Vendor/MSFT/ActiveSync/Accounts/*GUID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="a83b9-133">Расписание</span><span class="sxs-lookup"><span data-stu-id="a83b9-133">Schedule</span></span>](/windows/client-management/mdm/activesync-csp#options-schedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b9-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a83b9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a83b9-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a83b9-136">UseSSL</span><span class="sxs-lookup"><span data-stu-id="a83b9-136">UseSSL</span></span>](/windows/client-management/mdm/activesync-csp#options-usessl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a83b9-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a83b9-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a83b9-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a83b9-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a83b9-139">Требования</span><span class="sxs-lookup"><span data-stu-id="a83b9-139">Requirements</span></span>



| <span data-ttu-id="a83b9-140">Требование</span><span class="sxs-lookup"><span data-stu-id="a83b9-140">Requirement</span></span> | <span data-ttu-id="a83b9-141">Значение</span><span class="sxs-lookup"><span data-stu-id="a83b9-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a83b9-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a83b9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a83b9-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a83b9-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a83b9-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a83b9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a83b9-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a83b9-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a83b9-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a83b9-146">Namespace</span></span><br/>                | <span data-ttu-id="a83b9-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="a83b9-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a83b9-148">MOF</span><span class="sxs-lookup"><span data-stu-id="a83b9-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a83b9-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a83b9-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a83b9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="a83b9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a83b9-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a83b9-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a83b9-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a83b9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83b9-153">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="a83b9-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

