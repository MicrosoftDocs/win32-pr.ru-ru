---
description: Операционная корреспонденция с драйвером устройства компенсации движения
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: Операционная корреспонденция с драйвером устройства компенсации движения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262347"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>Операционная корреспонденция с драйвером устройства компенсации движения

В этом разделе содержится описание стороны драйвера устройства компенсации движения для интерфейса DirectX ва. (Справочник: Windows 2000 DDK-Graphics Drivers-руководство по проектированию — 3,0 DirectDraw DDI-3,12 компенсация движения. Документацию по структурам в виде полужирного начертания см. в Windows DDK.)

Следующие элементы ссылаются на записи, доступные в структуре **DD \_ мотионкомпкаллбаккс** :

1.  В начале соответствующей обработки драйвер устройства **ддмокомпкреате** используется для уведомления драйвера о том, что программный декодер начнет использовать объект ускорения видео.
2.  Идентификаторы GUID, полученные от [**иамвидеоакцелератор:: жетвидеоакцелераторгуидс**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) , берутся из **ддмокомпжетгуидс** драйвера устройства.
3.  Вызов [**иамвидеоакцелератор:: жетункомпформатссуппортед**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) из **ддмокомпжетформатс** драйвера устройства возвращает данные.
4.  \_Структура данных дксва коннектмоде из [**иамвидеоакцелераторнотифи:: жеткреатевидеоакцелератордата**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) передается в **ддмокомпкреате** драйвера устройства.
5.  Данные, возвращаемые из [**иамвидеоакцелератор:: жеткомпбуфферинфо**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) , исходят от **ддмокомпжетбуффинфо** драйвера устройства.
6.  Буферы, отправленные с помощью [**иамвидеоакцелератор:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) , принимаются **ддмокомпрендер** драйвера устройства.
7.  Использование [**иамвидеоакцелератор:: куерирендерстатус**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) вызывает **ддмокомпкуеристатус** драйвера устройства. Код возврата ДДЕРР \_ васстиллдравинг из ддмокомпкуеристатус будет рассматриваться декодером хоста как код возврата E \_ в ожидании от **Иамвидеоакцелератор:: куерирендерстатус**.
8.  Данные, отправленные в [**иамвидеоакцелератор:: бегинфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) , поступают **ддмокомпбегинфраме** драйвера устройства. Для Ддмокомпбегинфраме требуется код возврата от «ожидание», чтобы в \_ \_ ответ на **Иамвидеоакцелератор:: бегинфраме** было видно, что в ожидании виден декодер узла.
9.  Данные, отправленные в [**иамвидеоакцелератор:: ендфраме**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) , поступают **ддмокомпендфраме** драйвера устройства.
10. В конце соответствующей обработки драйвер устройства **ддмокомпдестрой** используется для уведомления драйвера о том, что текущий объект ускорение видео больше не будет использоваться, чтобы драйвер мог выполнить необходимую очистку.

 

 



