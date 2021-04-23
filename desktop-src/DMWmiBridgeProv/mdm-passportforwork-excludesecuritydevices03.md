---
title: Класс MDM_PassportForWork_ExcludeSecurityDevices03
description: Класс MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03 определяет доверенные платформенные модули, разрешенные для использования с Windows Hello для бизнеса.
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- Класс MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03 класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e5cc0374a3c313a118e5ee72791380225cc760
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071443"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a><span data-ttu-id="32474-105">\_Класс MDM пасспортфорворк \_ ExcludeSecurityDevices03</span><span class="sxs-lookup"><span data-stu-id="32474-105">MDM\_PassportForWork\_ExcludeSecurityDevices03 class</span></span>

<span data-ttu-id="32474-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="32474-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32474-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="32474-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32474-108">Класс MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03 определяет доверенные платформенные модули, разрешенные для использования с Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="32474-108">The MDM\_PassportForWork\_ExcludeSecurityDevices03 class defines the Trusted Platform Modules allowed to use with Windows Hello for Business.</span></span>

<span data-ttu-id="32474-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="32474-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32474-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32474-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a><span data-ttu-id="32474-111">Члены</span><span class="sxs-lookup"><span data-stu-id="32474-111">Members</span></span>

<span data-ttu-id="32474-112">Класс **MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="32474-112">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these types of members:</span></span>

-   [<span data-ttu-id="32474-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="32474-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32474-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="32474-114">Properties</span></span>

<span data-ttu-id="32474-115">Класс **MDM \_ пасспортфорворк \_ ExcludeSecurityDevices03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="32474-115">The **MDM\_PassportForWork\_ExcludeSecurityDevices03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32474-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="32474-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32474-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32474-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32474-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32474-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32474-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32474-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32474-120">Корневой узел.</span><span class="sxs-lookup"><span data-stu-id="32474-120">Root node.</span></span>

</dd> <dt>

<span data-ttu-id="32474-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="32474-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32474-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="32474-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32474-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32474-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32474-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32474-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32474-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="32474-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="32474-126">Дополнительные сведения см. в статье [ПАССПОРТФОРВОРК CSP](/windows/client-management/mdm/passportforwork-csp).</span><span class="sxs-lookup"><span data-stu-id="32474-126">For more information, see [PassportForWork CSP](/windows/client-management/mdm/passportforwork-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="32474-127">TPM12</span><span class="sxs-lookup"><span data-stu-id="32474-127">TPM12</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32474-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="32474-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="32474-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="32474-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32474-130">Требования</span><span class="sxs-lookup"><span data-stu-id="32474-130">Requirements</span></span>



| <span data-ttu-id="32474-131">Требование</span><span class="sxs-lookup"><span data-stu-id="32474-131">Requirement</span></span> | <span data-ttu-id="32474-132">Значение</span><span class="sxs-lookup"><span data-stu-id="32474-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32474-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32474-133">Minimum supported client</span></span><br/> | <span data-ttu-id="32474-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="32474-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32474-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32474-135">Minimum supported server</span></span><br/> | <span data-ttu-id="32474-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="32474-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="32474-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="32474-137">Namespace</span></span><br/>                | <span data-ttu-id="32474-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="32474-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="32474-139">MOF</span><span class="sxs-lookup"><span data-stu-id="32474-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32474-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32474-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="32474-141">DLL</span><span class="sxs-lookup"><span data-stu-id="32474-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32474-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32474-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

