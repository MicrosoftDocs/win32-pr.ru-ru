---
description: В этом примере показано, как создать установку пакета установщик Windows на основе URL-адреса.
ms.assetid: a38a1132-43b4-449d-b134-f351ce370223
title: Пример установки с применением установщика на базе URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a210eb1b93202930309223b49c737aa85b1812
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "105651533"
---
# <a name="a-url-based-windows-installer-installation-example"></a>Пример установки с применением установщика на базе URL

В этом примере показано, как создать установку пакета установщик Windows на основе URL-адреса. Дополнительные сведения о защите установки и использовании цифровых сертификатов см. в разделе [рекомендации по созданию безопасных установок](guidelines-for-authoring-secure-installations.md) и [цифровых подписей и установщик Windows](digital-signatures-and-windows-installer.md).

Для воспроизведения этого примера требуется программа [SignTool](../seccrypto/signtool.md) . Дополнительные сведения см. в [справочнике по инструментам CryptoAPI](../seccrypto/cryptoapi-tools-reference.md) в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows. [Для установщик Windows разработчиков](platform-sdk-components-for-windows-installer-developers.md)также требуются [Msistuff.exe](msistuff-exe.md) и Setup.exe служебные программы из Windows SDK компонентов. Дополнительные сведения см. в разделе [начальная загрузка Интернета](internet-download-bootstrapping.md).

Пример имеет следующие характеристики:

-   Когда пользователи посещают веб-сайт и щелкают ссылку "MySetup установка", они представляются с возможностью сохранения или запуска из этого расположения. Если пользователь выбирает Запуск из этого расположения, Setup.exe обновляет версию установщик Windows на компьютере, при необходимости проверяет цифровую подпись в пакете установщика и устанавливает пакет на своем компьютере.
-   Существует цифровой сертификат MyCert. cer, поставляемый с закрытым ключом MyCert. PVK.
-   URL-адрес гипотетического веб-сайта, который клиент будет посещать для установки пакета — HTTPS: \/ /www.blueyonderairlines.com/Products/MySetup/mysetup.html.
-   Макет веб-сервера выглядит следующим образом. 

    | URL-адрес                                                               | Файл        | Описание                                    |
    |-------------------------------------------------------------------|-------------|------------------------------------------------|
    | HTTPS: \/ /www.blueyonderairlines.com/products/MySetup/               | Setup.exe   | Загрузчик Setup.exe.                        |
    | HTTPS: \/ /www.blueyonderairlines.com/products/MySetup/               | MySetup.msi | Пакет установки                           |
    | HTTPS: \/ /www.blueyonderairlines.com/products/MySetup/               | Cab1.cab    | CAB-файл исходного файла \# 1                        |
    | HTTPS: \/ /www.blueyonderairlines.com/products/MySetup/               | Cab2.cab    | CAB-файл исходного файла \# 2                        |
    | HTTPS: \/ /www.blueyonderairlines.com/products/Common/InstMsi/ANSI    | Instmsi.exe | Распространяемый пакет ANSI установщик Windows 2,0.    |
    | HTTPS: \/ /www.blueyonderairlines.com/products/Common/InstMsi/Unicode | Instmsi.exe | Распространяемый компонент Unicode установщик Windows 2,0. |

    

     

[Продолжить](configuring-the-setup-exe-resources.md)

 

 
