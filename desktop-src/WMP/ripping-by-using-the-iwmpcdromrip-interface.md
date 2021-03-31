---
title: Копирование с помощью интерфейса Ивмпкдромрип
description: Копирование с помощью интерфейса Ивмпкдромрип
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
keywords:
- Проигрыватель Windows Media, копирование компакт-дисков
- Объектная модель проигрывателя Windows Media, копирование компакт-дисков
- Объектная модель, копирование компакт-дисков
- Элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Элемент управления ActiveX, копирование компакт-дисков
- Мобильный элемент управления ActiveX проигрывателя Windows Media, копирование компакт-дисков
- Проигрыватель Windows Media Mobile, копирование компакт-дисков
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Копирование компакт-дисков, интерфейс Ивмпкдромрип
- Интерфейс Ивмпкдромрип
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890256"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a>Копирование с помощью интерфейса Ивмпкдромрип

В этом разделе описывается использование интерфейса [ивмпкдромрип](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) для копирования музыки с компакт-диска.

Копирование компакт-диска с помощью интерфейса **ивмпкдромрип** действует так же, как копирование музыки с помощью пользовательского интерфейса проигрывателя Windows Media. Скопированное содержимое автоматически добавляется в библиотеку в соответствии с предпочтениями пользователя. Дополнительные сведения о копировании с компакт-диска см. в разделе «Копирование музыки с CD» в справке проигрывателя Windows Media.

В примерах кода в этом разделе используются классы библиотеки активных шаблонов (ATL), такие как **CComPtr**.

## <a name="included-headers"></a>Включаемые заголовки

Чтобы использовать код в этом разделе, включите следующие заголовки:


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a>Указатели интерфейса

Интерфейсы для проигрывателя Windows Media хранятся в следующих переменных члена.


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



В следующих разделах описывается использование интерфейса Ивмпкдромрип

-   [Получение интерфейса копирования данных с компакт-диска](retrieving-the-ripping-interface.md)
-   [Запуск процесса копирования](starting-the-rip-process.md)
-   [Получение состояния копирования](retrieving-the-rip-status.md)
-   [Выбор элементов для копирования](selecting-items-for-ripping.md)

 

 




