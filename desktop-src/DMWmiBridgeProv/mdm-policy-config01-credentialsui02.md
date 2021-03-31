---
title: Класс MDM_Policy_Config01_CredentialsUI02
description: '\_Класс политики MDM \_ Config01 \_ CredentialsUI02 настраивает доступные политики поставщика учетных данных.'
ms.assetid: 508b8dc8-cc89-4260-9346-30deeac606fd
keywords:
- Класс MDM_Policy_Config01_CredentialsUI02
- MDM_Policy_Config01_CredentialsUI02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialsUI02
- MDM_Policy_Config01_CredentialsUI02.InstanceID
- MDM_Policy_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e0fcb9b736adfabbf2b3de12d576ef76652e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071429"
---
# <a name="mdm_policy_config01_credentialsui02-class"></a><span data-ttu-id="ef9c5-105">\_Класс политики MDM \_ Config01 \_ CredentialsUI02</span><span class="sxs-lookup"><span data-stu-id="ef9c5-105">MDM\_Policy\_Config01\_CredentialsUI02 class</span></span>

<span data-ttu-id="ef9c5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ef9c5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ef9c5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ef9c5-108">\_Класс политики MDM \_ Config01 \_ CredentialsUI02 настраивает доступные политики поставщика учетных данных.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-108">The MDM\_Policy\_Config01\_CredentialsUI02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="ef9c5-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef9c5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef9c5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="ef9c5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="ef9c5-111">Members</span></span>

<span data-ttu-id="ef9c5-112">Класс **\_ политики MDM \_ Config01 \_ CredentialsUI02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ef9c5-112">The **MDM\_Policy\_Config01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="ef9c5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef9c5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef9c5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef9c5-114">Properties</span></span>

<span data-ttu-id="ef9c5-115">Класс **\_ политики MDM \_ Config01 \_ CredentialsUI02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ef9c5-115">The **MDM\_Policy\_Config01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ef9c5-116">дисаблепассвордревеал</span><span class="sxs-lookup"><span data-stu-id="ef9c5-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef9c5-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef9c5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef9c5-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ef9c5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ef9c5-119">енумератеадминистраторс</span><span class="sxs-lookup"><span data-stu-id="ef9c5-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef9c5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef9c5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef9c5-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ef9c5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ef9c5-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ef9c5-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef9c5-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef9c5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef9c5-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef9c5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef9c5-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ef9c5-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ef9c5-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ef9c5-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef9c5-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef9c5-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ef9c5-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef9c5-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ef9c5-129">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ef9c5-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef9c5-130">Требования</span><span class="sxs-lookup"><span data-stu-id="ef9c5-130">Requirements</span></span>



| <span data-ttu-id="ef9c5-131">Требование</span><span class="sxs-lookup"><span data-stu-id="ef9c5-131">Requirement</span></span> | <span data-ttu-id="ef9c5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ef9c5-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef9c5-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef9c5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ef9c5-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ef9c5-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef9c5-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef9c5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ef9c5-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ef9c5-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ef9c5-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef9c5-137">Namespace</span></span><br/>                | <span data-ttu-id="ef9c5-138">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ef9c5-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ef9c5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ef9c5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef9c5-140"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef9c5-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ef9c5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ef9c5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef9c5-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef9c5-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

