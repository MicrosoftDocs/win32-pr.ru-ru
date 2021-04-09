---
title: Класс MDM_ClientCertificateInstall_SCEP01_01
description: Класс MDM \_ клиентцертификатеинсталл \_ SCEP01 \_ 01 обеспечивает доступ к узлу для установки сертификата SCEP, используя уникальные идентификаторы для различения разных запросов на установку сертификатов.
ms.assetid: 273e6ef7-fd00-4049-bb8b-b9900b3d250b
keywords:
- Класс MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_SCEP01_01
- MDM_ClientCertificateInstall_SCEP01_01.InstanceID
- MDM_ClientCertificateInstall_SCEP01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f8db7decb2e3ae0674381b2f17df10f82ee38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892326"
---
# <a name="mdm_clientcertificateinstall_scep01_01-class"></a><span data-ttu-id="e933f-105">\_Класс MDM клиентцертификатеинсталл \_ SCEP01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="e933f-105">MDM\_ClientCertificateInstall\_SCEP01\_01 class</span></span>

<span data-ttu-id="e933f-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="e933f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e933f-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="e933f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e933f-108">Класс **MDM \_ клиентцертификатеинсталл \_ SCEP01 \_ 01** обеспечивает доступ к узлу для установки сертификата SCEP, используя уникальные идентификаторы для различения разных запросов на установку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e933f-108">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class enables access to the node for SCEP certificate installation, using unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="e933f-109">Требуется для установки сертификата SCEP.</span><span class="sxs-lookup"><span data-stu-id="e933f-109">Required for SCEP certificate installation.</span></span>

<span data-ttu-id="e933f-110">Поддерживаемые операции: Get, Add и DELETE.</span><span class="sxs-lookup"><span data-stu-id="e933f-110">Supported operations are Get, Add and Delete.</span></span>

<span data-ttu-id="e933f-111">Вызов Delete на этом узле должен удалить соответствующий сертификат SCEP.</span><span class="sxs-lookup"><span data-stu-id="e933f-111">Calling Delete on the this node should delete the corresponding SCEP certificate.</span></span>

<span data-ttu-id="e933f-112">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e933f-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e933f-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e933f-113">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_SCEP01_01
{
  string InstanceID;
  string ParentID;
  string CertThumbprint;
  sint32 Status;
  sint32 ErrorCode;
  string RespondentServerUrl;
};
```

## <a name="members"></a><span data-ttu-id="e933f-114">Члены</span><span class="sxs-lookup"><span data-stu-id="e933f-114">Members</span></span>

<span data-ttu-id="e933f-115">Класс **MDM \_ клиентцертификатеинсталл \_ SCEP01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e933f-115">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="e933f-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="e933f-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e933f-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="e933f-117">Properties</span></span>

<span data-ttu-id="e933f-118">Класс **MDM \_ клиентцертификатеинсталл \_ SCEP01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="e933f-118">The **MDM\_ClientCertificateInstall\_SCEP01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e933f-119">CertThumbprint</span><span class="sxs-lookup"><span data-stu-id="e933f-119">CertThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-certthumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e933f-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e933f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e933f-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e933f-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e933f-122">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="e933f-122">ErrorCode</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-errorcode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e933f-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e933f-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e933f-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e933f-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e933f-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e933f-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e933f-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e933f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e933f-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e933f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e933f-128">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e933f-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e933f-129">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="e933f-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="e933f-130">Для этого класса — уникальный идентификатор для различения разных запросов на установку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="e933f-130">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

<span data-ttu-id="e933f-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e933f-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e933f-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e933f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e933f-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e933f-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e933f-134">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e933f-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e933f-135">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="e933f-135">Describes the full path to the parent node.</span></span>

<span data-ttu-id="e933f-136">Строка имеет значение "./вендор/мсфт/клиентцертификатеинсталл/сцеп"</span><span class="sxs-lookup"><span data-stu-id="e933f-136">The string is "./Vendor/MSFT/ClientCertificateInstall/SCEP"</span></span>

</dd> <dt>

[<span data-ttu-id="e933f-137">респондентсерверурл</span><span class="sxs-lookup"><span data-stu-id="e933f-137">RespondentServerUrl</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-respondentserverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e933f-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e933f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e933f-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e933f-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e933f-140">Состояние</span><span class="sxs-lookup"><span data-stu-id="e933f-140">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e933f-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="e933f-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e933f-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="e933f-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e933f-143">Требования</span><span class="sxs-lookup"><span data-stu-id="e933f-143">Requirements</span></span>



| <span data-ttu-id="e933f-144">Требование</span><span class="sxs-lookup"><span data-stu-id="e933f-144">Requirement</span></span> | <span data-ttu-id="e933f-145">Значение</span><span class="sxs-lookup"><span data-stu-id="e933f-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e933f-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e933f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e933f-147">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e933f-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e933f-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e933f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e933f-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e933f-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e933f-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e933f-150">Namespace</span></span><br/>                | <span data-ttu-id="e933f-151">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="e933f-151">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e933f-152">MOF</span><span class="sxs-lookup"><span data-stu-id="e933f-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e933f-153"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e933f-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e933f-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e933f-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e933f-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e933f-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e933f-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e933f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e933f-157">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="e933f-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

