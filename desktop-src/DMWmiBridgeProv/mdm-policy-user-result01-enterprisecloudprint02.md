---
title: Класс MDM_Policy_User_Result01_EnterpriseCloudPrint02
description: '\_Класс политики MDM \_ user \_ Result01 \_ EnterpriseCloudPrint02 представляет доступные политики печати в облаке.'
ms.assetid: cf830cb5-2477-4b21-9d98-9fa9989daa7f
keywords:
- Класс MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_EnterpriseCloudPrint02
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.InstanceID
- MDM_Policy_User_Result01_EnterpriseCloudPrint02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dfa75d102da3a61ff0a9f2094d31e0ba5b4abca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490779"
---
# <a name="mdm_policy_user_result01_enterprisecloudprint02-class"></a><span data-ttu-id="888e5-105">\_Класс политики MDM \_ user \_ Result01 \_ EnterpriseCloudPrint02</span><span class="sxs-lookup"><span data-stu-id="888e5-105">MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class</span></span>

<span data-ttu-id="888e5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="888e5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="888e5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="888e5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="888e5-108">\_Класс политики MDM \_ user \_ Result01 \_ EnterpriseCloudPrint02 представляет доступные политики печати в облаке.</span><span class="sxs-lookup"><span data-stu-id="888e5-108">The MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02 class represents the available cloud print policies.</span></span>

<span data-ttu-id="888e5-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="888e5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="888e5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="888e5-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_EnterpriseCloudPrint02
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

## <a name="members"></a><span data-ttu-id="888e5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="888e5-111">Members</span></span>

<span data-ttu-id="888e5-112">Класс **\_ \_ user \_ Result01 \_ EnterpriseCloudPrint02 политики MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="888e5-112">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these types of members:</span></span>

-   [<span data-ttu-id="888e5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="888e5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="888e5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="888e5-114">Properties</span></span>

<span data-ttu-id="888e5-115">Класс **\_ \_ user \_ Result01 \_ EnterpriseCloudPrint02 политики MDM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="888e5-115">The **MDM\_Policy\_User\_Result01\_EnterpriseCloudPrint02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="888e5-116">клаудпринтердисковерендпоинт</span><span class="sxs-lookup"><span data-stu-id="888e5-116">CloudPrinterDiscoveryEndPoint</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprinterdiscoveryendpoint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="888e5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="888e5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="888e5-119">клаудпринтоаусаусорити</span><span class="sxs-lookup"><span data-stu-id="888e5-119">CloudPrintOAuthAuthority</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthauthority)
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="888e5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="888e5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="888e5-122">клаудпринтоаусклиентид</span><span class="sxs-lookup"><span data-stu-id="888e5-122">CloudPrintOAuthClientId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintoauthclientid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="888e5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="888e5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="888e5-125">клаудпринтресаурцеид</span><span class="sxs-lookup"><span data-stu-id="888e5-125">CloudPrintResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-cloudprintresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="888e5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="888e5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="888e5-128">дисковеримакспринтерлимит</span><span class="sxs-lookup"><span data-stu-id="888e5-128">DiscoveryMaxPrinterLimit</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-discoverymaxprinterlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="888e5-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="888e5-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="888e5-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="888e5-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="888e5-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="888e5-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="888e5-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="888e5-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="888e5-135">моприадисковериресаурцеид</span><span class="sxs-lookup"><span data-stu-id="888e5-135">MopriaDiscoveryResourceId</span></span>](/windows/client-management/mdm/policy-csp-enterprisecloudprint#enterprisecloudprint-mopriadiscoveryresourceid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="888e5-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="888e5-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="888e5-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="888e5-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="888e5-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="888e5-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="888e5-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="888e5-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="888e5-141">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="888e5-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="888e5-142">Требования</span><span class="sxs-lookup"><span data-stu-id="888e5-142">Requirements</span></span>



| <span data-ttu-id="888e5-143">Требование</span><span class="sxs-lookup"><span data-stu-id="888e5-143">Requirement</span></span> | <span data-ttu-id="888e5-144">Значение</span><span class="sxs-lookup"><span data-stu-id="888e5-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="888e5-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="888e5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="888e5-146">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="888e5-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="888e5-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="888e5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="888e5-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="888e5-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="888e5-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="888e5-149">Namespace</span></span><br/>                | <span data-ttu-id="888e5-150">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="888e5-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="888e5-151">MOF</span><span class="sxs-lookup"><span data-stu-id="888e5-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="888e5-152"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="888e5-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="888e5-153">DLL</span><span class="sxs-lookup"><span data-stu-id="888e5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="888e5-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="888e5-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

