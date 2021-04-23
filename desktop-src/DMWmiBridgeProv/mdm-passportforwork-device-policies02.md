---
title: Класс MDM_PassportForWork_Device_Policies02
description: Класс MDM \_ пасспортфорворк \_ Device \_ Policies02 определяет параметры политики Windows Hello для бизнеса.
ms.assetid: 7581ea7e-0360-4695-a4ad-566df24a8841
keywords:
- Класс MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02 класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Device_Policies02
- MDM_PassportForWork_Device_Policies02.InstanceID
- MDM_PassportForWork_Device_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66d642fb796d3b7af009197580f1eda21ab0bdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988464"
---
# <a name="mdm_passportforwork_device_policies02-class"></a><span data-ttu-id="b7334-105">\_ \_ Класс POLICIES02 устройства MDM пасспортфорворк \_</span><span class="sxs-lookup"><span data-stu-id="b7334-105">MDM\_PassportForWork\_Device\_Policies02 class</span></span>

<span data-ttu-id="b7334-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="b7334-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b7334-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="b7334-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b7334-108">Класс **MDM \_ пасспортфорворк \_ Device \_ Policies02** определяет параметры политики Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="b7334-108">The **MDM\_PassportForWork\_Device\_Policies02** class defines the Windows Hello for Business policy settings.</span></span>

<span data-ttu-id="b7334-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b7334-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7334-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7334-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Device_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UseCertificateForOnPremAuth;
};
```

## <a name="members"></a><span data-ttu-id="b7334-111">Члены</span><span class="sxs-lookup"><span data-stu-id="b7334-111">Members</span></span>

<span data-ttu-id="b7334-112">Класс **\_ \_ \_ Policies02 устройства MDM пасспортфорворк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b7334-112">The **MDM\_PassportForWork\_Device\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="b7334-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7334-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7334-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7334-114">Properties</span></span>

<span data-ttu-id="b7334-115">Класс **\_ \_ \_ Policies02 устройства MDM пасспортфорворк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b7334-115">The **MDM\_PassportForWork\_Device\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7334-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b7334-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7334-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7334-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7334-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7334-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7334-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7334-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7334-120">Узел для параметров политики Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="b7334-120">Node for the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

<span data-ttu-id="b7334-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b7334-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7334-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7334-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7334-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7334-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7334-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7334-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7334-125">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="b7334-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="b7334-126">Для этого класса строка имеет значение "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span><span class="sxs-lookup"><span data-stu-id="b7334-126">For this class, the string is "./Device/Vendor/MSFT/PassPortForWork/*TenantID*/"</span></span>

</dd> <dt>

[<span data-ttu-id="b7334-127">усецертификатефоронпремаус</span><span class="sxs-lookup"><span data-stu-id="b7334-127">UseCertificateForOnPremAuth</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7334-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b7334-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7334-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b7334-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7334-130">Требования</span><span class="sxs-lookup"><span data-stu-id="b7334-130">Requirements</span></span>



| <span data-ttu-id="b7334-131">Требование</span><span class="sxs-lookup"><span data-stu-id="b7334-131">Requirement</span></span> | <span data-ttu-id="b7334-132">Значение</span><span class="sxs-lookup"><span data-stu-id="b7334-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7334-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7334-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b7334-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b7334-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7334-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7334-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b7334-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b7334-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b7334-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b7334-137">Namespace</span></span><br/>                | <span data-ttu-id="b7334-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="b7334-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b7334-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b7334-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7334-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7334-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7334-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b7334-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7334-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7334-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

