---
description: в этом разделе приведены рекомендации по выполнению асинхронных операций агента Центр обновления Windows (WUA).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Рекомендации по асинхронным операциям WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24801c7639e75f34f1517ee626ff7acb7c1d13f85a6ebf57e7d824f7f0d3191d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049492"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Рекомендации по асинхронным операциям WUA

в этом разделе приведены рекомендации по выполнению асинхронных операций агента Центр обновления Windows (WUA).

-   Асинхронные операции WUA не гарантируют определенную скорость выполнения. Время завершения асинхронной операции WUA может сильно различаться в зависимости от оборудования компьютера, версии операционной системы и конфигурации сети. как и в случае с другими Windows api, которые имеют сетевые зависимости и не содержат параметр времени ожидания или задокументированное время ожидания, рекомендуется реализовать собственные механизмы времени ожидания, если требуется гарантированное время ответа. Например, можно создать рабочий поток, вызывающий асинхронный метод WUA и задающий событие или другой объект синхронизации по завершении асинхронной операции WUA. Затем главный поток может использовать функцию [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) или [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) , которая позволяет указать значение времени ожидания.
-   При завершении поиска, скачивания, установки или удаления обновлений можно использовать [**иупдатесеарчер:: ендсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**Иупдатедовлоадер:: метод**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**Иупдатеинсталлер:: Ендинсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) и [**иупдатеинсталлер:: EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) из любого потока.
-   При запуске поиска, скачивания, установки или удаления обновлений с помощью [**иупдатесеарчер:: бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**Иупдатедовнлоадер:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**Иупдатеинсталлер:: Бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)и [**иупдатеинсталлер:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)убедитесь, что при освобождении ссылок на объекты API WUA вы сохраняете достаточно прав доступа разрешения.
    -   Убедитесь, что все объекты обратного вызова, используемые в асинхронной операции, не ссылаются до их уничтожения. Подождите, пока счетчик ссылок объекта обратного вызова вернется к начальному значению перед уничтожением.
    -   Ссылка на объект задания, возвращаемый из соответствующего метода **Begin** , должна управляться объектом, который отличается от объектов обратного вызова. Используйте объект, отличающийся от объектов обратного вызова, чтобы избежать циклических ссылок.
    -   При попытке управления ссылкой на объект задания с помощью объекта обратного вызова необходимо вызвать метод [**идовнлоаджоб:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**Иинсталлатионжоб:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)или [**исеарчжоб:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) вне функции обратного вызова, чтобы отключить объект задания от объекта обратного вызова. Это необходимо сделать перед тем, как освободить ссылку на объект задания, возвращаемый методом **Begin** .
-   Убедитесь, что асинхронные операции WUA завершены. Windows Сервер скриптов может завершить выполнение скрипта при завершении всех команд за пределами функции, даже если в API-интерфейсе WUA имеются ссылки на объект обратного вызова.
    -   Используйте один из методов **очистки** или задайте для функции обратного вызова общую глобальную переменную после завершения.
    -   Никогда не вызывайте [**идовнлоаджоб:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**Иинсталлатионжоб:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)или [**исеарчжоб:: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) в объекте задания в своей функции обратного вызова.
    -   чтобы обеспечить правильную последовательность очистки в скрипте, который выполняется в Windows Internet Explorer, вызовите метод **CleanUp** для всех объектов задания при обработке window. онбефореунлоад.
-   Не используйте определяемые пользователем типы данных (UDT) для асинхронных операций WUA. Тип не поддерживается [**иупдатесеарчер:: бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**Иупдатедовнлоадер:: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**Иупдатеинсталлер:: Бегининсталл**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)или [**иупдатеинсталлер:: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall).

 

 
