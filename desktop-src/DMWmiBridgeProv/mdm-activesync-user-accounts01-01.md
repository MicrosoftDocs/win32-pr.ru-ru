---
title: Класс MDM_ActiveSync_User_Accounts01_01
description: Класс MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01 определяет все доступные учетные записи ActiveSync.
ms.assetid: bcd1fdcb-675a-4833-9d3c-0509e68f7b00
keywords:
- Класс MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_ActiveSync_User_Accounts01_01
- MDM_ActiveSync_User_Accounts01_01.InstanceID
- MDM_ActiveSync_User_Accounts01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a065fb3f33e69b636a35fc848e5d717898f1fa3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490179"
---
# <a name="mdm_activesync_user_accounts01_01-class"></a><span data-ttu-id="6b14d-105">\_ \_ \_ Класс User Accounts01 \_ 01 MDM ActiveSync</span><span class="sxs-lookup"><span data-stu-id="6b14d-105">MDM\_ActiveSync\_User\_Accounts01\_01 class</span></span>

<span data-ttu-id="6b14d-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="6b14d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6b14d-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="6b14d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6b14d-108">Класс **MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01** определяет все доступные учетные записи ActiveSync.</span><span class="sxs-lookup"><span data-stu-id="6b14d-108">The **MDM\_ActiveSync\_User\_Accounts01\_01** class defines all available ActiveSync accounts.</span></span>

<span data-ttu-id="6b14d-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b14d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b14d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b14d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ActiveSync_User_Accounts01_01
{
  string InstanceID;
  string ParentID;
  string EmailAddress;
  string Domain;
  string AccountIcon;
  string AccountType;
  string AccountName;
  string Password;
  string ServerName;
  string UserName;
};
```

## <a name="members"></a><span data-ttu-id="6b14d-111">Члены</span><span class="sxs-lookup"><span data-stu-id="6b14d-111">Members</span></span>

<span data-ttu-id="6b14d-112">Класс **MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6b14d-112">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="6b14d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b14d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b14d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b14d-114">Properties</span></span>

<span data-ttu-id="6b14d-115">Класс **MDM \_ ActiveSync \_ user \_ Accounts01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="6b14d-115">The **MDM\_ActiveSync\_User\_Accounts01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6b14d-116">AccountIcon</span><span class="sxs-lookup"><span data-stu-id="6b14d-116">AccountIcon</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounticon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b14d-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="6b14d-119">AccountName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accountname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b14d-122">AccountType</span><span class="sxs-lookup"><span data-stu-id="6b14d-122">AccountType</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-accounttype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b14d-125">Доменная</span><span class="sxs-lookup"><span data-stu-id="6b14d-125">Domain</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-domain)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b14d-128">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="6b14d-128">EmailAddress</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-emailaddress)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6b14d-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6b14d-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b14d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6b14d-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6b14d-135">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="6b14d-135">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="6b14d-136">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6b14d-136">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b14d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-139">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6b14d-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6b14d-140">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="6b14d-140">Describes the full path to the parent node.</span></span> <span data-ttu-id="6b14d-141">Для этого класса строка имеет значение "./вендор/мсфт/активесинк/"</span><span class="sxs-lookup"><span data-stu-id="6b14d-141">For this class, the string is "./Vendor/MSFT/ActiveSync/"</span></span>

</dd> <dt>

[<span data-ttu-id="6b14d-142">Пароль</span><span class="sxs-lookup"><span data-stu-id="6b14d-142">Password</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b14d-145">ServerName</span><span class="sxs-lookup"><span data-stu-id="6b14d-145">ServerName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-servername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-147">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6b14d-148">UserName</span><span class="sxs-lookup"><span data-stu-id="6b14d-148">UserName</span></span>](/windows/client-management/mdm/activesync-csp#account-guid-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b14d-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6b14d-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6b14d-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6b14d-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b14d-151">Требования</span><span class="sxs-lookup"><span data-stu-id="6b14d-151">Requirements</span></span>



| <span data-ttu-id="6b14d-152">Требование</span><span class="sxs-lookup"><span data-stu-id="6b14d-152">Requirement</span></span> | <span data-ttu-id="6b14d-153">Значение</span><span class="sxs-lookup"><span data-stu-id="6b14d-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b14d-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b14d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="6b14d-155">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="6b14d-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b14d-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b14d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="6b14d-157">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6b14d-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6b14d-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b14d-158">Namespace</span></span><br/>                | <span data-ttu-id="6b14d-159">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="6b14d-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6b14d-160">MOF</span><span class="sxs-lookup"><span data-stu-id="6b14d-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b14d-161"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b14d-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b14d-162">DLL</span><span class="sxs-lookup"><span data-stu-id="6b14d-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b14d-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b14d-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b14d-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b14d-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b14d-165">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="6b14d-165">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

