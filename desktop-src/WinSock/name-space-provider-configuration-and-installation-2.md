---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Конфигурация и установка поставщика пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c87de8fee4ccaea0fb6978037e1e41684b56267
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541546"
---
# <a name="namespace-provider-configuration-and-installation"></a>Конфигурация и установка поставщика пространства имен

-   [**всценабленспровидер**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider)
-   [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32)
-   [**всЦинсталлнамеспаце**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace)
-   [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32)
-   [**всЦинсталлнамеспацеекс**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex)
-   [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)
-   [**вскунинсталлнамеспаце**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)
-   [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32)
-   [**всквритенамеспацеордер**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder)
-   [**WSCWriteNameSpaceOrder32**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder32)

Как упоминалось ранее, приложение установки для поставщика пространства имен должно вызывать [**всЦинсталлнамеспаце**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) или [**всЦинсталлнамеспацеекс**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) для регистрации в Ws2 \_32.dll и предоставления статических сведений о конфигурации. Чтобы установить в 32-разрядный каталог на 64-разрядной платформе, поставщик пространства имен должен вызвать [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) или [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32). 32.dll Ws2 \_ использует эти сведения для выполнения своей функции маршрутизации и в реализации [**Всаенумнамеспацепровидерс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) и [**всаенумнамеспацепровидерсекс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa). Функция [**вскунинсталлнамеспаце**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) используется для удаления поставщика пространства имен из реестра, а функция [**всценабленспровидер**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) используется для переключения поставщика между активным и неактивным состояниями.

На 64-разрядной платформе [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) и [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) — аналогичные функции для работы с 32-битным каталогом.

Результаты этих трех операций невидимы для приложений, которые в настоящее время загружены и выполняются. Только приложения, которые начинают выполняться после возникновения этих операций, будут затронуты этими операциями.

Эта архитектура явным образом поддерживает создание экземпляров нескольких поставщиков пространств имен в одной библиотеке DLL, однако каждый такой поставщик должен иметь выделенный уникальный идентификатор поставщика пространства имен (GUID) и отдельный вызов [**всЦинсталлнамеспаце**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) или [**всЦинсталлнамеспацеекс**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) для каждого экземпляра (на 64-разрядных платформах функции для 32-разрядного каталога — [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) и [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)). Такой поставщик может определить, какой экземпляр вызывается, так как идентификатор поставщика пространства имен (NSP) отображается как параметр в каждой функции NSP.

 

 



