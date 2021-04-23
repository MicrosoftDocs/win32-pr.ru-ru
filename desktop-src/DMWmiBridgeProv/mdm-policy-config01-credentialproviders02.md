---
title: Класс MDM_Policy_Config01_CredentialProviders02
description: '\_Класс политики MDM \_ Config01 \_ CredentialProviders02 настраивает доступные политики поставщика учетных данных.'
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- Класс MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489918"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a><span data-ttu-id="dd0f5-105">\_Класс политики MDM \_ Config01 \_ CredentialProviders02</span><span class="sxs-lookup"><span data-stu-id="dd0f5-105">MDM\_Policy\_Config01\_CredentialProviders02 class</span></span>

<span data-ttu-id="dd0f5-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="dd0f5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd0f5-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="dd0f5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd0f5-108">\_Класс политики MDM \_ Config01 \_ CredentialProviders02 настраивает доступные политики поставщика учетных данных.</span><span class="sxs-lookup"><span data-stu-id="dd0f5-108">The MDM\_Policy\_Config01\_CredentialProviders02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="dd0f5-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dd0f5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0f5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd0f5-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="dd0f5-111">Члены</span><span class="sxs-lookup"><span data-stu-id="dd0f5-111">Members</span></span>

<span data-ttu-id="dd0f5-112">Класс **\_ политики MDM \_ Config01 \_ CredentialProviders02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd0f5-112">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="dd0f5-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd0f5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd0f5-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd0f5-114">Properties</span></span>

<span data-ttu-id="dd0f5-115">Класс **\_ политики MDM \_ Config01 \_ CredentialProviders02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd0f5-115">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dd0f5-116">алловпинлогон</span><span class="sxs-lookup"><span data-stu-id="dd0f5-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd0f5-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd0f5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd0f5-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd0f5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd0f5-119">блоккпиктурепассворд</span><span class="sxs-lookup"><span data-stu-id="dd0f5-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd0f5-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd0f5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd0f5-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd0f5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd0f5-122">DisableAutomaticReDeploymentCredentials</span><span class="sxs-lookup"><span data-stu-id="dd0f5-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd0f5-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="dd0f5-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd0f5-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dd0f5-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd0f5-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd0f5-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd0f5-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd0f5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd0f5-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd0f5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd0f5-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd0f5-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd0f5-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd0f5-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd0f5-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dd0f5-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd0f5-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd0f5-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd0f5-132">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd0f5-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd0f5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="dd0f5-133">Requirements</span></span>



| <span data-ttu-id="dd0f5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="dd0f5-134">Requirement</span></span> | <span data-ttu-id="dd0f5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="dd0f5-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0f5-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd0f5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dd0f5-137">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dd0f5-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd0f5-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd0f5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dd0f5-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dd0f5-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd0f5-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dd0f5-140">Namespace</span></span><br/>                | <span data-ttu-id="dd0f5-141">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="dd0f5-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dd0f5-142">MOF</span><span class="sxs-lookup"><span data-stu-id="dd0f5-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd0f5-143"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd0f5-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd0f5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="dd0f5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd0f5-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd0f5-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

