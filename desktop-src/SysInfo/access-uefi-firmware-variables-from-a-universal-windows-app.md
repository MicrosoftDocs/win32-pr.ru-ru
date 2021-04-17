---
description: Как получить доступ к переменным встроенного по Единый интерфейс EFI (UEFI) из универсального приложения Windows.
ms.assetid: 4131CCED-3B76-4569-B0A7-111E4E9215EF
title: Доступ к переменным встроенного по UEFI из универсального приложения Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738b7042b4c650c74115760e6dcd2e93131d6780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663502"
---
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a><span data-ttu-id="022b4-103">Доступ к переменным встроенного по UEFI из универсального приложения Windows</span><span class="sxs-lookup"><span data-stu-id="022b4-103">Access UEFI firmware variables from a Universal Windows App</span></span>

<span data-ttu-id="022b4-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="022b4-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="022b4-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="022b4-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="022b4-106">Как получить доступ к переменным встроенного по Единый интерфейс EFI (UEFI) из универсального приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="022b4-106">How to access Unified Extensible Firmware Interface (UEFI) firmware variables from a Universal Windows app.</span></span>

<span data-ttu-id="022b4-107">Начиная с Windows 10 версии 1803, универсальные приложения для Windows могут использовать [**жетфирмваринвиронментвариабле**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) и [**сетфирмваринвиронментвариабле**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (и их варианты "ex") для доступа к переменным встроенного по UEFI, выполняя следующие действия.</span><span class="sxs-lookup"><span data-stu-id="022b4-107">Starting with Windows 10, version 1803, Universal Windows apps can use [**GetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) and [**SetFirmwareEnvironmentVariable**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (and their 'ex' variants) to access UEFI firmware variables by doing the following:</span></span>

-   <span data-ttu-id="022b4-108">Объявите пользовательскую возможность **Microsoft. фирмваререад \_ cw5n1h2txyewy** в манифесте для чтения переменной встроенного по и/или возможности **Microsoft. фирмвареврите \_ cw5n1h2txyewy** для записи переменной встроенного по.</span><span class="sxs-lookup"><span data-stu-id="022b4-108">Declare the **Microsoft.firmwareRead\_cw5n1h2txyewy** custom capability in the manifest to read a firmware variable, and/or the **Microsoft.firmwareWrite\_cw5n1h2txyewy** capability to write a firmware variable.</span></span>
-   <span data-ttu-id="022b4-109">Также объявите возможность ограничения **протектедапп** в манифесте приложения.</span><span class="sxs-lookup"><span data-stu-id="022b4-109">Also declare the **protectedApp** restricted capability in the app manifest.</span></span>
-   <span data-ttu-id="022b4-110">Например, следующие дополнения манифеста приложения позволяют универсальному приложению Windows считывать переменные встроенного по:</span><span class="sxs-lookup"><span data-stu-id="022b4-110">For example, the following app manifest additions allow the Universal Windows app to read firmware variables:</span></span>

    ``` syntax
    <Package
      ...
      xmlns:uap4=http://schemas.microsoft.com/appx/manifest/uap/windows10/4
      xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities"
      IgnorableNamespaces="uap mp uap4 rescap">  
      ...
      <Capabilities>
        <rescap:Capability Name="protectedApp"/>
        <uap4:CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy" />
      </Capabilities>
    </Package>
    ```

<!-- -->

-   <span data-ttu-id="022b4-111">Перед отправкой приложения в Microsoft Store задайте параметр компоновщика **/INTEGRITYCHECK** для всех конфигураций проекта.</span><span class="sxs-lookup"><span data-stu-id="022b4-111">Set the linker option **/INTEGRITYCHECK**, for all project configurations, before submitting the app to the Microsoft Store.</span></span> <span data-ttu-id="022b4-112">Это гарантирует, что приложение будет запущено в качестве защищенного приложения.</span><span class="sxs-lookup"><span data-stu-id="022b4-112">This ensures that the app will be launched as a protected app.</span></span> <span data-ttu-id="022b4-113">Дополнительные сведения см. в разделе [/INTEGRITYCHECK (требовать проверку подписи)](/cpp/build/reference/integritycheck-require-signature-check) .</span><span class="sxs-lookup"><span data-stu-id="022b4-113">See [/INTEGRITYCHECK (Require Signature Check)](/cpp/build/reference/integritycheck-require-signature-check) for details.</span></span>
-   <span data-ttu-id="022b4-114">Получите [подписанный файл пользовательского дескриптора возможностей](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (сккд) от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="022b4-114">Obtain a [Signed Custom Capability Descriptor](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (SCCD) file from Microsoft.</span></span> <span data-ttu-id="022b4-115">См. статью [Создание пользовательской возможности для связывания драйвера с приложением поддержки оборудования (хса)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) и [Использование пользовательской возможности для связывания приложения поддержки оборудования (хса) с драйвером](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) для получения сведений о том, как получить подписанный файл сккд от Майкрософт, как упаковать его в приложение и как включить режим разработчика.</span><span class="sxs-lookup"><span data-stu-id="022b4-115">See [Creating a custom capability to pair a driver with a Hardware Support App (HSA)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) and [Using a custom capability to pair a Hardware Support App (HSA) with a driver](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) for information about how to obtain signed SCCD file from Microsoft, how to package it with your app, and how to enable developer mode.</span></span> <span data-ttu-id="022b4-116">Ниже приведен пример файла ССКД из [примера кустомкапабилити](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span><span class="sxs-lookup"><span data-stu-id="022b4-116">Here is an example SSCD file from the [CustomCapability sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):</span></span>
    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <CustomCapabilityDescriptor xmlns="http://schemas.microsoft.com/appx/2016/sccd" xmlns:s="http://schemas.microsoft.com/appx/2016/sccd">
      <CustomCapabilities>
        <CustomCapability Name="microsoft.hsaTestCustomCapability_q536wpkpf5cy2"></CustomCapability>
        <CustomCapability Name="microsoft.firmwareRead_cw5n1h2txyewy"></CustomCapability>
      </CustomCapabilities>
      <AuthorizedEntities>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="ca9fc964db7e0c2938778f4559946833e7a8cfde0f3eaa07650766d4764e86c4"></AuthorizedEntity>
        <AuthorizedEntity AppPackageFamilyName="Microsoft.SDKSamples.CustomCapability.CPP_8wekyb3d8bbwe" CertificateSignatureHash="279cd652c4e252bfbe5217ac722205d7729ba409148cfa9e6d9e5b1cb94eaff1"></AuthorizedEntity>
      </AuthorizedEntities>
      <Catalog>xxxx</Catalog>
    </CustomCapabilityDescriptor>
    ```

    

-   <span data-ttu-id="022b4-117">Отправьте приложение на Microsoft Store, чтобы получить подпись.</span><span class="sxs-lookup"><span data-stu-id="022b4-117">Submit the app to the Microsoft Store to get it signed.</span></span> <span data-ttu-id="022b4-118">В целях разработки можно пропустить подпись, включив тестовый вход в базу данных конфигурации загрузки (BCD).</span><span class="sxs-lookup"><span data-stu-id="022b4-118">For development purposes, you can skip signing by enabling test-signing in the boot configuration database (bcd).</span></span> <span data-ttu-id="022b4-119">Дополнительные сведения см. в описании [параметра конфигурации Тестсигнинг Boot](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .</span><span class="sxs-lookup"><span data-stu-id="022b4-119">See [The TESTSIGNING Boot Configuration Option](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) for details.</span></span>

## <a name="related-topics"></a><span data-ttu-id="022b4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="022b4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="022b4-121">Особые и ограниченные возможности</span><span class="sxs-lookup"><span data-stu-id="022b4-121">Special and restricted capabilities</span></span>](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[<span data-ttu-id="022b4-122">**жетфирмваринвиронментвариабле**</span><span class="sxs-lookup"><span data-stu-id="022b4-122">**GetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="022b4-123">**жетфирмваринвиронментвариабликс**</span><span class="sxs-lookup"><span data-stu-id="022b4-123">**GetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="022b4-124">**сетфирмваринвиронментвариабле**</span><span class="sxs-lookup"><span data-stu-id="022b4-124">**SetFirmwareEnvironmentVariable**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[<span data-ttu-id="022b4-125">**сетфирмваринвиронментвариабликс**</span><span class="sxs-lookup"><span data-stu-id="022b4-125">**SetFirmwareEnvironmentVariableEx**</span></span>](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[<span data-ttu-id="022b4-126">Доступ к сведениям SMBIOS из универсального приложения Windows</span><span class="sxs-lookup"><span data-stu-id="022b4-126">Access SMBIOS information from a Universal Windows App</span></span>](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
