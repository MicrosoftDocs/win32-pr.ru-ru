---
title: Общие сведения о пользователях пакета SDK Windows Media Format
description: Общие сведения о пользователях пакета SDK Windows Media Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows Media Format SDK, расширенные API клиента DRM
- Пакет SDK для Windows Media Format, расширенные API клиента
- Windows Media Format SDK, расширенные API
- Windows Media Format SDK, API
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Управление цифровыми правами (DRM), расширенные API клиента
- DRM (Управление цифровыми правами), расширенные API клиента
- Управление цифровыми правами (DRM), расширенные API
- DRM (Управление цифровыми правами), расширенные API
- Управление цифровыми правами (DRM), API
- DRM (Управление цифровыми правами), API
- Расширенные API клиента DRM, о
- Расширенные API клиента, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410995"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Общие сведения о пользователях пакета SDK Windows Media Format

Большая часть функциональных возможностей, обеспечиваемых расширенными API клиента DRM Windows Media, аналогична функциональным возможностям, предоставляемым объектами пакета SDK Windows Media Format. Пакет Windows Media Format SDK предоставляет разработчикам объекты, необходимые для создания, доступа и управления файлами мультимедиа, использующими структуру файлов ASF. Так как Windows Media DRM предназначена для защиты файлов ASF, клиентские функции DRM были добавлены в пакет SDK Windows Media Format.

Расширенные API клиента Windows Media DRM выпускаются совместно с платформой цифрового мультимедиа следующего поколения Майкрософт, Microsoft Media Foundationным пакетом SDK. Media Foundation будет включать функции ASF, которые перекрывают некоторые функции пакета SDK Windows Media Format. Поскольку теперь существуют два пакета Microsoft SDK для работы с файлами ASF, функциональность DRM на стороне клиента отделяется от Windows Media Format SDK до расширенных API клиента DRM Windows Media. Доступ к этим API можно получить у пользователей Windows Media Format SDK и Media Foundation SDK. В настоящее время эти API-интерфейсы входят в состав установочного пакета пакета SDK Windows Media Format и задокументированы в пакете Windows Media Format SDK. Однако расширенные API клиента DRM Windows Media реализуются в собственной библиотеке и имеют собственный файл заголовка. После установки пакета SDK для формата Windows Media эти API можно использовать самостоятельно, не включая заголовки или библиотеки пакета SDK Windows Media Format в приложение.

При разработке приложений, использующих пакет SDK для формата Windows Media, необходимо решить, использовать ли функциональные возможности DRM, предоставляемые пакетом SDK, или использовать расширенные API клиента DRM Windows Media. Хотя многие функции этих двух пакетов SDK очень похожи, расширенные API клиента DRM Windows Media предлагают следующие функции, недоступные пользователям старых подпрограмм DRM:

-   Возможность импортировать содержимое, защищенное сторонней системой управления правами.
-   Возможность экспорта содержимого, защищенного Windows Media DRM, в систему управления правами сторонних производителей.
-   Прямое перечисление лицензий в хранилище лицензий.
-   Простой запрос агрегированных прав на основе идентификатора ключа (нет необходимости загружать файл мультимедиа).
-   Возможность продлить отозванные компоненты с помощью стандартного интерфейса Media Foundation **имфконтентенаблер**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**О расширенных API-интерфейсах клиента DRM Windows Media**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




