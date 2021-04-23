---
title: Класс MDM_PassportForWork_Remote03
description: Класс MDM \_ пасспортфорворк \_ Remote03 определяет параметры удаленной политики Windows Hello для бизнеса.
ms.assetid: 221701be-944f-42cd-847e-553d41281749
keywords:
- Класс MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03 класс, описание
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Remote03
- MDM_PassportForWork_Remote03.InstanceID
- MDM_PassportForWork_Remote03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae111389ad0f7c46b1f0b217bffc016e451ca9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071440"
---
# <a name="mdm_passportforwork_remote03-class"></a><span data-ttu-id="d4d9e-105">\_Класс MDM пасспортфорворк \_ Remote03</span><span class="sxs-lookup"><span data-stu-id="d4d9e-105">MDM\_PassportForWork\_Remote03 class</span></span>

<span data-ttu-id="d4d9e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="d4d9e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d4d9e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="d4d9e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d4d9e-108">Класс **MDM \_ пасспортфорворк \_ Remote03** определяет параметры удаленной политики Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="d4d9e-108">The **MDM\_PassportForWork\_Remote03** class defines the Windows Hello for Business remote policy settings.</span></span>

<span data-ttu-id="d4d9e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d4d9e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d9e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d4d9e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Remote03
{
  string  InstanceID;
  string  ParentID;
  boolean UseRemotePassport;
};
```

## <a name="members"></a><span data-ttu-id="d4d9e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="d4d9e-111">Members</span></span>

<span data-ttu-id="d4d9e-112">Класс **MDM \_ пасспортфорворк \_ Remote03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d4d9e-112">The **MDM\_PassportForWork\_Remote03** class has these types of members:</span></span>

-   [<span data-ttu-id="d4d9e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4d9e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4d9e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="d4d9e-114">Properties</span></span>

<span data-ttu-id="d4d9e-115">Класс **MDM \_ пасспортфорворк \_ Remote03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d4d9e-115">The **MDM\_PassportForWork\_Remote03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4d9e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d4d9e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4d9e-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4d9e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4d9e-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4d9e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4d9e-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d4d9e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d4d9e-120">Внутренний узел для определения удаленных политик Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="d4d9e-120">Interior node for defining remote Windows Hello for Business policies.</span></span> <span data-ttu-id="d4d9e-121">Этот узел был добавлен в Windows 10 версии 1511.</span><span class="sxs-lookup"><span data-stu-id="d4d9e-121">This node was added in Windows 10, version 1511.</span></span>

</dd> <dt>

<span data-ttu-id="d4d9e-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d4d9e-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4d9e-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d4d9e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4d9e-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d4d9e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4d9e-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d4d9e-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d4d9e-126">Узел для определения параметров политики Windows Hello для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="d4d9e-126">Node for defining the Windows Hello for Business policy settings.</span></span>

</dd> <dt>

[<span data-ttu-id="d4d9e-127">UseRemotePassport</span><span class="sxs-lookup"><span data-stu-id="d4d9e-127">UseRemotePassport</span></span>](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4d9e-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d4d9e-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d4d9e-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d4d9e-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4d9e-130">Требования</span><span class="sxs-lookup"><span data-stu-id="d4d9e-130">Requirements</span></span>



| <span data-ttu-id="d4d9e-131">Требование</span><span class="sxs-lookup"><span data-stu-id="d4d9e-131">Requirement</span></span> | <span data-ttu-id="d4d9e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="d4d9e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d9e-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d4d9e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d9e-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d4d9e-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4d9e-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d4d9e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d9e-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d4d9e-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d4d9e-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d4d9e-137">Namespace</span></span><br/>                | <span data-ttu-id="d4d9e-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="d4d9e-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d4d9e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d4d9e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4d9e-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4d9e-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4d9e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d4d9e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4d9e-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4d9e-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4d9e-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4d9e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4d9e-144">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="d4d9e-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

