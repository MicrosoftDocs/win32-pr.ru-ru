---
title: Класс MDM_Policy_Result01_Licensing02
description: '\_Класс политики MDM \_ Result01 \_ Licensing02 представляет доступные политики лицензирования.'
ms.assetid: 0f3faa78-c9ed-4166-a860-b5096b33772a
keywords:
- Класс MDM_Policy_Result01_Licensing02
- MDM_Policy_Result01_Licensing02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Licensing02
- MDM_Policy_Result01_Licensing02.InstanceID
- MDM_Policy_Result01_Licensing02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa40b1aa0ff64ddd360a304f5366f961fc2c993c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071509"
---
# <a name="mdm_policy_result01_licensing02-class"></a><span data-ttu-id="f5f99-105">\_Класс политики MDM \_ Result01 \_ Licensing02</span><span class="sxs-lookup"><span data-stu-id="f5f99-105">MDM\_Policy\_Result01\_Licensing02 class</span></span>

<span data-ttu-id="f5f99-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="f5f99-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f5f99-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="f5f99-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f5f99-108">Класс **\_ политики MDM \_ Result01 \_ Licensing02** представляет доступные политики лицензирования.</span><span class="sxs-lookup"><span data-stu-id="f5f99-108">The **MDM\_Policy\_Result01\_Licensing02** class represents the licensing policies available.</span></span>

<span data-ttu-id="f5f99-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f5f99-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5f99-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5f99-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Licensing02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsEntitlementReactivation;
  sint32 DisallowKMSClientOnlineAVSValidation;
};
```

## <a name="members"></a><span data-ttu-id="f5f99-111">Члены</span><span class="sxs-lookup"><span data-stu-id="f5f99-111">Members</span></span>

<span data-ttu-id="f5f99-112">Класс **\_ политики MDM \_ Result01 \_ Licensing02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f5f99-112">The **MDM\_Policy\_Result01\_Licensing02** class has these types of members:</span></span>

-   [<span data-ttu-id="f5f99-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5f99-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5f99-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5f99-114">Properties</span></span>

<span data-ttu-id="f5f99-115">Класс **\_ политики MDM \_ Result01 \_ Licensing02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f5f99-115">The **MDM\_Policy\_Result01\_Licensing02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f5f99-116">AllowWindowsEntitlementReactivation</span><span class="sxs-lookup"><span data-stu-id="f5f99-116">AllowWindowsEntitlementReactivation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-allowwindowsentitlementreactivation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5f99-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f5f99-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5f99-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f5f99-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f5f99-119">DisallowKMSClientOnlineAVSValidation</span><span class="sxs-lookup"><span data-stu-id="f5f99-119">DisallowKMSClientOnlineAVSValidation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-disallowkmsclientonlineavsvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5f99-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f5f99-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5f99-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f5f99-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f5f99-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f5f99-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5f99-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5f99-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5f99-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5f99-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5f99-125">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5f99-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5f99-126">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="f5f99-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="f5f99-127">Для этого класса строка имеет значение "Licensing".</span><span class="sxs-lookup"><span data-stu-id="f5f99-127">For this class, the string is "Licensing".</span></span>

</dd> <dt>

<span data-ttu-id="f5f99-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f5f99-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5f99-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5f99-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5f99-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5f99-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5f99-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5f99-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5f99-132">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="f5f99-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="f5f99-133">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="f5f99-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5f99-134">Требования</span><span class="sxs-lookup"><span data-stu-id="f5f99-134">Requirements</span></span>



| <span data-ttu-id="f5f99-135">Требование</span><span class="sxs-lookup"><span data-stu-id="f5f99-135">Requirement</span></span> | <span data-ttu-id="f5f99-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f5f99-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f99-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5f99-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f5f99-138">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f5f99-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f5f99-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5f99-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f5f99-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5f99-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="f5f99-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5f99-141">Namespace</span></span><br/>                | <span data-ttu-id="f5f99-142">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="f5f99-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="f5f99-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f5f99-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5f99-144"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5f99-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="f5f99-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f5f99-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5f99-146"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5f99-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

