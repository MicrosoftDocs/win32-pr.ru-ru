---
title: URI в Windows 8.1
description: Windows 8.1 допускает только uri https, а не uri http
ms.assetid: 06BDD3A3-67B7-4085-83DA-F322F718C876
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022485f9fc5dc2657127f7bae49127e0bd3b5954
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886121"
---
# <a name="windows-81-allows-only-https-uris-not-http-uris"></a>Windows 8.1 допускает только uri https, а не uri http

## <a name="platforms"></a>Платформы

<dl> Клиенты — Windows 8.1  
серверы — Windows Server 2012 R2  
</dl>

## <a name="description"></a>Описание

хотя приложения, созданные для Windows 8, могут включать uri http и https в uri содержимого приложения, приложения, созданные для Windows 8.1, могут содержать только uri-адреса https.

Единственным исключением является динамическое Контентурирулес, указанное в файле AppxManifest.xml приложения. Благодаря динамическому Контентурирулес приложения могут обращаться к дополнительным доменам или сетевым ресурсам, предоставляемым администратором, например групповая политика URI. однако динамические контентурирулес доступны только для приложений Windows Store, если они отвечают следующим условиям:

-   групповая политика включен
-   Пакет указал возможность Ентерприсеаусентикатион
-   OSMaxVersionTested пакета Windows 8.1 или больше

новые ограничения в Windows 8.1 являются частью улучшенных ограничений безопасности для дальнейшей защиты платформы.

## <a name="manifestations"></a>Проявлениями

при запуске приложения, созданного для Windows 8 на Windows 8.1, разрешено использование uri http в [аппликатионконтентурирулес](/uwp/schemas/appxpackage/appxmanifestschema/element-applicationcontenturirules) .

## <a name="mitigations"></a>Устранение проблем

Рекомендуется, чтобы ВВА разработчики переключились с на [<iframe>](https://msdn.microsoft.com/library/windows/apps/hh465955.aspx) элемент управления [WebView](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) ( &lt; x-MS-WebView &gt; ). Тем не менее, если требуется поддержка Аппкаче, Индекседдб, географического расположения или программного доступа к буферу обмена, необходимо продолжить использовать <iframe> для Windows 8.1.

Продолжение использования <iframe> для удаленного содержимого потребуется новая запись в Аппликатионконтентурирулес для приложения. Приложениям с WebView требуются новые записи в Аппликатионконтентурирулес, если веб-содержимому необходимо вызвать метод Window. external. notify для создания события [скриптнотифи](/uwp/api/Windows.UI.Xaml.Controls.WebView?view=winrt-19041) . если у вас нет Visual Studio, можно обновить манифест приложения, добавив следующий код XML, включая подстановочные знаки для поддоменов (например, https:// \* . microsoft.com):


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

 

 
