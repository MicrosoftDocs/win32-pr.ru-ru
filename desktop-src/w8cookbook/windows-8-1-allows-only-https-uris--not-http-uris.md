---
title: URI в Windows 8.1
description: Windows 8.1 допускает только URI HTTPS, а не URI HTTP
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994780798bfe7ada0d7dc49794deb284e30f1605
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413502"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 допускает только URI HTTPS, а не URI HTTP

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8.1  
Серверы — Windows Server 2012 R2  
</dl>

## <a name="description"></a>Описание

Хотя приложения, созданные для Windows 8, могут включать URI HTTP и HTTPS в URI содержимого приложения, приложения, созданные для Windows 8.1, могут содержать только URI-адреса HTTPS.

Единственным исключением является динамическое Контентурирулес, указанное в файле AppxManifest.xml приложения. Благодаря динамическому Контентурирулес приложения могут обращаться к дополнительным доменам или сетевым ресурсам, предоставляемым администратором, например групповая политика URI. Однако динамические Контентурирулес доступны только для приложений Магазина Windows, если они отвечают следующим условиям:

-   групповая политика включен
-   Пакет указал возможность Ентерприсеаусентикатион
-   OSMaxVersionTested пакета Windows 8.1 или больше

Новые ограничения в Windows 8.1 являются частью улучшенных ограничений безопасности для дальнейшей защиты платформы.

## <a name="manifestations"></a>Проявлениями

При запуске приложения, созданного для Windows 8 на Windows 8.1, разрешено использование URI HTTP в [аппликатионконтентурирулес](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) .

## <a name="mitigations"></a>Устранение проблем

Рекомендуется, чтобы ВВА разработчики переключились с [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) элемента управления [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) (<x-ms-WebView>). Тем не менее, если требуется поддержка Аппкаче, Индекседдб, географического расположения или программного доступа к буферу обмена, необходимо продолжить использовать <iframe> для Windows 8.1.

Продолжение использования <iframe> для удаленного содержимого потребуется новая запись в Аппликатионконтентурирулес для приложения. Приложениям с WebView требуются новые записи в Аппликатионконтентурирулес, если веб-содержимому необходимо вызвать метод Window. external. notify для создания события [скриптнотифи](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) . Если у вас нет Visual Studio, вы можете обновить манифест приложения, добавив следующий код XML, включая подстановочные знаки для поддоменов (например, https:// \* . Microsoft.com):


```
<Package>
    …
    <Applications>
        <Application>
            …
            <ApplicationContentUriRules>
                <Rule Match="https://www.example.com" Type="include"/>
            </ApplicationContentUriRules>
        </Application>
    </Applications>
</Package>
```



## <a name="resources"></a>Ресурсы

-   [ApplicationContentUriRules](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules)
-   [<iframe>\| <iframe> объект element](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx)
-   [Класс WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)
-   [WebView. Скриптнотифи, событие](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041)

 

 