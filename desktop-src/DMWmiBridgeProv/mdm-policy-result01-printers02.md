---
title: Класс MDM_Policy_Result01_Printers02
description: '\_Класс политики MDM \_ Result01 \_ Printers02 представляет политики принтера.'
ms.assetid: f64fbb03-c62c-4f8e-97ad-e08e068a31d1
keywords:
- Класс MDM_Policy_Result01_Printers02
- MDM_Policy_Result01_Printers02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Printers02
- MDM_Policy_Result01_Printers02.InstanceID
- MDM_Policy_Result01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042820825441928aa04d499a06df3a05ced3889d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415001"
---
# <a name="mdm_policy_result01_printers02-class"></a><span data-ttu-id="f0c18-105">\_Класс политики MDM \_ Result01 \_ Printers02</span><span class="sxs-lookup"><span data-stu-id="f0c18-105">MDM\_Policy\_Result01\_Printers02 class</span></span>

<span data-ttu-id="f0c18-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f0c18-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f0c18-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f0c18-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f0c18-108">\_Класс политики MDM \_ Result01 \_ Printers02 представляет политики принтера.</span><span class="sxs-lookup"><span data-stu-id="f0c18-108">The MDM\_Policy\_Result01\_Printers02 class represents the printer policies.</span></span>

<span data-ttu-id="f0c18-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f0c18-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c18-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0c18-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions;
  string PublishPrinters;
};
```

## <a name="members"></a><span data-ttu-id="f0c18-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f0c18-111">Members</span></span>

<span data-ttu-id="f0c18-112">Класс **\_ политики MDM \_ Result01 \_ Printers02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f0c18-112">The **MDM\_Policy\_Result01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="f0c18-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f0c18-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0c18-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f0c18-114">Properties</span></span>

<span data-ttu-id="f0c18-115">Класс **\_ политики MDM \_ Result01 \_ Printers02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f0c18-115">The **MDM\_Policy\_Result01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f0c18-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0c18-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c18-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0c18-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c18-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0c18-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0c18-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0c18-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0c18-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f0c18-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c18-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0c18-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c18-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f0c18-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0c18-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0c18-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0c18-124">поинтандпринтрестриктионс</span><span class="sxs-lookup"><span data-stu-id="f0c18-124">PointAndPrintRestrictions</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c18-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0c18-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c18-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0c18-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0c18-127">публишпринтерс</span><span class="sxs-lookup"><span data-stu-id="f0c18-127">PublishPrinters</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-publishprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0c18-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f0c18-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0c18-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f0c18-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0c18-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f0c18-130">Requirements</span></span>



| <span data-ttu-id="f0c18-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f0c18-131">Requirement</span></span> | <span data-ttu-id="f0c18-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f0c18-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c18-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0c18-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c18-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f0c18-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0c18-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0c18-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c18-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0c18-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f0c18-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0c18-137">Namespace</span></span><br/>                | <span data-ttu-id="f0c18-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f0c18-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f0c18-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f0c18-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0c18-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0c18-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0c18-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f0c18-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0c18-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c18-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

