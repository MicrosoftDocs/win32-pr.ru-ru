---
title: Класс MDM_ClientCertificateInstall_PFXCertInstall01_01
description: Класс MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01 позволяет Организации использовать уникальные идентификаторы для различения разных запросов на установку сертификатов.
ms.assetid: 13b4d646-b49e-4a9d-b644-b52279249063
keywords:
- Класс MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_PFXCertInstall01_01
- MDM_ClientCertificateInstall_PFXCertInstall01_01.InstanceID
- MDM_ClientCertificateInstall_PFXCertInstall01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed0bbbfad0e61a95fa8130921e639de1772233d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136790"
---
# <a name="mdm_clientcertificateinstall_pfxcertinstall01_01-class"></a><span data-ttu-id="d9a58-105">\_Класс MDM клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="d9a58-105">MDM\_ClientCertificateInstall\_PFXCertInstall01\_01 class</span></span>

<span data-ttu-id="d9a58-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="d9a58-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d9a58-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="d9a58-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d9a58-108">Класс **MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01** позволяет Организации использовать уникальные идентификаторы для различения разных запросов на установку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d9a58-108">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class enables the enterprise to use unique IDs to differentiate different certificate install requests.</span></span>

<span data-ttu-id="d9a58-109">Требуется для установки сертификата PFX.</span><span class="sxs-lookup"><span data-stu-id="d9a58-109">Required for PFX certificate installation.</span></span> <span data-ttu-id="d9a58-110">При вызове Delete на этом узле необходимо удалить сертификаты и ключи, которые были установлены соответствующим BLOB-объектом PFX.</span><span class="sxs-lookup"><span data-stu-id="d9a58-110">Calling Delete on the this node, should delete the certificates and the keys that were installed by the corresponding PFX blob.</span></span>

<span data-ttu-id="d9a58-111">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d9a58-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9a58-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9a58-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_PFXCertInstall01_01
{
  string  InstanceID;
  string  ParentID;
  sint32  KeyLocation;
  string  ContainerName;
  string  PFXCertBlob;
  string  PFXCertPassword;
  sint32  PFXCertPasswordEncryptionType;
  boolean PFXKeyExportable;
  string  Thumbprint;
  sint32  Status;
  string  PFXCertPasswordEncryptionStore;
};
```

## <a name="members"></a><span data-ttu-id="d9a58-113">Члены</span><span class="sxs-lookup"><span data-stu-id="d9a58-113">Members</span></span>

<span data-ttu-id="d9a58-114">Класс **MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9a58-114">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="d9a58-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9a58-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9a58-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9a58-116">Properties</span></span>

<span data-ttu-id="d9a58-117">Класс **MDM \_ клиентцертификатеинсталл \_ PFXCertInstall01 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="d9a58-117">The **MDM\_ClientCertificateInstall\_PFXCertInstall01\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d9a58-118">ContainerName</span><span class="sxs-lookup"><span data-stu-id="d9a58-118">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a58-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9a58-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d9a58-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a58-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a58-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-124">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9a58-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9a58-125">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="d9a58-125">Identifies the name of the parent node.</span></span> <span data-ttu-id="d9a58-126">Для этого класса — уникальный идентификатор для различения разных запросов на установку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d9a58-126">For this class, a unique ID to differentiate different certificate install requests.</span></span>

</dd> <dt>

[<span data-ttu-id="d9a58-127">KeyLocation</span><span class="sxs-lookup"><span data-stu-id="d9a58-127">KeyLocation</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-keylocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d9a58-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d9a58-130">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d9a58-130">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a58-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9a58-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9a58-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9a58-134">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="d9a58-134">Describes the full path to the parent node.</span></span>

<span data-ttu-id="d9a58-135">Строка имеет значение "./вендор/мсфт/клиентцертификатеинсталл/пфксцертинсталл"</span><span class="sxs-lookup"><span data-stu-id="d9a58-135">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall"</span></span>

</dd> <dt>

[<span data-ttu-id="d9a58-136">пфксцертблоб</span><span class="sxs-lookup"><span data-stu-id="d9a58-136">PFXCertBlob</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertblob)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a58-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-139">Квалификаторы: **октетстринг**</span><span class="sxs-lookup"><span data-stu-id="d9a58-139">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a58-140">пфксцертпассворд</span><span class="sxs-lookup"><span data-stu-id="d9a58-140">PFXCertPassword</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a58-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a58-143">пфксцертпассворденкриптионсторе</span><span class="sxs-lookup"><span data-stu-id="d9a58-143">PFXCertPasswordEncryptionStore</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptionstore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a58-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a58-146">пфксцертпассворденкриптионтипе</span><span class="sxs-lookup"><span data-stu-id="d9a58-146">PFXCertPasswordEncryptionType</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxcertpasswordencryptiontype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d9a58-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a58-149">пфкскэйекспортабле</span><span class="sxs-lookup"><span data-stu-id="d9a58-149">PFXKeyExportable</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-pfxkeyexportable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-150">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9a58-150">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a58-152">Состояние</span><span class="sxs-lookup"><span data-stu-id="d9a58-152">Status</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="d9a58-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d9a58-155">Отпечаток</span><span class="sxs-lookup"><span data-stu-id="d9a58-155">Thumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-thumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9a58-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9a58-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9a58-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d9a58-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9a58-158">Требования</span><span class="sxs-lookup"><span data-stu-id="d9a58-158">Requirements</span></span>



| <span data-ttu-id="d9a58-159">Требование</span><span class="sxs-lookup"><span data-stu-id="d9a58-159">Requirement</span></span> | <span data-ttu-id="d9a58-160">Значение</span><span class="sxs-lookup"><span data-stu-id="d9a58-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a58-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9a58-161">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a58-162">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d9a58-162">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9a58-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9a58-163">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a58-164">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d9a58-164">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d9a58-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9a58-165">Namespace</span></span><br/>                | <span data-ttu-id="d9a58-166">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="d9a58-166">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d9a58-167">MOF</span><span class="sxs-lookup"><span data-stu-id="d9a58-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9a58-168"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9a58-168"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9a58-169">DLL</span><span class="sxs-lookup"><span data-stu-id="d9a58-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9a58-170"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9a58-170"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a58-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9a58-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a58-172">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="d9a58-172">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

