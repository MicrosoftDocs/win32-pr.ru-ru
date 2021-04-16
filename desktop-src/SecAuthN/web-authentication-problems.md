---
description: В этом разделе описаны рекомендации по устранению неполадок при использовании API посредника веб-проверки подлинности для веб-страниц.
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Неполадки при веб-аутентификации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569907"
---
# <a name="web-authentication-problems"></a>Неполадки при веб-аутентификации

В этом разделе описаны рекомендации по устранению неполадок при использовании API посредника веб-проверки подлинности для веб-страниц.

-   [Операционные журналы](#operational-logs)
-   [Использование Fiddler с брокером веб-проверки подлинности](#using-fiddler-with-web-authentication-broker)
-   [См. также](#related-topics)

## <a name="operational-logs"></a>Операционные журналы

Нередко определить, что именно не работает, помогают операционные журналы. Существует выделенный канал журнала событий Microsoft-Windows- \\ Web AUTH, позволяющий разработчикам веб-сайтов понять, как веб-страницы обрабатываются брокером веб-проверки подлинности. Чтобы включить его, запустите eventvwr.exe и включите операционный журнал в приложении и службах \\ Microsoft \\ Windows веб \\ AUTH. Кроме того, брокер веб-проверки подлинности добавляет в строку агента пользователя уникальную строку для идентификации себя на веб-сервере. Это строка "MSAuthHost/1.0". Обратите внимание, что номер версии в дальнейшем может меняться, поэтому ваш код не должен зависеть от номера версии. Ниже приведен пример полной строки агента пользователя.

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

Пример использования операционных журналов

1.  Включить Операционные журналы
2.  Запуск приложения Contoso Social![Средство просмотра событий, отображающее операционные журналы WebAuth](images/wab-figure15.png)
3.  Созданные записи журналов можно использовать для более подробного понимания поведения брокера веб-проверки подлинности. В нашем случае записи могут содержать следующую информацию.
    -   Навигация начата: регистрирует время запуска AuthHost и содержит сведения о URL-адресах начала и окончания навигации.
    -   ![Иллюстрация к сведениям о начале навигации](images/wab-figure16.png)
    -   Навигация выполнена: регистрирует выполнение загрузки веб-страницы.
    -   Метатег: регистрирует подробную информацию в случае обнаружения метатега.
    -   Завершение навигации: навигация завершена пользователем.
    -   Ошибка навигации: AuthHost обнаруживает ошибку навигации в URL-адресе, включая код состояния HttpStatusCode.
    -   Завершение навигации: обнаружен завершающий URL-адрес.

## <a name="using-fiddler-with-web-authentication-broker"></a>Использование Fiddler с брокером веб-проверки подлинности

Веб-отладчик Fiddler можно использовать с приложениями Windows 8.

1.  Так как AuthHost работает в собственном контейнере приложения, чтобы предоставить ему возможность частной сети, необходимо настроить раздел реестра: редактор реестра Windows версии 5.00

    **HKey \_ \_** \\  \\  \\  \\  \\ **Параметры выполнения файлов образа** Microsoft Windows NT CurrentVersion по локальному компьютеру \\ **authhost.exe** \\ **енаблеприватенетворк** = 00000001<dl> <dt>

                     Data type
</dt> <dd>                     DWORD</dd> </dl>

2.  Добавьте правило для AuthHost, поскольку эта служба создает исходящий трафик.
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  Добавьте правило брандмауэра для входящего трафика в Fiddler.

Дополнительные сведения см. [в блоге использование веб-отладчика Fiddler с приложениями для Магазина Windows](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Рекомендации по разработке веб-страниц](considerations-for-the-web-page-development.md)
</dt> <dt>

[Вопросы и ответы по брокеру веб-проверки подлинности](faq-for-web-authentication-broker.md)
</dt> <dt>

[Пример приложения SDK брокера веб-проверки подлинности](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
