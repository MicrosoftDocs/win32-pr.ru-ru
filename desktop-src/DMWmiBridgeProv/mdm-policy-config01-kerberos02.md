---
title: Класс MDM_Policy_Config01_Kerberos02
description: '\_Класс политики MDM \_ Config01 \_ Kerberos02 настраивает политики Kerberos.'
ms.assetid: d34ccc8a-0c0c-4b7a-88c2-35360ebd0b8e
keywords:
- Класс MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02.InstanceID
- MDM_Policy_Config01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c173c892985487ed1ac061ea720e3485ecb355ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891906"
---
# <a name="mdm_policy_config01_kerberos02-class"></a><span data-ttu-id="bb139-105">\_Класс политики MDM \_ Config01 \_ Kerberos02</span><span class="sxs-lookup"><span data-stu-id="bb139-105">MDM\_Policy\_Config01\_Kerberos02 class</span></span>

<span data-ttu-id="bb139-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="bb139-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bb139-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="bb139-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bb139-108">\_Класс политики MDM \_ Config01 \_ Kerberos02 настраивает политики Kerberos.</span><span class="sxs-lookup"><span data-stu-id="bb139-108">The MDM\_Policy\_Config01\_Kerberos02 class configures the Kerberos policies.</span></span>

<span data-ttu-id="bb139-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="bb139-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb139-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb139-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a><span data-ttu-id="bb139-111">Члены</span><span class="sxs-lookup"><span data-stu-id="bb139-111">Members</span></span>

<span data-ttu-id="bb139-112">Класс **\_ политики MDM \_ Config01 \_ Kerberos02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bb139-112">The **MDM\_Policy\_Config01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="bb139-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb139-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb139-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb139-114">Properties</span></span>

<span data-ttu-id="bb139-115">Класс **\_ политики MDM \_ Config01 \_ Kerberos02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bb139-115">The **MDM\_Policy\_Config01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bb139-116">алловфорестсеарчордер</span><span class="sxs-lookup"><span data-stu-id="bb139-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb139-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb139-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb139-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb139-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bb139-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bb139-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb139-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb139-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb139-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb139-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb139-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb139-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb139-123">керберосклиентсуппортсклаимскомпаундармор</span><span class="sxs-lookup"><span data-stu-id="bb139-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb139-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb139-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb139-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb139-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bb139-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bb139-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb139-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb139-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb139-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb139-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb139-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bb139-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb139-130">рекуирекерберосарморинг</span><span class="sxs-lookup"><span data-stu-id="bb139-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb139-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb139-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb139-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb139-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb139-133">рекуирестрикткдквалидатион</span><span class="sxs-lookup"><span data-stu-id="bb139-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb139-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb139-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb139-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb139-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bb139-136">сетмаксимумконтексттокенсизе</span><span class="sxs-lookup"><span data-stu-id="bb139-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb139-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb139-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb139-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb139-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb139-139">Требования</span><span class="sxs-lookup"><span data-stu-id="bb139-139">Requirements</span></span>



| <span data-ttu-id="bb139-140">Требование</span><span class="sxs-lookup"><span data-stu-id="bb139-140">Requirement</span></span> | <span data-ttu-id="bb139-141">Значение</span><span class="sxs-lookup"><span data-stu-id="bb139-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb139-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb139-142">Minimum supported client</span></span><br/> | <span data-ttu-id="bb139-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bb139-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb139-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb139-144">Minimum supported server</span></span><br/> | <span data-ttu-id="bb139-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bb139-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bb139-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb139-146">Namespace</span></span><br/>                | <span data-ttu-id="bb139-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="bb139-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bb139-148">MOF</span><span class="sxs-lookup"><span data-stu-id="bb139-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb139-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb139-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb139-150">DLL</span><span class="sxs-lookup"><span data-stu-id="bb139-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb139-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb139-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

