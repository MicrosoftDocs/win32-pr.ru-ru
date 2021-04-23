---
title: Класс MDM_Policy_User_Config01_Authentication02
description: '\_Класс политики MDM \_ user \_ Config01 \_ Authentication02 представляет доступные политики управления аутентификацией.'
ms.assetid: 66d94f97-07ea-4025-95f9-d55282df3661
keywords:
- Класс MDM_Policy_User_Config01_Authentication02
- MDM_Policy_User_Config01_Authentication02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Authentication02
- MDM_Policy_User_Config01_Authentication02.InstanceID
- MDM_Policy_User_Config01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d278ad679f97047d0a4cf7e95eeb2eee0695e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989048"
---
# <a name="mdm_policy_user_config01_authentication02-class"></a><span data-ttu-id="620fe-105">\_Класс политики MDM \_ user \_ Config01 \_ Authentication02</span><span class="sxs-lookup"><span data-stu-id="620fe-105">MDM\_Policy\_User\_Config01\_Authentication02 class</span></span>

<span data-ttu-id="620fe-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="620fe-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="620fe-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="620fe-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="620fe-108">Класс **\_ политики MDM \_ user \_ Config01 \_ Authentication02** представляет доступные политики управления аутентификацией.</span><span class="sxs-lookup"><span data-stu-id="620fe-108">The **MDM\_Policy\_User\_Config01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="620fe-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="620fe-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="620fe-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="620fe-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEAPCertSSO;
};
```

## <a name="members"></a><span data-ttu-id="620fe-111">Члены</span><span class="sxs-lookup"><span data-stu-id="620fe-111">Members</span></span>

<span data-ttu-id="620fe-112">Класс **\_ \_ user \_ Config01 \_ Authentication02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="620fe-112">The **MDM\_Policy\_User\_Config01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="620fe-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="620fe-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="620fe-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="620fe-114">Properties</span></span>

<span data-ttu-id="620fe-115">Класс **\_ \_ user \_ Config01 \_ Authentication02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="620fe-115">The **MDM\_Policy\_User\_Config01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="620fe-116">алловеапцертссо</span><span class="sxs-lookup"><span data-stu-id="620fe-116">AllowEAPCertSSO</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-alloweapcertsso)
</dt> <dd> <dl> <dt>

<span data-ttu-id="620fe-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="620fe-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="620fe-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="620fe-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="620fe-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="620fe-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="620fe-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="620fe-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="620fe-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="620fe-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="620fe-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="620fe-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="620fe-123">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="620fe-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="620fe-124">Для этого класса строка имеет значение Authentication.</span><span class="sxs-lookup"><span data-stu-id="620fe-124">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="620fe-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="620fe-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="620fe-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="620fe-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="620fe-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="620fe-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="620fe-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="620fe-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="620fe-129">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="620fe-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="620fe-130">Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="620fe-130">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="620fe-131">Требования</span><span class="sxs-lookup"><span data-stu-id="620fe-131">Requirements</span></span>



| <span data-ttu-id="620fe-132">Требование</span><span class="sxs-lookup"><span data-stu-id="620fe-132">Requirement</span></span> | <span data-ttu-id="620fe-133">Значение</span><span class="sxs-lookup"><span data-stu-id="620fe-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620fe-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="620fe-134">Minimum supported client</span></span><br/> | <span data-ttu-id="620fe-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="620fe-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="620fe-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="620fe-136">Minimum supported server</span></span><br/> | <span data-ttu-id="620fe-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="620fe-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="620fe-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="620fe-138">Namespace</span></span><br/>                | <span data-ttu-id="620fe-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="620fe-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="620fe-140">MOF</span><span class="sxs-lookup"><span data-stu-id="620fe-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="620fe-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="620fe-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="620fe-142">DLL</span><span class="sxs-lookup"><span data-stu-id="620fe-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="620fe-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="620fe-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="620fe-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="620fe-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620fe-145">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="620fe-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

