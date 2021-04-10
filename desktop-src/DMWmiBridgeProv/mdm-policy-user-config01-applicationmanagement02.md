---
title: Класс MDM_Policy_User_Config01_ApplicationManagement02
description: '\_ \_ \_ Класс User CONFIG01 ApplicationManagement02 политики MDM \_ представляет доступные политики запуска, заданные для каждого пользователя.'
ms.assetid: 3dd20364-6723-4ed6-87c0-729789ddd948
keywords:
- Класс MDM_Policy_User_Config01_ApplicationManagement02
- MDM_Policy_User_Config01_ApplicationManagement02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_ApplicationManagement02
- MDM_Policy_User_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88226122eefb3335ef1b19680268ea5acf1d5388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135199"
---
# <a name="mdm_policy_user_config01_applicationmanagement02-class"></a><span data-ttu-id="1ce46-105">\_Класс политики MDM \_ user \_ Config01 \_ ApplicationManagement02</span><span class="sxs-lookup"><span data-stu-id="1ce46-105">MDM\_Policy\_User\_Config01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="1ce46-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="1ce46-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1ce46-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="1ce46-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1ce46-108">Класс **\_ \_ user \_ Config01 \_ ApplicationManagement02 политики MDM** представляет доступные политики запуска, заданные для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="1ce46-108">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="1ce46-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1ce46-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce46-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ce46-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a><span data-ttu-id="1ce46-111">Члены</span><span class="sxs-lookup"><span data-stu-id="1ce46-111">Members</span></span>

<span data-ttu-id="1ce46-112">Класс **\_ \_ user \_ Config01 \_ ApplicationManagement02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1ce46-112">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="1ce46-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1ce46-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ce46-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="1ce46-114">Properties</span></span>

<span data-ttu-id="1ce46-115">Класс **\_ \_ user \_ Config01 \_ ApplicationManagement02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1ce46-115">The **MDM\_Policy\_User\_Config01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1ce46-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1ce46-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce46-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1ce46-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ce46-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1ce46-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ce46-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ce46-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ce46-120">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="1ce46-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="1ce46-121">Для этого класса строка имеет значение "Аппликатионманажемент".</span><span class="sxs-lookup"><span data-stu-id="1ce46-121">For this class, the string is "ApplicationManagement"</span></span>

</dd> <dt>

<span data-ttu-id="1ce46-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1ce46-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce46-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="1ce46-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1ce46-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1ce46-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1ce46-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1ce46-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1ce46-126">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="1ce46-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="1ce46-127">Для этого класса строка имеет значение "./Усер/вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="1ce46-127">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="1ce46-128">рекуиреприватестореонли</span><span class="sxs-lookup"><span data-stu-id="1ce46-128">RequirePrivateStoreOnly</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1ce46-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="1ce46-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1ce46-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1ce46-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ce46-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1ce46-131">Requirements</span></span>



| <span data-ttu-id="1ce46-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1ce46-132">Requirement</span></span> | <span data-ttu-id="1ce46-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1ce46-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce46-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1ce46-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce46-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1ce46-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ce46-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1ce46-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce46-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1ce46-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1ce46-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1ce46-138">Namespace</span></span><br/>                | <span data-ttu-id="1ce46-139">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="1ce46-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1ce46-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1ce46-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ce46-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ce46-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ce46-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1ce46-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ce46-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ce46-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce46-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ce46-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce46-145">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="1ce46-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

