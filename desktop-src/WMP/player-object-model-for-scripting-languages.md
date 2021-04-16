---
title: Объектная модель проигрывателя для языков сценариев
description: Объектная модель проигрывателя для языков сценариев
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Проигрыватель Windows Media, объектная модель
- Объектная модель проигрывателя Windows Media, о программе
- Объектная модель, сведения
- Элемент управления ActiveX проигрывателя Windows Media, объектная модель
- Элемент управления ActiveX, объектная модель
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, объектная модель
- Проигрыватель Windows Media Mobile, объектная модель
- пакет средств разработки программного обеспечения (SDK), объектная модель элемента управления ActiveX проигрывателя Windows Media
- Пакет SDK (пакет средств разработки программного обеспечения), объектная модель элемента управления ActiveX проигрывателя Windows Media
- Документация, объектная модель элемента управления ActiveX проигрывателя Windows Media
- Проигрыватель Windows Media, языки сценариев
- Объектная модель проигрывателя Windows Media, языки сценариев
- Объектная модель, языки сценариев
- Элемент управления ActiveX проигрывателя Windows Media, языки сценариев
- Элемент управления ActiveX, языки сценариев
- Элемент управления мобильными устройствами ActiveX проигрывателя Windows Media, языки сценариев
- Проигрыватель Windows Media Mobile, языки сценариев
- Языки сценариев
- Проигрыватель Windows Media Player, объект Player
- Объектная модель проигрывателя Windows Media, объект Player
- Объектная модель, объект Player
- Элемент управления ActiveX проигрывателя Windows Media, объект Player
- Элемент управления ActiveX, объект Player
- Элемент управления ActiveX проигрывателя Windows Media Mobile, объект Player
- Проигрыватель Windows Media Mobile, объект Player
- Объект Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561722"
---
# <a name="player-object-model-for-scripting-languages"></a>Объектная модель проигрывателя для языков сценариев

ActiveX использует концепцию объектов для хранения функциональных возможностей программирования. Проигрыватель Windows Media использует несколько объектов для разделения функциональных возможностей, предоставляемых элементом управления. Корневой объект — это объект **Player** , а другие объекты присоединяются к объекту **Player** через определенные свойства.

На следующей схеме показано, как работает объектная модель элемента управления ActiveX в проигрывателе Windows Media 11 для языков сценариев.

![Схема объектной модели проигрывателя Windows Media 11](images/playeromdiag.png)

В C++ и иногда в языках .NET объекты представлены COM-интерфейсами. В объектной модели проигрывателя Windows Media имена COM-интерфейсов совпадают с именами объектов, но начинаются с префикса "ИВМП". Например, объект **сети** предоставляется через интерфейс **ивмпнетворк** .

В следующих разделах приводятся общие обзоры для каждого объекта.

-   [Сведения об объектах CDROM и Кдромколлектион](about-the-cdrom-and-cdromcollection-objects.md)
-   [Сведения об объекте Клоседкаптион](about-the-closedcaption-object.md)
-   [Об объекте Controls](about-the-controls-object.md)
-   [Об объекте DVD](about-the-dvd-object.md)
-   [Об ошибках и объектах Ерроритем](about-the-error-and-erroritem-objects.md)
-   [Сведения об объектах Медиаколлектион и Media](about-the-mediacollection-and-media-objects.md)
-   [Сведения об объекте Метадатапиктуре](about-the-metadatapicture-object.md)
-   [Сведения об объекте Метадататекст](about-the-metadatatext-object.md)
-   [О сетевом объекте](about-the-network-object.md)
-   [Сведения об объекте Player](about-the-player-object.md)
-   [Сведения об объекте Плайераппликатион](about-the-playerapplication-object.md)
-   [Сведения об объектах списков воспроизведения, Плайлистколлектион и Плайлистаррай](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Сведения об объекте Query](about-the-query-object.md)
-   [Сведения об объекте Settings](about-the-settings-object.md)
-   [Сведения об объекте StringCollection](about-the-stringcollection-object.md)

Дополнительные функциональные возможности доступны через определенные COM-интерфейсы. Доступность этих интерфейсов может зависеть от языка, используемого для программирования, и других факторов, таких как режим, используемый для создания экземпляра элемента управления проигрывателя Windows Media. Полный список COM-интерфейсов, предоставляемых элементом управления проигрывателя Windows Media, см. в [справочнике по объектной модели для C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Сведения об объектной модели проигрывателя**](about-the-player-object-model.md)
</dt> <dt>

[**Использование элемента управления проигрывателя Windows Media в платформа .NET Framework решении**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




