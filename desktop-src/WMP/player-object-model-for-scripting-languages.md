---
title: Объектная модель проигрывателя для языков сценариев
description: Объектная модель проигрывателя для языков сценариев
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- проигрыватель Windows Media, объектная модель
- объектная модель проигрыватель Windows Media, сведения
- Объектная модель, сведения
- проигрыватель Windows Media ActiveX элемент управления, объектная модель
- элемент управления ActiveX, объектная модель
- проигрыватель Windows Media мобильный ActiveX элемент управления, объектная модель
- проигрыватель Windows Media Мобильные устройства, объектная модель
- пакет средств разработки программного обеспечения (SDK), объектная модель проигрыватель Windows Media ActiveX элементов управления
- пакет SDK (пакет средств разработки программного обеспечения), проигрыватель Windows Media объектная модель ActiveX элементов управления
- документация, проигрыватель Windows Media объектная модель ActiveX элемента управления
- проигрыватель Windows Media, языки сценариев
- проигрыватель Windows Media объектной модели, языки сценариев
- Объектная модель, языки сценариев
- проигрыватель Windows Media ActiveX элемент управления, языки сценариев
- ActiveX элемент управления, языки сценариев
- проигрыватель Windows Media управление мобильными ActiveXми, языки сценариев
- проигрыватель Windows Media Мобильные, языки сценариев
- Языки сценариев
- проигрыватель Windows Media, объект Player
- объектная модель проигрыватель Windows Media, объект Player
- Объектная модель, объект Player
- проигрыватель Windows Media ActiveX элемент управления, объект Player
- элемент управления ActiveX, объект Player
- проигрыватель Windows Media мобильный ActiveX элемент управления, объект Player
- проигрыватель Windows Media Мобильный, объект Player
- Объект Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe34bfc227dfe250a9c9d7ebb60977a9ab079c4a062067c65e83e62f0e5976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996033"
---
# <a name="player-object-model-for-scripting-languages"></a>Объектная модель проигрывателя для языков сценариев

ActiveX использует концепцию объектов для хранения функциональных возможностей программирования. проигрыватель Windows Media использует несколько объектов для разделения функциональных возможностей, предоставляемых элементом управления. Корневой объект — это объект **Player** , а другие объекты присоединяются к объекту **Player** через определенные свойства.

на следующей схеме показано, как работает объектная модель ActiveX элемента управления проигрыватель Windows Media 11 для языков сценариев.

![Схема объектной модели проигрывателя Windows Media 11](images/playeromdiag.png)

В C++ и иногда в языках .NET объекты представлены COM-интерфейсами. в объектной модели проигрыватель Windows Media имена COM-интерфейсов совпадают с именами объектов, но начинаются с префикса "ивмп". Например, объект **сети** предоставляется через интерфейс **ивмпнетворк** .

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
-   [об объекте Параметры](about-the-settings-object.md)
-   [Сведения об объекте StringCollection](about-the-stringcollection-object.md)

Дополнительные функциональные возможности доступны через определенные COM-интерфейсы. доступность этих интерфейсов может зависеть от языка, используемого для программирования, и других факторов, таких как режим, используемый для создания экземпляра элемента управления проигрыватель Windows Media. полный список COM-интерфейсов, предоставляемых элементом управления проигрыватель Windows Media, см. в [справочнике по объектной модели для C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Сведения об объектной модели проигрывателя**](about-the-player-object-model.md)
</dt> <dt>

[**использование элемента управления проигрыватель Windows Media в решении платформа .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




