---
title: Класс MDM_Policy_Config01_DataUsage02
description: '\_Класс политики MDM \_ Config01 \_ DataUsage02 настраивает доступные политики использования данных.'
ms.assetid: c5e77d82-df5e-4eed-90f5-50f2ed62e975
keywords:
- Класс MDM_Policy_Config01_DataUsage02
- MDM_Policy_Config01_DataUsage02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DataUsage02
- MDM_Policy_Config01_DataUsage02.InstanceID
- MDM_Policy_Config01_DataUsage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b878ec3bf38444dd82c08fe880e84028067bbd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135546"
---
# <a name="mdm_policy_config01_datausage02-class"></a><span data-ttu-id="5214e-105">\_Класс политики MDM \_ Config01 \_ DataUsage02</span><span class="sxs-lookup"><span data-stu-id="5214e-105">MDM\_Policy\_Config01\_DataUsage02 class</span></span>

<span data-ttu-id="5214e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="5214e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5214e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="5214e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5214e-108">\_Класс политики MDM \_ Config01 \_ DataUsage02 настраивает доступные политики использования данных.</span><span class="sxs-lookup"><span data-stu-id="5214e-108">The MDM\_Policy\_Config01\_DataUsage02 class configures the available data usage policies.</span></span>

<span data-ttu-id="5214e-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5214e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5214e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5214e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DataUsage02
{
  string InstanceID;
  string ParentID;
  string SetCost3G;
  string SetCost4G;
};
```

## <a name="members"></a><span data-ttu-id="5214e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="5214e-111">Members</span></span>

<span data-ttu-id="5214e-112">Класс **\_ политики MDM \_ Config01 \_ DataUsage02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5214e-112">The **MDM\_Policy\_Config01\_DataUsage02** class has these types of members:</span></span>

-   [<span data-ttu-id="5214e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5214e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5214e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="5214e-114">Properties</span></span>

<span data-ttu-id="5214e-115">Класс **\_ политики MDM \_ Config01 \_ DataUsage02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5214e-115">The **MDM\_Policy\_Config01\_DataUsage02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5214e-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5214e-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5214e-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5214e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5214e-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5214e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5214e-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5214e-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5214e-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5214e-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5214e-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5214e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5214e-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5214e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5214e-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5214e-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5214e-124">SetCost3G</span><span class="sxs-lookup"><span data-stu-id="5214e-124">SetCost3G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost3g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5214e-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5214e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5214e-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5214e-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5214e-127">SetCost4G</span><span class="sxs-lookup"><span data-stu-id="5214e-127">SetCost4G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost4g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5214e-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5214e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5214e-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5214e-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5214e-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5214e-130">Requirements</span></span>



| <span data-ttu-id="5214e-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5214e-131">Requirement</span></span> | <span data-ttu-id="5214e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5214e-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5214e-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5214e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5214e-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5214e-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5214e-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5214e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5214e-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5214e-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5214e-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5214e-137">Namespace</span></span><br/>                | <span data-ttu-id="5214e-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="5214e-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5214e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5214e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5214e-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5214e-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5214e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5214e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5214e-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5214e-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

