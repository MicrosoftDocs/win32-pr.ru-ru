---
title: Класс MDM_Policy_User_Config01_EnterpriseCloudPrint02
description: '\_Класс политики MDM \_ user \_ Config01 \_ EnterpriseCloudPrint02 представляет доступные политики печати в облаке.'
ms.assetid: cc885184-1197-48c4-ba48-a2944a416534
keywords:
- Класс MDM_Policy_User_Config01_EnterpriseCloudPrint02
- MDM_Policy_User_Config01_EnterpriseCloudPrint02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_EnterpriseCloudPrint02
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Config01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2b9d42afbab4d3f17d91b6db630ef67faf6ccc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891985"
---
# <a name="mdm_policy_user_config01_enterprisecloudprint02-class"></a><span data-ttu-id="e8570-105">\_Класс политики MDM \_ user \_ Config01 \_ EnterpriseCloudPrint02</span><span class="sxs-lookup"><span data-stu-id="e8570-105">MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="e8570-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e8570-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e8570-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e8570-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e8570-108">\_Класс политики MDM \_ user \_ Config01 \_ EnterpriseCloudPrint02 представляет доступные политики печати в облаке.</span><span class="sxs-lookup"><span data-stu-id="e8570-108">The MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="e8570-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e8570-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8570-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8570-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_EnterpriseCloudPrint02
{
  string InstanceID;
  string ParentID;
  string CloudPrinterDiscoveryEndPoint;
  string CloudPrintOAuthAuthority;
  string CloudPrintOAuthClientId;
  string CloudPrintResourceId;
  sint32 DiscoveryMaxPrinterLimit;
  string MopriaDiscoveryResourceId;
};
```

## <a name="members"></a><span data-ttu-id="e8570-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e8570-111">Members</span></span>

<span data-ttu-id="e8570-112">Класс **\_ \_ user \_ Config01 \_ EnterpriseCloudPrint02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e8570-112">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="e8570-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8570-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8570-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8570-114">Properties</span></span>

<span data-ttu-id="e8570-115">Класс **\_ \_ user \_ Config01 \_ EnterpriseCloudPrint02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="e8570-115">The **MDM\_Policy\_User\_Config01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e8570-116">клаудпринтердисковерендпоинт</span><span class="sxs-lookup"><span data-stu-id="e8570-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8570-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8570-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8570-119">клаудпринтоаусаусорити</span><span class="sxs-lookup"><span data-stu-id="e8570-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8570-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8570-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8570-122">клаудпринтоаусклиентид</span><span class="sxs-lookup"><span data-stu-id="e8570-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8570-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8570-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8570-125">клаудпринтресаурцеид</span><span class="sxs-lookup"><span data-stu-id="e8570-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8570-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8570-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8570-128">дисковеримакспринтерлимит</span><span class="sxs-lookup"><span data-stu-id="e8570-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e8570-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8570-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8570-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e8570-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8570-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8570-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8570-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8570-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e8570-135">моприадисковериресаурцеид</span><span class="sxs-lookup"><span data-stu-id="e8570-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8570-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e8570-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e8570-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e8570-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8570-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e8570-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8570-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8570-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8570-141">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e8570-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8570-142">Требования</span><span class="sxs-lookup"><span data-stu-id="e8570-142">Requirements</span></span>



| <span data-ttu-id="e8570-143">Требование</span><span class="sxs-lookup"><span data-stu-id="e8570-143">Requirement</span></span> | <span data-ttu-id="e8570-144">Значение</span><span class="sxs-lookup"><span data-stu-id="e8570-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8570-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8570-145">Minimum supported client</span></span><br/> | <span data-ttu-id="e8570-146">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e8570-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e8570-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8570-147">Minimum supported server</span></span><br/> | <span data-ttu-id="e8570-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e8570-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e8570-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8570-149">Namespace</span></span><br/>                | <span data-ttu-id="e8570-150">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e8570-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e8570-151">MOF</span><span class="sxs-lookup"><span data-stu-id="e8570-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8570-152"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8570-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8570-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e8570-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8570-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8570-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

