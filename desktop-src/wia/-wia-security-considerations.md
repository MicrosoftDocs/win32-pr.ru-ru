---
description: В этом документе содержатся сведения о вопросах безопасности, связанных с получением образа Windows (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Вопросы безопасности: получение образа Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711089"
---
# <a name="security-considerations-windows-image-acquisition"></a>Вопросы безопасности: получение образа Windows

В этом документе содержатся сведения о вопросах безопасности, связанных с получением образа Windows (WIA). Этот документ не предоставляет все, что нужно знать о проблемах безопасности. вместо этого используйте его в качестве отправной точки и справочной информации для этой области технологий.

-   [Используйте кавычки вокруг имен путей](#use-quotation-marks-around-path-names)
-   [Размещение зарегистрированных приложений в защищенных расположениях](#place-registered-applications-in-secure-locations)
-   [Не используйте базовые каталоги или разделы реестра](#do-not-use-underlying-directories-or-registry-keys)
-   [См. также](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Используйте кавычки вокруг имен путей

При использовании [**ивиадевмгр:: регистеревенткаллбаккпрограм**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) для регистрации приложения для получения событий устройства обязательно заключите путь и имя файла приложения в кавычки. Это позволяет избежать неправильной интерпретации пути и запуска неавторизованного приложения.

## <a name="place-registered-applications-in-secure-locations"></a>Размещение зарегистрированных приложений в защищенных расположениях

Когда приложение регистрируется для получения события устройства, оно может быть запущено любым пользователем, имеющим доступ к этому устройству. Например, если приложение зарегистрировано для события сканирования, нажатие кнопки "Сканировать" на сканере приведет к запуску этого приложения. Если приложение работает с более высокой привилегией, чем у пользователя, это вызывает потенциальную угрозу безопасности.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>Не используйте базовые каталоги или разделы реестра

Для хранения данных или информации WIA использует несколько каталогов и разделов реестра. Не изменяйте доступ к этим каталогам или разделам реестра напрямую. Вместо этого используйте предоставляемые методы интерфейса, чтобы указать каталоги для полученных изображений.

## <a name="related-topics"></a>См. также

-   [Microsoft Security](https://www.microsoft.com/security/)
-   [Домашняя страница безопасности библиотеки MSDN](https://msdn.microsoft.com/security/default.aspx)
-   [Материалы по безопасности](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Материалы по безопасности TechNet](https://technet.microsoft.com/security/default.aspx)
-   [Вопросы безопасности для разработчиков Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Рекомендации по обеспечению безопасности](../secbp/best-practices-for-the-security-apis.md)

 

 
