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
# <a name="access-uefi-firmware-variables-from-a-universal-windows-app"></a>Доступ к переменным встроенного по UEFI из универсального приложения Windows

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Как получить доступ к переменным встроенного по Единый интерфейс EFI (UEFI) из универсального приложения Windows.

Начиная с Windows 10 версии 1803, универсальные приложения для Windows могут использовать [**жетфирмваринвиронментвариабле**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea) и [**сетфирмваринвиронментвариабле**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea) (и их варианты "ex") для доступа к переменным встроенного по UEFI, выполняя следующие действия.

-   Объявите пользовательскую возможность **Microsoft. фирмваререад \_ cw5n1h2txyewy** в манифесте для чтения переменной встроенного по и/или возможности **Microsoft. фирмвареврите \_ cw5n1h2txyewy** для записи переменной встроенного по.
-   Также объявите возможность ограничения **протектедапп** в манифесте приложения.
-   Например, следующие дополнения манифеста приложения позволяют универсальному приложению Windows считывать переменные встроенного по:

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

-   Перед отправкой приложения в Microsoft Store задайте параметр компоновщика **/INTEGRITYCHECK** для всех конфигураций проекта. Это гарантирует, что приложение будет запущено в качестве защищенного приложения. Дополнительные сведения см. в разделе [/INTEGRITYCHECK (требовать проверку подписи)](/cpp/build/reference/integritycheck-require-signature-check) .
-   Получите [подписанный файл пользовательского дескриптора возможностей](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa#preparing-the-signed-custom-capability-descriptor-sccd-file) (сккд) от корпорации Майкрософт. См. статью [Создание пользовательской возможности для связывания драйвера с приложением поддержки оборудования (хса)](/windows-hardware/drivers/devapps/creating-a-custom-capability-to-pair-driver-with-hsa) и [Использование пользовательской возможности для связывания приложения поддержки оборудования (хса) с драйвером](/windows-hardware/drivers/devapps/using-a-custom-capability-to-pair-hsa-with-driver) для получения сведений о том, как получить подписанный файл сккд от Майкрософт, как упаковать его в приложение и как включить режим разработчика. Ниже приведен пример файла ССКД из [примера кустомкапабилити](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/CustomCapability):
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

    

-   Отправьте приложение на Microsoft Store, чтобы получить подпись. В целях разработки можно пропустить подпись, включив тестовый вход в базу данных конфигурации загрузки (BCD). Дополнительные сведения см. в описании [параметра конфигурации Тестсигнинг Boot](/windows-hardware/drivers/install/the-testsigning-boot-configuration-option) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Особые и ограниченные возможности](/windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities)
</dt> <dt>

[**жетфирмваринвиронментвариабле**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariablea)
</dt> <dt>

[**жетфирмваринвиронментвариабликс**](/windows/desktop/api/Winbase/nf-winbase-getfirmwareenvironmentvariableexa)
</dt> <dt>

[**сетфирмваринвиронментвариабле**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariablea)
</dt> <dt>

[**сетфирмваринвиронментвариабликс**](/windows/desktop/api/Winbase/nf-winbase-setfirmwareenvironmentvariableexa)
</dt> <dt>

[Доступ к сведениям SMBIOS из универсального приложения Windows](access-smbios-information-from-a-universal-windows-app.md)
</dt> </dl>

 

 
