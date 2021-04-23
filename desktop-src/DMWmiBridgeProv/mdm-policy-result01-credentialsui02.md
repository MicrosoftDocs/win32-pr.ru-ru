---
title: Класс MDM_Policy_Result01_CredentialsUI02
description: '\_Класс политики MDM \_ Result01 \_ CredentialsUI02 представляет доступные политики учетных данных.'
ms.assetid: d50a4cc5-e87f-44a5-9345-744126615d04
keywords:
- Класс MDM_Policy_Result01_CredentialsUI02
- MDM_Policy_Result01_CredentialsUI02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_CredentialsUI02
- MDM_Policy_Result01_CredentialsUI02.InstanceID
- MDM_Policy_Result01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e444e36f2602fa30ca51601e6cd08e7fa8e30c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489609"
---
# <a name="mdm_policy_result01_credentialsui02-class"></a><span data-ttu-id="4bcab-105">\_Класс политики MDM \_ Result01 \_ CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="4bcab-105">MDM\_Policy\_Result01\_CredentialsUI02 class</span></span>

<span data-ttu-id="4bcab-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="4bcab-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4bcab-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="4bcab-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4bcab-108">\_Класс политики MDM \_ Result01 \_ CredentialsUI02 представляет доступные политики учетных данных.</span><span class="sxs-lookup"><span data-stu-id="4bcab-108">The MDM\_Policy\_Result01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="4bcab-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4bcab-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bcab-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4bcab-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="4bcab-111">Члены</span><span class="sxs-lookup"><span data-stu-id="4bcab-111">Members</span></span>

<span data-ttu-id="4bcab-112">Класс **\_ политики MDM \_ Result01 \_ CredentialsUI02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4bcab-112">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="4bcab-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4bcab-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bcab-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="4bcab-114">Properties</span></span>

<span data-ttu-id="4bcab-115">Класс **\_ политики MDM \_ Result01 \_ CredentialsUI02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4bcab-115">The **MDM\_Policy\_Result01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4bcab-116">дисаблепассвордревеал</span><span class="sxs-lookup"><span data-stu-id="4bcab-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bcab-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4bcab-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bcab-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4bcab-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4bcab-119">енумератеадминистраторс</span><span class="sxs-lookup"><span data-stu-id="4bcab-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bcab-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4bcab-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bcab-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4bcab-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4bcab-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4bcab-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bcab-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4bcab-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bcab-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4bcab-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bcab-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4bcab-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4bcab-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4bcab-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bcab-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4bcab-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bcab-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4bcab-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bcab-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4bcab-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bcab-130">Требования</span><span class="sxs-lookup"><span data-stu-id="4bcab-130">Requirements</span></span>



| <span data-ttu-id="4bcab-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4bcab-131">Requirement</span></span> | <span data-ttu-id="4bcab-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4bcab-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bcab-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bcab-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4bcab-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4bcab-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4bcab-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bcab-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4bcab-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4bcab-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4bcab-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4bcab-137">Namespace</span></span><br/>                | <span data-ttu-id="4bcab-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="4bcab-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="4bcab-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4bcab-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bcab-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bcab-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bcab-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4bcab-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bcab-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bcab-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

