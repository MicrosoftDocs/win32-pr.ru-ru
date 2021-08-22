---
title: упаковка, развертывание и запрос приложений Windows
description: программное создание пакетов приложений для Windows приложений, установка, обновление, запрос и удаление пакетов приложений.
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca79d235aa8d0d69c887eb67704d30137cf36a7583471f28269ac939a26b2a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814277"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a>упаковка, развертывание и запрос приложений Windows

развертывание, администрирование и обслуживание Windows приложений (включая увпс и классические приложения) с помощью пакетов приложений msix/. appx на основе формата OPC. Каждый пакет приложения содержит файлы, составляющие приложение, и файл манифеста, описывающий программное обеспечение для Windows.

## <a name="introduction"></a>Введение

Как правило, разработчики создают и подписывают пакеты приложений с помощью Visual Studio. Дополнительные сведения см. в статье [Упаковка приложения UWP с помощью Visual Studio](/windows/msix/package/packaging-uwp-apps).

Microsoft Store позволяет легко создавать, отправлять и продавать приложения клиентам по всему миру. Дополнительные сведения см. в разделе [Отправка приложений](/windows/uwp/publish/app-submissions).

командлеты Windows PowerShell позволяют устанавливать бизнес-Windows приложения и управлять ими без использования магазина. Дополнительные сведения см. в разделе [командлеты модуля appx](/powershell/module/appx/index?view=win10-ps).

С помощью API упаковки, развертывания и запросов можно программно выполнять следующие задачи:

-   создание пакета приложения для Windows приложения
-   развертывание упакованного Windows приложения
-   Перечисление пакетов приложений, установленных в системе, и получение сведений о них из манифеста
-   Использование содержимого пакета приложения

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                                                                    | Описание                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Создание пакета приложения (C++)](how-to-create-a-package.md)                                        | Узнайте, как создать пакет приложения с помощью API упаковки.                                                                                                                           |
| [Создание сертификата для подписи пакета приложения](how-to-create-a-package-signing-certificate.md)      | Узнайте, как использовать [**MakeCert**](/windows-hardware/drivers/devtest/makecert) и [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) для создания тестового сертификата подписи кода, чтобы можно было подписать пакеты приложений. |
| [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Подписывание пакета приложения с помощью SignTool)                    | Узнайте, как подписывать пакеты приложений с помощью средства [**SignTool**](/windows-hardware/drivers/devtest/signtool) , чтобы их можно было развернуть.                                                                    |
| [Устранение ошибок подписи пакета приложения](how-to-troubleshoot-app-package-signature-errors.md) | Сбой развертывания приложения может быть вызван сбоем при проверке цифровой подписи пакета приложения. Узнайте, как распознать эти сбои и что делать с ними.          |
| [Как программно подписать пакет приложения (C++)](how-to-programmatically-sign-a-package.md)          | Узнайте, как подписать пакет приложения с помощью функции [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .                                                                                   |
| [Разработка приложения OEM, использующего пользовательский файл](how-to-develop-oem-app-with-custom-file.md)         | Узнайте, как разработать приложение, использующее пользовательский файл для передачи сведений от изготовителя оборудования в приложение.                                                                                             |
| [Извлечение содержимого пакета приложения (C++)](how-to-extract-content-from-a-package.md)                          | Узнайте, как извлечь файлы из пакета приложения с помощью API упаковки.                                                                                                               |
| [Сведения о манифесте пакета приложения запроса (C++)](how-to-query-package-identity-information.md)                   | Узнайте, как получить сведения из манифеста пакета приложения с помощью API упаковки.                                                                                                            |
| [Устранение неполадок](troubleshooting.md)                                                                   | Предоставляет сведения, помогающие устранять проблемы, возникающие при упаковке, развертывании или выполнении запросов к пакету приложения.                                                                 |
| [Справочник по API упаковки](interfaces.md)                                                                | API упаковки создает, считывает и записывает пакеты приложений.                                                                                                                            |
| [Справочник по API развертывания](package-deployment-api.md)                                                   | API развертывания устанавливает, обновляет и удаляет пакеты приложений.                                                                                                                    |
| [Справочник по API запроса](functions.md)                                                                     | API запросов получает сведения о пакетах приложений, установленных в системе.                                                                                                               |
| [Средства и командлеты PowerShell](appx-packaging-tools.md)                                                 | Используйте эти средства и командлеты для создания, установки пакетов приложений и управления ими.                                                                                                              |
| [Примеры SDK](appx-packaging-samples.md)                                                                | загрузите примеры SDK, демонстрирующие интерфейсы api упаковки, развертывания и запросов для Windows приложений.                                                                               |
| [Словарь терминов](appx-packaging-glossary.md)                                                                  | сведения о терминах, связанных с упаковкой, развертыванием и запросом Windows приложений.                                                                                              |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Основные понятия**
</dt> <dt>

[Пакеты и развертывание приложений](/previous-versions/windows/apps/hh464929(v=win.10))
</dt> <dt>

**Другая ссылка**
</dt> <dt>

[Схема манифеста пакета приложений](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[**Windows. ApplicationModel. Package**](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[**Windows. ApplicationModel. PackageId**](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[**Windows.Management.Deployment.PackageManager**](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[**Windows.Management.Deployment.PackageUserInformation**](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 