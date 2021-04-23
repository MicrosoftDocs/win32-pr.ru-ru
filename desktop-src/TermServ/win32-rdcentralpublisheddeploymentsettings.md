---
title: Класс Win32_RDCentralPublishedDeploymentSettings
description: Содержит параметры развертывания, используемые для создания RDP-файлов для ресурсов, опубликованных из фермы.
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDCentralPublishedDeploymentSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDCentralPublishedDeploymentSettings, описание
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416037"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a><span data-ttu-id="f3257-105">\_Класс Win32 рдцентралпублишеддеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="f3257-105">Win32\_RDCentralPublishedDeploymentSettings class</span></span>

<span data-ttu-id="f3257-106">Содержит параметры развертывания, используемые для создания RDP-файлов для ресурсов, опубликованных из фермы.</span><span class="sxs-lookup"><span data-stu-id="f3257-106">Contains the deployment settings used to generate RDP files for resources published from a farm.</span></span>

<span data-ttu-id="f3257-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f3257-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3257-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3257-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="f3257-109">Члены</span><span class="sxs-lookup"><span data-stu-id="f3257-109">Members</span></span>

<span data-ttu-id="f3257-110">Класс **Win32 \_ рдцентралпублишеддеплойментсеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f3257-110">The **Win32\_RDCentralPublishedDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="f3257-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3257-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3257-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3257-112">Properties</span></span>

<span data-ttu-id="f3257-113">Класс **Win32 \_ рдцентралпублишеддеплойментсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f3257-113">The **Win32\_RDCentralPublishedDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3257-114">**алловфонтсмусинг**</span><span class="sxs-lookup"><span data-stu-id="f3257-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-115">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3257-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-117">**значение true** , чтобы разрешить сглаживание шрифтов; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f3257-117">**true** to allow font smoothing; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f3257-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3257-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3257-121">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f3257-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f3257-122">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="f3257-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f3257-123">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3257-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3257-124">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="f3257-124">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-125">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f3257-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f3257-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-127">Сертификат, используемый для подписания RDP-файлов; обязательно только в том случае, если *хасцертификате* имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="f3257-127">The certificate used to sign the RDP files; necessarily only if *HasCertificate* is true.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-128">**колорбитдепс**</span><span class="sxs-lookup"><span data-stu-id="f3257-128">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3257-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-131">Содержит глубину цветового бита:</span><span class="sxs-lookup"><span data-stu-id="f3257-131">Contains the color bit depth:</span></span>

<dt>

<span id="4"></span>

<span data-ttu-id="f3257-132">**4** ()</span><span class="sxs-lookup"><span data-stu-id="f3257-132">**4** ()</span></span>


</dt> <dd></dd> <dt>

<span id="8"></span>

<span data-ttu-id="f3257-133">**8** ()</span><span class="sxs-lookup"><span data-stu-id="f3257-133">**8** ()</span></span>


</dt> <dd></dd> <dt>

<span id="15"></span>

<span data-ttu-id="f3257-134">**15** ()</span><span class="sxs-lookup"><span data-stu-id="f3257-134">**15** ()</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="f3257-135">**16** ()</span><span class="sxs-lookup"><span data-stu-id="f3257-135">**16** ()</span></span>


</dt> <dd></dd> <dt>

<span id="24"></span>

<span data-ttu-id="f3257-136">**24** ()</span><span class="sxs-lookup"><span data-stu-id="f3257-136">**24** ()</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="f3257-137">**32** ()</span><span class="sxs-lookup"><span data-stu-id="f3257-137">**32** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3257-138">**кустомрдпсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f3257-138">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-141">Содержит содержимое RDP-файла, соответствующего настраиваемым параметрам протокола удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="f3257-141">Contains the contents of the RDP file corresponding to the custom RDP settings.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-142">**деплойментрдпсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f3257-142">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-145">Содержит содержимое RDP-файла, соответствующего параметрам развертывания.</span><span class="sxs-lookup"><span data-stu-id="f3257-145">Contains the contents of the RDP file corresponding to the deployment settings.</span></span> <span data-ttu-id="f3257-146">Если этот параметр задан, система будет использовать этот RDP-файл и игнорировать другие параметры RDP в этом вызове.</span><span class="sxs-lookup"><span data-stu-id="f3257-146">If this parameter is set, the system will use this RDP file, and ignore the other RDP settings in this call.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-147">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f3257-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3257-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3257-150">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f3257-150">Description of the object.</span></span>

<span data-ttu-id="f3257-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3257-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3257-152">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="f3257-152">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-155">Имя фермы.</span><span class="sxs-lookup"><span data-stu-id="f3257-155">The name of the farm.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-156">**гатевайаусмоде**</span><span class="sxs-lookup"><span data-stu-id="f3257-156">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-157">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3257-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-159">Содержит режим проверки подлинности шлюза:</span><span class="sxs-lookup"><span data-stu-id="f3257-159">Contains the gateway authentication mode:</span></span>

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span data-ttu-id="f3257-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Пароль (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="f3257-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password(0)** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span data-ttu-id="f3257-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Смарт-карта (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="f3257-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard(1)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span data-ttu-id="f3257-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Разрешить пользователю выбирать (4)** (4)</span><span class="sxs-lookup"><span data-stu-id="f3257-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Allow User to Choose(4)** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3257-163">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="f3257-163">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-166">Имя шлюза.</span><span class="sxs-lookup"><span data-stu-id="f3257-166">The name of the gateway.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-167">**гатевайусаже**</span><span class="sxs-lookup"><span data-stu-id="f3257-167">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-168">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3257-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-170">Описание использования шлюза.</span><span class="sxs-lookup"><span data-stu-id="f3257-170">Describes how the gateway is used:</span></span>

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span data-ttu-id="f3257-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**Шлюз** не (0)</span><span class="sxs-lookup"><span data-stu-id="f3257-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f3257-172">Нет шлюза.</span><span class="sxs-lookup"><span data-stu-id="f3257-172">No gateway.</span></span>

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span data-ttu-id="f3257-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**Усегатевайбипасслокал** (1)</span><span class="sxs-lookup"><span data-stu-id="f3257-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f3257-174">Используйте для передачи шлюза локально.</span><span class="sxs-lookup"><span data-stu-id="f3257-174">Use gateway pass by local.</span></span>

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span data-ttu-id="f3257-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**Усегатевай** (2)</span><span class="sxs-lookup"><span data-stu-id="f3257-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f3257-176">Используйте шлюз.</span><span class="sxs-lookup"><span data-stu-id="f3257-176">Use gateway.</span></span>

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span data-ttu-id="f3257-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**Детектгатевай** (3)</span><span class="sxs-lookup"><span data-stu-id="f3257-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f3257-178">Выявление шлюза.</span><span class="sxs-lookup"><span data-stu-id="f3257-178">Detect gateway.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f3257-179">**гатевайусекачедкредс**</span><span class="sxs-lookup"><span data-stu-id="f3257-179">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3257-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-182">**значение true** , чтобы использовать одни и те же учетные данные пользователя для ШЛЮЗА служб терминалов и сервера TS, когда это возможно; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f3257-182">**true** to use the same user credentials for TS gateway and TS server when possible; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-183">**хасцертификате**</span><span class="sxs-lookup"><span data-stu-id="f3257-183">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-184">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3257-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-186">**значение true** , чтобы использовать сертификат для ПОДписывания RDP-файлов; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f3257-186">**true** to use a certificate to sign the RDP files; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-187">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3257-187">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-188">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3257-188">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3257-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3257-190">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="f3257-190">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f3257-191">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="f3257-191">The date the object was installed.</span></span> <span data-ttu-id="f3257-192">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="f3257-192">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f3257-193">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3257-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3257-194">**Name**</span><span class="sxs-lookup"><span data-stu-id="f3257-194">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3257-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3257-197">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="f3257-197">The name of the object.</span></span>

<span data-ttu-id="f3257-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3257-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3257-199">**порт**.</span><span class="sxs-lookup"><span data-stu-id="f3257-199">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-200">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3257-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-201">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-202">Порт RDP.</span><span class="sxs-lookup"><span data-stu-id="f3257-202">The RDP port.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-203">**публишингфарм**</span><span class="sxs-lookup"><span data-stu-id="f3257-203">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3257-206">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3257-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3257-207">Псевдоним фермы, которая опубликовала приложение.</span><span class="sxs-lookup"><span data-stu-id="f3257-207">The alias of the farm that published the application.</span></span>

</dd> <dt>

<span data-ttu-id="f3257-208">**редиректионоптионс**</span><span class="sxs-lookup"><span data-stu-id="f3257-208">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-209">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3257-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-210">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-211">Параметры перенаправления:</span><span class="sxs-lookup"><span data-stu-id="f3257-211">Redirection Options:</span></span>

<dt>

<span data-ttu-id="f3257-212">0</span><span class="sxs-lookup"><span data-stu-id="f3257-212">0</span></span>
</dt> <dd>

<span data-ttu-id="f3257-213">None</span><span class="sxs-lookup"><span data-stu-id="f3257-213">None</span></span>

</dd> <dt>

<span data-ttu-id="f3257-214">1</span><span class="sxs-lookup"><span data-stu-id="f3257-214">1</span></span>
</dt> <dd>

<span data-ttu-id="f3257-215">Диски</span><span class="sxs-lookup"><span data-stu-id="f3257-215">Drives</span></span>

</dd> <dt>

<span data-ttu-id="f3257-216">2</span><span class="sxs-lookup"><span data-stu-id="f3257-216">2</span></span>
</dt> <dd>

<span data-ttu-id="f3257-217">принтеры;</span><span class="sxs-lookup"><span data-stu-id="f3257-217">Printers</span></span>

</dd> <dt>

<span data-ttu-id="f3257-218">4</span><span class="sxs-lookup"><span data-stu-id="f3257-218">4</span></span>
</dt> <dd>

<span data-ttu-id="f3257-219">Буфер обмена</span><span class="sxs-lookup"><span data-stu-id="f3257-219">Clipboard</span></span>

</dd> <dt>

<span data-ttu-id="f3257-220">8</span><span class="sxs-lookup"><span data-stu-id="f3257-220">8</span></span>
</dt> <dd>

<span data-ttu-id="f3257-221">Plug and Play</span><span class="sxs-lookup"><span data-stu-id="f3257-221">Plug and Play</span></span>

</dd> <dt>

<span data-ttu-id="f3257-222">16</span><span class="sxs-lookup"><span data-stu-id="f3257-222">16</span></span>
</dt> <dd>

<span data-ttu-id="f3257-223">Смарт-карта</span><span class="sxs-lookup"><span data-stu-id="f3257-223">Smart Card</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f3257-224">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f3257-224">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3257-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3257-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3257-227">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f3257-227">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f3257-228">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f3257-228">Current status of the object.</span></span> <span data-ttu-id="f3257-229">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="f3257-229">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f3257-230">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="f3257-230">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f3257-231">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="f3257-231">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f3257-232">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="f3257-232">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f3257-233">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f3257-233">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f3257-234">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3257-234">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f3257-235">("ОК")</span><span class="sxs-lookup"><span data-stu-id="f3257-235">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3257-236">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="f3257-236">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3257-237">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="f3257-237">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3257-238">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f3257-238">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3257-239">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f3257-239">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3257-240">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f3257-240">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3257-241">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="f3257-241">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f3257-242">("Служба")</span><span class="sxs-lookup"><span data-stu-id="f3257-242">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f3257-243">**усемултимон**</span><span class="sxs-lookup"><span data-stu-id="f3257-243">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3257-244">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3257-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3257-245">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3257-245">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3257-246">**значение true** , чтобы включить несколько мониторов для настольных систем (не салазок); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f3257-246">**true** to enable multi-monitor for desktop (not RAIL); otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3257-247">Требования</span><span class="sxs-lookup"><span data-stu-id="f3257-247">Requirements</span></span>



| <span data-ttu-id="f3257-248">Требование</span><span class="sxs-lookup"><span data-stu-id="f3257-248">Requirement</span></span> | <span data-ttu-id="f3257-249">Значение</span><span class="sxs-lookup"><span data-stu-id="f3257-249">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3257-250">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3257-250">Minimum supported client</span></span><br/> | <span data-ttu-id="f3257-251">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f3257-251">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f3257-252">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3257-252">Minimum supported server</span></span><br/> | <span data-ttu-id="f3257-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3257-253">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="f3257-254">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3257-254">Namespace</span></span><br/>                | <span data-ttu-id="f3257-255">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f3257-255">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f3257-256">MOF</span><span class="sxs-lookup"><span data-stu-id="f3257-256">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3257-257"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3257-257"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f3257-258">DLL</span><span class="sxs-lookup"><span data-stu-id="f3257-258">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3257-259"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3257-259"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

