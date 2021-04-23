---
title: Класс Win32_TSDeploymentSettings
description: Определяет параметры по умолчанию, используемые диспетчер удаленных приложений RemoteApp при создании файлов протокол удаленного рабочего стола (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSDeploymentSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSDeploymentSettings, описание
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490284"
---
# <a name="win32_tsdeploymentsettings-class"></a><span data-ttu-id="b37ef-105">\_Класс Win32 тсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="b37ef-105">Win32\_TSDeploymentSettings class</span></span>

<span data-ttu-id="b37ef-106">Определяет параметры по умолчанию, используемые диспетчер удаленных приложений RemoteApp при создании файлов протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="b37ef-106">Defines the default settings that the RemoteApp Manager uses when creating Remote Desktop Protocol (RDP) files.</span></span> <span data-ttu-id="b37ef-107">Эти параметры не влияют на опубликованные приложения или рабочие столы.</span><span class="sxs-lookup"><span data-stu-id="b37ef-107">These settings do not affect any published applications or desktops.</span></span>

## <a name="syntax"></a><span data-ttu-id="b37ef-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b37ef-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="b37ef-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b37ef-109">Members</span></span>

<span data-ttu-id="b37ef-110">Класс **Win32 \_ тсдеплойментсеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b37ef-110">The **Win32\_TSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="b37ef-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b37ef-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b37ef-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="b37ef-112">Properties</span></span>

<span data-ttu-id="b37ef-113">Класс **Win32 \_ тсдеплойментсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b37ef-113">The **Win32\_TSDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b37ef-114">**алловфонтсмусинг**</span><span class="sxs-lookup"><span data-stu-id="b37ef-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-115">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b37ef-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-117">Указывает, разрешено ли сглаживание шрифтов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-117">Indicates whether to allow font smoothing.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b37ef-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b37ef-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b37ef-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-122">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="b37ef-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b37ef-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ef-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-124">**цертификатикспиресон**</span><span class="sxs-lookup"><span data-stu-id="b37ef-124">**CertificateExpiresOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-127">Дата истечения срока действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="b37ef-127">The date that the certificate expires on.</span></span> <span data-ttu-id="b37ef-128">Это значение хранится в формате 64-разрядного [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="b37ef-128">This value is stored as a 64-bit [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-129">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="b37ef-129">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-130">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b37ef-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-132">Отпечаток сертификата, который используется для подписи RDP-файлов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-132">The thumbprint of the certificate that is used to sign RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-133">**цертификатеиссуедби**</span><span class="sxs-lookup"><span data-stu-id="b37ef-133">**CertificateIssuedBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-136">Указывает, кому выдан сертификат.</span><span class="sxs-lookup"><span data-stu-id="b37ef-136">Specifies who the certificate is issued by.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-137">**цертификатеиссуедто**</span><span class="sxs-lookup"><span data-stu-id="b37ef-137">**CertificateIssuedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-140">Указывает, кому выдан сертификат.</span><span class="sxs-lookup"><span data-stu-id="b37ef-140">Specifies who the certificate is issued to.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-141">**колорбитдепс**</span><span class="sxs-lookup"><span data-stu-id="b37ef-141">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-142">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b37ef-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-144">Глубина цветового бита дисплея.</span><span class="sxs-lookup"><span data-stu-id="b37ef-144">The color bit depth of the display.</span></span> <span data-ttu-id="b37ef-145">Возможные значения: 4, 8, 15, 16, 24 и 32.</span><span class="sxs-lookup"><span data-stu-id="b37ef-145">Possible values are 4, 8, 15, 16, 24, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-146">**кустомрдпсеттингс**</span><span class="sxs-lookup"><span data-stu-id="b37ef-146">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-149">Содержимое RDP-файла, соответствующего настраиваемым параметрам RDP в диспетчер удаленных приложений RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b37ef-149">The contents of the RDP file that correspond to the Custom RDP Settings in RemoteApp Manager.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-150">**деплойментрдпсеттингс**</span><span class="sxs-lookup"><span data-stu-id="b37ef-150">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-153">Содержимое RDP-файла, соответствующего параметрам развертывания в диспетчер удаленных приложений RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b37ef-153">The contents of the RDP file that correspond to the deployment settings in RemoteApp Manager.</span></span> <span data-ttu-id="b37ef-154">Если задано это значение, параметры развертывания RDP заменяют параметры по умолчанию в этом классе.</span><span class="sxs-lookup"><span data-stu-id="b37ef-154">If this value is set, the RDP deployment settings supersede the default settings in this class.</span></span> <span data-ttu-id="b37ef-155">Например, если задать свойство **гатевайаусмоде** в этом классе и задать свойство **деплойментрдпсеттингс** , то свойство **гатевайаусмоде** из этого класса будет игнорироваться и будет использоваться значение **гатевайаусмоде** из **деплойментрдпсеттингс** .</span><span class="sxs-lookup"><span data-stu-id="b37ef-155">For example, if you set the **GatewayAuthMode** property in this class, and set the **DeploymentRDPSettings** property, the **GatewayAuthMode** property from this class will be ignored and the **GatewayAuthMode** value from the **DeploymentRDPSettings** will be used.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-156">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b37ef-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b37ef-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-159">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b37ef-159">Description of the object.</span></span>

<span data-ttu-id="b37ef-160">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ef-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-161">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="b37ef-161">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-164">Имя сервера узла сеансов удаленных рабочих столов или полное доменное имя фермы серверов узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-164">The name of the RD Session Host server, or the fully qualified domain name (FQDN) of the RD Session Host server farm.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-165">**гатевайаусмоде**</span><span class="sxs-lookup"><span data-stu-id="b37ef-165">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-166">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b37ef-166">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-167">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-168">Метод проверки подлинности шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-168">The RD Gateway authentication method.</span></span> <span data-ttu-id="b37ef-169">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b37ef-169">The following values are possible.</span></span>

<dt>

<span data-ttu-id="b37ef-170">0</span><span class="sxs-lookup"><span data-stu-id="b37ef-170">0</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-171">Пароль</span><span class="sxs-lookup"><span data-stu-id="b37ef-171">Password</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-172">1</span><span class="sxs-lookup"><span data-stu-id="b37ef-172">1</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-173">Смарт-карта</span><span class="sxs-lookup"><span data-stu-id="b37ef-173">Smart card</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-174">4</span><span class="sxs-lookup"><span data-stu-id="b37ef-174">4</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-175">Разрешить пользователю выбирать во время подключения.</span><span class="sxs-lookup"><span data-stu-id="b37ef-175">Allow user to select during connection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b37ef-176">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="b37ef-176">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-179">Имя сервера шлюза удаленных рабочих столов для использования.</span><span class="sxs-lookup"><span data-stu-id="b37ef-179">The name of the RD Gateway server to use.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-180">**гатевайусаже**</span><span class="sxs-lookup"><span data-stu-id="b37ef-180">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-181">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b37ef-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-183">Указывает, следует ли использовать сервер шлюза удаленных рабочих столов для подключения к целевому серверу узла сеансов удаленных рабочих столов через брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="b37ef-183">Indicates whether to use an RD Gateway server to connect to the target RD Session Host server across a firewall.</span></span> <span data-ttu-id="b37ef-184">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b37ef-184">The following values are possible.</span></span>

<dt>

<span data-ttu-id="b37ef-185">0</span><span class="sxs-lookup"><span data-stu-id="b37ef-185">0</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-186">Не используйте сервер шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-186">Do not use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-187">1</span><span class="sxs-lookup"><span data-stu-id="b37ef-187">1</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-188">Используйте сервер шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-188">Use an RD Gateway server.</span></span> <span data-ttu-id="b37ef-189">Обход сервера шлюза удаленных рабочих столов для локальных адресов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-189">Bypass the RD Gateway server for local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-190">2</span><span class="sxs-lookup"><span data-stu-id="b37ef-190">2</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-191">Используйте сервер шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-191">Use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-192">3</span><span class="sxs-lookup"><span data-stu-id="b37ef-192">3</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-193">Автоматическое определение параметров сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-193">Automatically detect RD Gateway server settings.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b37ef-194">**гатевайусекачедкредс**</span><span class="sxs-lookup"><span data-stu-id="b37ef-194">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-195">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b37ef-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-196">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-196">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-197">По возможности используйте те же учетные данные пользователя для сервера шлюза удаленных рабочих столов и сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-197">When possible, use the same user credentials for the RD Gateway server and the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-198">**хасцертификате**</span><span class="sxs-lookup"><span data-stu-id="b37ef-198">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-199">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b37ef-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-200">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-201">Указывает, следует ли использовать сертификат для подписывания RDP-файлов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-201">Indicates whether to use a certificate to sign the RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b37ef-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-203">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b37ef-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b37ef-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-205">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="b37ef-205">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-206">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b37ef-206">The date the object was installed.</span></span> <span data-ttu-id="b37ef-207">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="b37ef-207">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b37ef-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ef-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-209">**Name**</span><span class="sxs-lookup"><span data-stu-id="b37ef-209">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b37ef-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-212">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="b37ef-212">The name of the object.</span></span>

<span data-ttu-id="b37ef-213">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ef-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-214">**порт**.</span><span class="sxs-lookup"><span data-stu-id="b37ef-214">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-215">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b37ef-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-216">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-217">Используемый порт RDP.</span><span class="sxs-lookup"><span data-stu-id="b37ef-217">The RDP port to use.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-218">**редиректионоптионс**</span><span class="sxs-lookup"><span data-stu-id="b37ef-218">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-219">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="b37ef-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-221">Указывает параметры перенаправления устройств и ресурсов для подключений RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b37ef-221">Specifies the device and resource redirection options for RemoteApp connections.</span></span> <span data-ttu-id="b37ef-222">Флаги для **редиректионоптионс** можно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="b37ef-222">Flags for **RedirectionOptions** can be combined.</span></span> <span data-ttu-id="b37ef-223">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b37ef-223">The following values are possible.</span></span>

<dt>

<span data-ttu-id="b37ef-224">0</span><span class="sxs-lookup"><span data-stu-id="b37ef-224">0</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-225">Нет перенаправления устройства или ресурса.</span><span class="sxs-lookup"><span data-stu-id="b37ef-225">No device or resource redirection.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-226">1</span><span class="sxs-lookup"><span data-stu-id="b37ef-226">1</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-227">Перенаправление дисков.</span><span class="sxs-lookup"><span data-stu-id="b37ef-227">Redirect disk drives.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-228">2</span><span class="sxs-lookup"><span data-stu-id="b37ef-228">2</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-229">Перенаправление принтеров.</span><span class="sxs-lookup"><span data-stu-id="b37ef-229">Redirect printers.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-230">4</span><span class="sxs-lookup"><span data-stu-id="b37ef-230">4</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-231">Перенаправление буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="b37ef-231">Redirect the Clipboard.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-232">8</span><span class="sxs-lookup"><span data-stu-id="b37ef-232">8</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-233">Перенаправление поддерживаемых самонастраивающийся устройств.</span><span class="sxs-lookup"><span data-stu-id="b37ef-233">Redirect supported Plug and Play devices.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-234">16</span><span class="sxs-lookup"><span data-stu-id="b37ef-234">16</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-235">Перенаправление смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="b37ef-235">Redirect smart cards.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-236">32</span><span class="sxs-lookup"><span data-stu-id="b37ef-236">32</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-237">Перенаправление звука.</span><span class="sxs-lookup"><span data-stu-id="b37ef-237">Redirect audio.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-238">64</span><span class="sxs-lookup"><span data-stu-id="b37ef-238">64</span></span>
</dt> <dd>

<span data-ttu-id="b37ef-239">Перенаправление последовательных портов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-239">Redirect serial ports.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b37ef-240">**рекуиресервераус**</span><span class="sxs-lookup"><span data-stu-id="b37ef-240">**RequireServerAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-241">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b37ef-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-242">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-243">Указывает, требуется ли проверка подлинности сервера.</span><span class="sxs-lookup"><span data-stu-id="b37ef-243">Indicates whether to require server authentication.</span></span>

</dd> <dt>

<span data-ttu-id="b37ef-244">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b37ef-244">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b37ef-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-246">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b37ef-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-247">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b37ef-247">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-248">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b37ef-248">Current status of the object.</span></span> <span data-ttu-id="b37ef-249">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="b37ef-249">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b37ef-250">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="b37ef-250">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b37ef-251">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="b37ef-251">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b37ef-252">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="b37ef-252">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b37ef-253">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b37ef-253">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b37ef-254">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b37ef-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b37ef-255">("ОК")</span><span class="sxs-lookup"><span data-stu-id="b37ef-255">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b37ef-256">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="b37ef-256">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b37ef-257">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="b37ef-257">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b37ef-258">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b37ef-258">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b37ef-259">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b37ef-259">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b37ef-260">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b37ef-260">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b37ef-261">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="b37ef-261">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b37ef-262">("Служба")</span><span class="sxs-lookup"><span data-stu-id="b37ef-262">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b37ef-263">**усемултимон**</span><span class="sxs-lookup"><span data-stu-id="b37ef-263">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b37ef-264">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b37ef-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b37ef-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b37ef-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b37ef-266">Указывает, разрешено ли для рабочего стола несколько мониторов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-266">Indicates if multiple monitors are enabled for the desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b37ef-267">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b37ef-267">Remarks</span></span>

<span data-ttu-id="b37ef-268">Для задания свойств с помощью этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-268">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="b37ef-269">Если **рекуиресервераус** имеет значение **true**, учитывайте следующее.</span><span class="sxs-lookup"><span data-stu-id="b37ef-269">If **RequireServerAuth** is set to **TRUE**, consider the following:</span></span>

-   <span data-ttu-id="b37ef-270">Если программа RemoteApp предназначена для использования в интрасети и все клиентские компьютеры работают под управлением Windows Server 2008 или Windows Vista, нет необходимости настраивать сервер узла сеансов удаленных рабочих столов для использования SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="b37ef-270">If the RemoteApp program is for intranet use, and all client computers are running either Windows Server 2008 or Windows Vista, you do not have to configure the RD Session Host server to use an SSL certificate.</span></span> <span data-ttu-id="b37ef-271">В этом случае используется проверка подлинности на уровне сети.</span><span class="sxs-lookup"><span data-stu-id="b37ef-271">In this case, Network Level Authentication is used.</span></span>
-   <span data-ttu-id="b37ef-272">Необходимо указать полное доменное имя сервера или фермы в качестве значения свойства **фармнаме** .</span><span class="sxs-lookup"><span data-stu-id="b37ef-272">You must specify the FQDN of the server or farm for the value of the **FarmName** property.</span></span>

<span data-ttu-id="b37ef-273">Для подключения к \\ пространству имен "CIMV2 терминалсервицес" уровень проверки подлинности должен включать конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-273">To connect to the "CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="b37ef-274">Для вызовов C/C++ это уровень проверки подлинности " **PKT" RPC \_ C \_ AUTHN \_ Level \_ \_**, который можно задать с помощью функции [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) com.</span><span class="sxs-lookup"><span data-stu-id="b37ef-274">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="b37ef-275">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="b37ef-275">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="b37ef-276">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="b37ef-276">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="b37ef-277">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="b37ef-277">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b37ef-278">Они устанавливаются на компьютере при добавлении связанной роли.</span><span class="sxs-lookup"><span data-stu-id="b37ef-278">They are installed on the computer when you add the associated role.</span></span> <span data-ttu-id="b37ef-279">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b37ef-279">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b37ef-280">Требования</span><span class="sxs-lookup"><span data-stu-id="b37ef-280">Requirements</span></span>



| <span data-ttu-id="b37ef-281">Требование</span><span class="sxs-lookup"><span data-stu-id="b37ef-281">Requirement</span></span> | <span data-ttu-id="b37ef-282">Значение</span><span class="sxs-lookup"><span data-stu-id="b37ef-282">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b37ef-283">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b37ef-283">Minimum supported client</span></span><br/> | <span data-ttu-id="b37ef-284">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b37ef-284">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b37ef-285">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b37ef-285">Minimum supported server</span></span><br/> | <span data-ttu-id="b37ef-286">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b37ef-286">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b37ef-287">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b37ef-287">Namespace</span></span><br/>                | <span data-ttu-id="b37ef-288">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="b37ef-288">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b37ef-289">MOF</span><span class="sxs-lookup"><span data-stu-id="b37ef-289">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b37ef-290"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b37ef-290"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="b37ef-291">DLL</span><span class="sxs-lookup"><span data-stu-id="b37ef-291">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b37ef-292"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b37ef-292"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

