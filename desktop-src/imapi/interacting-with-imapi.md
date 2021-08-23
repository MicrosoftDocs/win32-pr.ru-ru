---
title: Взаимодействие с IMAPI
description: Следующие шаги описывают типичное взаимодействие между приложением и IMAPI.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab97d1a9d76d1e82dab64fb777ef5207d3d47560b2a889981c698ab78e3622b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726994"
---
# <a name="interacting-with-imapi"></a>Взаимодействие с IMAPI

Следующие шаги описывают типичное взаимодействие между приложением и IMAPI.

1.  Создайте экземпляр **мсдискмастеробж** (с помощью **CoCreateInstance**, смарт-указателей из импорта и т. д.) и запросите интерфейс [**идискмастер**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) .
2.  Получите доступ к IMAPI, вызвав [**идискмастер:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open). При успешном вызове приложение получает полный доступ ко всем интерфейсам и методам, реализованным в **мсдискмастеробж**.
3.  Получите перечислитель формата мастера дисков с помощью [**енумдискмастерформатс**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats). Перечисляет набор форматов, поддерживаемых главным объектом диска, а затем выберите активный формат. Форматы, возвращаемые из перечислителя, являются идентификаторов IID интерфейсов для [**ижолиетдискмастер**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) и [**иредбукдискмастер**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster).
4.  Получите перечислитель записи на диск с помощью [**енумдискрекордерс**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders). Перечислите список поддерживаемых средств записи дисков (для конкретного активного формата), а затем выберите активный объект записи. Интерфейс [**идискрекордер**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) представляет физическое устройство.
5.  Используйте [**идискмастер::P рогрессадвисе**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) , чтобы зарегистрировать обратные вызовы хода выполнения.
6.  Для создания содержимого используйте интерфейс для выбранного формата. Содержимое строится постепенно, поэтому дорожки или содержимое папки можно добавить на диск в части. Создание этого содержимого называется *промежуточной настройкой образа*. Содержимое промежуточного образа не может быть постепенно удалено (нельзя удалить добавленную запись), но можно очистить содержимое промежуточного образа, чтобы промежуточное хранение можно было запустить снова. Используйте [**идискмастер:: клеарформатконтент**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) для перезапуска промежуточного хранения.

* * Для аудио: * *

1.  Используйте [**иредбукдискмастер:: креатеаудиотракк**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) , чтобы указать, что на диске начинается новая звуковая дорожка.
2.  Используйте [**иредбукдискмастер:: аддаудиотраккблоккс**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) для добавления необработанных аудио-данных в дорожку. Приложение может использовать [**жетаваилаблеаудиотраккблоккс**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks), [**жеттоталаудиоблоккс**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)и [**жетуседаудиоблоккс**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) для получения статистических данных.
3.  Чтобы закрыть звуковую дорожку, используйте [**иредбукдискмастер:: клосеаудиотракк**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) .
4.  Повторите шаги 1-3, пока не освободится место или не будут записаны все звуковые дорожки.

* * Для данных: * *

1.  Чтобы добавить содержимое папки в образ, используйте [**ижолиетдискмастер:: адддата**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) . Элементы в папке помещаются в корневую папку файла изображения. Для получения статистических данных используйте [**жеттоталдатаблоккс**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) и [**жетуседдатаблоккс**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) .
2.  Повторите описанный выше шаг, пока не освободится место или не будут добавлены все данные.

* * Для всех дисков: * *

1.  Используйте [**идискмастер:: рекорддиск**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) для записи диска.
2.  Закройте сеанс IMAPI с помощью [**идискмастер:: Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). Закрытие сеанса очищает содержимое образа диска.

 

 




