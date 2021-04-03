---
title: Класс MDM_ClientCertificateInstall_Install03
description: Класс MDM \_ клиентцертификатеинсталл \_ Install03 позволяет настроить установку сертификатов клиента на предприятии.
ms.assetid: 0083e54c-e621-47da-a20d-17c8bbf7dd3a
keywords:
- Класс MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03 класс, описание
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03
- MDM_ClientCertificateInstall_Install03.InstanceID
- MDM_ClientCertificateInstall_Install03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ac690808551e05d6ceba4f3c84bcaa521d4d01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136791"
---
# <a name="mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="a9508-105">\_Класс MDM клиентцертификатеинсталл \_ Install03</span><span class="sxs-lookup"><span data-stu-id="a9508-105">MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="a9508-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="a9508-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a9508-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="a9508-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a9508-108">Класс **MDM \_ клиентцертификатеинсталл \_ Install03** позволяет настроить установку сертификатов клиента на предприятии. Требуется для регистрации сертификата SCEP.</span><span class="sxs-lookup"><span data-stu-id="a9508-108">The **MDM\_ClientCertificateInstall\_Install03** class enables the enterprise to set the installation of client certificates.Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="a9508-109">Родительский узел для группирования запроса, связанного с установкой сертификата SCEP.</span><span class="sxs-lookup"><span data-stu-id="a9508-109">Parent node to group SCEP cert install related request.</span></span>

> [!Note]  
> <span data-ttu-id="a9508-110">Хотя дочерние узлы в разделе Install поддерживают команды replace, после отправки команды exec на устройство устройство принимает значения, заданные при принятии команды exec.</span><span class="sxs-lookup"><span data-stu-id="a9508-110">Even though the child nodes under Install support Replace commands, after the Exec command is sent to the device, the device will take the values which are set when the Exec command is accepted.</span></span> <span data-ttu-id="a9508-111">Сервер не должен предполагать, что изменение значения узла после принятия команды exec повлияет на текущую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="a9508-111">The server should not expect the node value change after Exec command is accepted will impact the current undergoing enrollment.</span></span> <span data-ttu-id="a9508-112">Сервер должен проверить значение узла состояния и убедиться, что устройство находится на неизвестном этапе, прежде чем изменять значения дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="a9508-112">The server should check the Status node value and make sure the device is not at unknown stage before changing child node values.</span></span>

 

<span data-ttu-id="a9508-113">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a9508-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9508-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9508-114">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_ClientCertificateInstall_Install03
{
  string InstanceID;
  string ParentID;
  string ServerURL;
  string Challenge;
  string EKUMapping;
  sint32 KeyUsage;
  string SubjectName;
  sint32 KeyProtection;
  sint32 RetryDelay;
  sint32 RetryCount;
  string TemplateName;
  sint32 KeyLength;
  string HashAlgorithm;
  string CAThumbprint;
  string SubjectAlternativeNames;
  string ValidPeriod;
  sint32 ValidPeriodUnits;
  string ContainerName;
  string CustomTextToShowInPrompt;
  string AADKeyIdentifierList;
};
```

## <a name="members"></a><span data-ttu-id="a9508-115">Члены</span><span class="sxs-lookup"><span data-stu-id="a9508-115">Members</span></span>

<span data-ttu-id="a9508-116">Класс **MDM \_ клиентцертификатеинсталл \_ Install03** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a9508-116">The **MDM\_ClientCertificateInstall\_Install03** class has these types of members:</span></span>

-   [<span data-ttu-id="a9508-117">Методы</span><span class="sxs-lookup"><span data-stu-id="a9508-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="a9508-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9508-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a9508-119">Методы</span><span class="sxs-lookup"><span data-stu-id="a9508-119">Methods</span></span>

<span data-ttu-id="a9508-120">Класс **MDM \_ клиентцертификатеинсталл \_ Install03** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a9508-120">The **MDM\_ClientCertificateInstall\_Install03** class has these methods.</span></span>



| <span data-ttu-id="a9508-121">Метод</span><span class="sxs-lookup"><span data-stu-id="a9508-121">Method</span></span>                                                                      | <span data-ttu-id="a9508-122">Описание</span><span class="sxs-lookup"><span data-stu-id="a9508-122">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="a9508-123">**енроллмесод**</span><span class="sxs-lookup"><span data-stu-id="a9508-123">**EnrollMethod**</span></span>](mdm-clientcertificateinstall-install03-enrollmethod.md) | <span data-ttu-id="a9508-124">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a9508-124">Required.</span></span> <span data-ttu-id="a9508-125">Активирует устройство для запуска регистрации сертификата.</span><span class="sxs-lookup"><span data-stu-id="a9508-125">Triggers the device to start the certificate enrollment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a9508-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="a9508-126">Properties</span></span>

<span data-ttu-id="a9508-127">Класс **MDM \_ клиентцертификатеинсталл \_ Install03** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a9508-127">The **MDM\_ClientCertificateInstall\_Install03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a9508-128">аадкэйидентифиерлист</span><span class="sxs-lookup"><span data-stu-id="a9508-128">AADKeyIdentifierList</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-aadkeyidentifierlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-131">касумбпринт</span><span class="sxs-lookup"><span data-stu-id="a9508-131">CAThumbprint</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-cathumbprint)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-134">Задача</span><span class="sxs-lookup"><span data-stu-id="a9508-134">Challenge</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-challenge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-137">ContainerName</span><span class="sxs-lookup"><span data-stu-id="a9508-137">ContainerName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-pfxcertinstall-uniqueid-containername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-140">кустомтексттошовинпромпт</span><span class="sxs-lookup"><span data-stu-id="a9508-140">CustomTextToShowInPrompt</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-customtexttoshowinprompt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-143">екумаппинг</span><span class="sxs-lookup"><span data-stu-id="a9508-143">EKUMapping</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-ekumapping)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="a9508-146">HashAlgorithm</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-hashalgorithm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9508-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9508-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9508-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9508-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a9508-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a9508-153">Требуется для регистрации сертификата SCEP.</span><span class="sxs-lookup"><span data-stu-id="a9508-153">Required for SCEP certificate enrollment.</span></span> <span data-ttu-id="a9508-154">Родительский узел для группирования запроса, связанного с установкой сертификата SCEP.</span><span class="sxs-lookup"><span data-stu-id="a9508-154">Parent node to group SCEP cert install related request.</span></span>

<span data-ttu-id="a9508-155">Формат — Node.</span><span class="sxs-lookup"><span data-stu-id="a9508-155">The Format is node.</span></span>

</dd> <dt>

[<span data-ttu-id="a9508-156">KeyLength</span><span class="sxs-lookup"><span data-stu-id="a9508-156">KeyLength</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keylength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-157">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a9508-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-159">кэйпротектион</span><span class="sxs-lookup"><span data-stu-id="a9508-159">KeyProtection</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-keyprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-160">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a9508-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-161">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-162">кэйусаже</span><span class="sxs-lookup"><span data-stu-id="a9508-162">KeyUsage</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-163">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a9508-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-164">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a9508-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a9508-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9508-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9508-168">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a9508-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a9508-169">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="a9508-169">Describes the full path to the parent node.</span></span>

<span data-ttu-id="a9508-170">Строка имеет значение "./вендор/мсфт/клиентцертификатеинсталл/пфксцертинсталл/сцеп/*UniqueID*"</span><span class="sxs-lookup"><span data-stu-id="a9508-170">The string is "./Vendor/MSFT/ClientCertificateInstall/PFXCertInstall/SCEP/*UniqueID*"</span></span>

</dd> <dt>

[<span data-ttu-id="a9508-171">RetryCount</span><span class="sxs-lookup"><span data-stu-id="a9508-171">RetryCount</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrycount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-172">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a9508-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-174">ретриделай</span><span class="sxs-lookup"><span data-stu-id="a9508-174">RetryDelay</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-retrydelay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-175">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a9508-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-176">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-177">ServerURL</span><span class="sxs-lookup"><span data-stu-id="a9508-177">ServerURL</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-serverurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-180">субжекталтернативенамес</span><span class="sxs-lookup"><span data-stu-id="a9508-180">SubjectAlternativeNames</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectalternativenames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-183">SubjectName</span><span class="sxs-lookup"><span data-stu-id="a9508-183">SubjectName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-subjectname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-185">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-186">TemplateName</span><span class="sxs-lookup"><span data-stu-id="a9508-186">TemplateName</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-templatename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-188">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-188">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-189">валидпериод</span><span class="sxs-lookup"><span data-stu-id="a9508-189">ValidPeriod</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a9508-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-191">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-191">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a9508-192">валидпериодунитс</span><span class="sxs-lookup"><span data-stu-id="a9508-192">ValidPeriodUnits</span></span>](/windows/client-management/mdm/clientcertificateinstall-csp#clientcertificateinstall-scep-uniqueid-install-validperiodunits)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9508-193">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="a9508-193">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a9508-194">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a9508-194">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9508-195">Требования</span><span class="sxs-lookup"><span data-stu-id="a9508-195">Requirements</span></span>



| <span data-ttu-id="a9508-196">Требование</span><span class="sxs-lookup"><span data-stu-id="a9508-196">Requirement</span></span> | <span data-ttu-id="a9508-197">Значение</span><span class="sxs-lookup"><span data-stu-id="a9508-197">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9508-198">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9508-198">Minimum supported client</span></span><br/> | <span data-ttu-id="a9508-199">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a9508-199">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9508-200">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9508-200">Minimum supported server</span></span><br/> | <span data-ttu-id="a9508-201">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a9508-201">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a9508-202">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a9508-202">Namespace</span></span><br/>                | <span data-ttu-id="a9508-203">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="a9508-203">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a9508-204">MOF</span><span class="sxs-lookup"><span data-stu-id="a9508-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9508-205"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9508-205"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9508-206">DLL</span><span class="sxs-lookup"><span data-stu-id="a9508-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9508-207"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9508-207"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9508-208">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9508-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9508-209">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="a9508-209">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

