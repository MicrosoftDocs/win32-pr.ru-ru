---
title: Класс MDM_Policy_Config01_NetworkIsolation02
description: '\_Класс политики MDM \_ Config01 \_ NetworkIsolation02 представляет доступные политики браузера.'
ms.assetid: f25ecbef-d232-4731-bac8-38a7d597db00
keywords:
- Класс MDM_Policy_Config01_NetworkIsolation02
- MDM_Policy_Config01_NetworkIsolation02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_NetworkIsolation02
- MDM_Policy_Config01_NetworkIsolation02.InstanceID
- MDM_Policy_Config01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9062d150de07860fd9d5b2510269ddcc3d2f8a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071600"
---
# <a name="mdm_policy_config01_networkisolation02-class"></a><span data-ttu-id="db335-105">\_Класс политики MDM \_ Config01 \_ NetworkIsolation02</span><span class="sxs-lookup"><span data-stu-id="db335-105">MDM\_Policy\_Config01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="db335-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="db335-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="db335-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="db335-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="db335-108">Класс **\_ политики MDM \_ Config01 \_ NetworkIsolation02** представляет доступные политики браузера.</span><span class="sxs-lookup"><span data-stu-id="db335-108">The **MDM\_Policy\_Config01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="db335-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="db335-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="db335-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db335-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string NeutralResources;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="db335-111">Члены</span><span class="sxs-lookup"><span data-stu-id="db335-111">Members</span></span>

<span data-ttu-id="db335-112">Класс **\_ политики MDM \_ Config01 \_ NetworkIsolation02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="db335-112">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="db335-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="db335-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db335-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="db335-114">Properties</span></span>

<span data-ttu-id="db335-115">Класс **\_ политики MDM \_ Config01 \_ NetworkIsolation02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="db335-115">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="db335-116">ентерприсеклаудресаурцес</span><span class="sxs-lookup"><span data-stu-id="db335-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="db335-119">ентерприсеинтерналпроксисерверс</span><span class="sxs-lookup"><span data-stu-id="db335-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="db335-122">ентерприсеипранже</span><span class="sxs-lookup"><span data-stu-id="db335-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="db335-125">ентерприсеипранжесареаусоритативе</span><span class="sxs-lookup"><span data-stu-id="db335-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="db335-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="db335-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="db335-128">ентерприсенетворкдомаиннамес</span><span class="sxs-lookup"><span data-stu-id="db335-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="db335-131">ентерприсепроксисерверс</span><span class="sxs-lookup"><span data-stu-id="db335-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="db335-134">ентерприсепроксисерверсареаусоритативе</span><span class="sxs-lookup"><span data-stu-id="db335-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="db335-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="db335-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="db335-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="db335-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db335-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db335-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="db335-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="db335-141">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="db335-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="db335-142">Для этого класса строка имеет значение "Нетворкисолатион".</span><span class="sxs-lookup"><span data-stu-id="db335-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="db335-143">неутралресаурцес</span><span class="sxs-lookup"><span data-stu-id="db335-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="db335-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="db335-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="db335-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db335-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db335-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db335-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db335-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db335-149">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="db335-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="db335-150">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="db335-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="db335-151">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="db335-151">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db335-152">Требования</span><span class="sxs-lookup"><span data-stu-id="db335-152">Requirements</span></span>



| <span data-ttu-id="db335-153">Требование</span><span class="sxs-lookup"><span data-stu-id="db335-153">Requirement</span></span> | <span data-ttu-id="db335-154">Значение</span><span class="sxs-lookup"><span data-stu-id="db335-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db335-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db335-155">Minimum supported client</span></span><br/> | <span data-ttu-id="db335-156">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="db335-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db335-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db335-157">Minimum supported server</span></span><br/> | <span data-ttu-id="db335-158">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="db335-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="db335-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db335-159">Namespace</span></span><br/>                | <span data-ttu-id="db335-160">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="db335-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="db335-161">MOF</span><span class="sxs-lookup"><span data-stu-id="db335-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db335-162"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db335-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="db335-163">DLL</span><span class="sxs-lookup"><span data-stu-id="db335-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db335-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db335-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

