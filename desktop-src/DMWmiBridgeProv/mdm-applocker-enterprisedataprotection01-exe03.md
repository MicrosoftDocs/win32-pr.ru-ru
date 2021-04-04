---
title: Класс MDM_AppLocker_EnterpriseDataProtection01_EXE03
description: Класс MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03 фиксирует список исполняемых приложений, которым разрешено работать с корпоративными данными.
ms.assetid: 43f253d4-3f9d-4651-91b4-b7460706e8b4
keywords:
- Класс MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03 класс, описание
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_EXE03
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_EXE03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6cbaba46034c26524ca7e12aaa93b588708f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137546"
---
# <a name="mdm_applocker_enterprisedataprotection01_exe03-class"></a><span data-ttu-id="bcc5a-105">\_Класс MDM AppLocker \_ EnterpriseDataProtection01 \_ EXE03</span><span class="sxs-lookup"><span data-stu-id="bcc5a-105">MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03 class</span></span>

<span data-ttu-id="bcc5a-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="bcc5a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bcc5a-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="bcc5a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bcc5a-108">Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** фиксирует список исполняемых приложений, которым разрешено работать с корпоративными данными.</span><span class="sxs-lookup"><span data-stu-id="bcc5a-108">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class captures the list of executable applications that are allowed to handle enterprise data.</span></span> <span data-ttu-id="bcc5a-109">Следует использовать в сочетании с параметрами в./вендор/мсфт/Полици/конфигсаурце/датапротектион.</span><span class="sxs-lookup"><span data-stu-id="bcc5a-109">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="bcc5a-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="bcc5a-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcc5a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcc5a-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_EXE03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="bcc5a-112">Члены</span><span class="sxs-lookup"><span data-stu-id="bcc5a-112">Members</span></span>

<span data-ttu-id="bcc5a-113">Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bcc5a-113">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these types of members:</span></span>

-   [<span data-ttu-id="bcc5a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="bcc5a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bcc5a-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="bcc5a-115">Properties</span></span>

<span data-ttu-id="bcc5a-116">Класс **MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ EXE03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bcc5a-116">The **MDM\_AppLocker\_EnterpriseDataProtection01\_EXE03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bcc5a-117">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bcc5a-117">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcc5a-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcc5a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcc5a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcc5a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcc5a-120">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bcc5a-120">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bcc5a-121">Определяет ограничения для запуска исполняемых приложений.</span><span class="sxs-lookup"><span data-stu-id="bcc5a-121">Defines restrictions for launching executable applications.</span></span>

</dd> <dt>

<span data-ttu-id="bcc5a-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bcc5a-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcc5a-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcc5a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcc5a-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bcc5a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bcc5a-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bcc5a-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bcc5a-126">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="bcc5a-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="bcc5a-127">Для этого класса строка имеет значение "./вендор/мсфт/апплоккер/ентерприседатапротектион/*GROUPING*"</span><span class="sxs-lookup"><span data-stu-id="bcc5a-127">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="bcc5a-128">**Политика**</span><span class="sxs-lookup"><span data-stu-id="bcc5a-128">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bcc5a-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bcc5a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bcc5a-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bcc5a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcc5a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="bcc5a-131">Requirements</span></span>



| <span data-ttu-id="bcc5a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bcc5a-132">Requirement</span></span> | <span data-ttu-id="bcc5a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bcc5a-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc5a-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bcc5a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc5a-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bcc5a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcc5a-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bcc5a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc5a-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bcc5a-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bcc5a-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bcc5a-138">Namespace</span></span><br/>                | <span data-ttu-id="bcc5a-139">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="bcc5a-139">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="bcc5a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bcc5a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcc5a-141"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bcc5a-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcc5a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bcc5a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcc5a-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcc5a-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc5a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcc5a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc5a-145">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="bcc5a-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

