---
title: Класс MDM_Policy_Result01_Kerberos02
description: '\_Класс политики MDM \_ Result01 \_ Kerberos02 представляет политики Kerberos.'
ms.assetid: a628272d-723f-491a-a6a1-70514e5096ef
keywords:
- Класс MDM_Policy_Result01_Kerberos02
- MDM_Policy_Result01_Kerberos02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Kerberos02
- MDM_Policy_Result01_Kerberos02.InstanceID
- MDM_Policy_Result01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713d7747fe45fa72cb7dcf44a02aa57526161c17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490170"
---
# <a name="mdm_policy_result01_kerberos02-class"></a><span data-ttu-id="25982-105">\_Класс политики MDM \_ Result01 \_ Kerberos02</span><span class="sxs-lookup"><span data-stu-id="25982-105">MDM\_Policy\_Result01\_Kerberos02 class</span></span>

<span data-ttu-id="25982-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="25982-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="25982-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="25982-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="25982-108">\_Класс политики MDM \_ Result01 \_ Kerberos02 представляет политики Kerberos.</span><span class="sxs-lookup"><span data-stu-id="25982-108">The MDM\_Policy\_Result01\_Kerberos02 class represents the Kerberos policies.</span></span>

<span data-ttu-id="25982-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="25982-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="25982-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25982-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Kerberos02
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

## <a name="members"></a><span data-ttu-id="25982-111">Члены</span><span class="sxs-lookup"><span data-stu-id="25982-111">Members</span></span>

<span data-ttu-id="25982-112">Класс **\_ политики MDM \_ Result01 \_ Kerberos02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="25982-112">The **MDM\_Policy\_Result01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="25982-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="25982-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25982-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="25982-114">Properties</span></span>

<span data-ttu-id="25982-115">Класс **\_ политики MDM \_ Result01 \_ Kerberos02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="25982-115">The **MDM\_Policy\_Result01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="25982-116">алловфорестсеарчордер</span><span class="sxs-lookup"><span data-stu-id="25982-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25982-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25982-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25982-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25982-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25982-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="25982-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25982-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25982-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25982-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25982-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25982-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="25982-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="25982-123">керберосклиентсуппортсклаимскомпаундармор</span><span class="sxs-lookup"><span data-stu-id="25982-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25982-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25982-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25982-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25982-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25982-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="25982-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25982-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25982-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25982-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25982-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25982-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="25982-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="25982-130">рекуирекерберосарморинг</span><span class="sxs-lookup"><span data-stu-id="25982-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25982-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25982-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25982-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25982-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="25982-133">рекуирестрикткдквалидатион</span><span class="sxs-lookup"><span data-stu-id="25982-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25982-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25982-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25982-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25982-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="25982-136">сетмаксимумконтексттокенсизе</span><span class="sxs-lookup"><span data-stu-id="25982-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25982-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25982-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25982-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="25982-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25982-139">Требования</span><span class="sxs-lookup"><span data-stu-id="25982-139">Requirements</span></span>



| <span data-ttu-id="25982-140">Требование</span><span class="sxs-lookup"><span data-stu-id="25982-140">Requirement</span></span> | <span data-ttu-id="25982-141">Значение</span><span class="sxs-lookup"><span data-stu-id="25982-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25982-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25982-142">Minimum supported client</span></span><br/> | <span data-ttu-id="25982-143">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="25982-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25982-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25982-144">Minimum supported server</span></span><br/> | <span data-ttu-id="25982-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25982-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="25982-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="25982-146">Namespace</span></span><br/>                | <span data-ttu-id="25982-147">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="25982-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="25982-148">MOF</span><span class="sxs-lookup"><span data-stu-id="25982-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25982-149"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25982-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="25982-150">DLL</span><span class="sxs-lookup"><span data-stu-id="25982-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25982-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25982-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

