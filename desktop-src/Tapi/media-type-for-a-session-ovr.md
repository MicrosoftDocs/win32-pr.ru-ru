---
description: Тип носителя (или режим) описывает тип передаваемых данных, например интерактивный речевой ввод. Данный сеанс связи может содержать несколько типов носителей.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Тип носителя для сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974935baf17652c0376386eea63028ba04eeb886d1f48eba1aaf7f8469a9c374
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002882"
---
# <a name="media-type-for-a-session"></a>Тип носителя для сеанса

Тип носителя (или режим) описывает тип передаваемых данных, например интерактивный речевой ввод. Данный сеанс связи может содержать несколько типов носителей.

Поставщики услуг предоставляют интерфейсу TAPI и приложениям тип или типы носителей, которые они поддерживают. Сведения о получении этих данных см. в разделе Общие сведения о [типе носителя](media-type-ovr.md) устройства.

**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**линесетмедиамоде**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**линемонитормедиа**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**Line \_ монитормедиа**](./line-monitormedia.md) сообщение, [ \_ константы линемедиамоде](./linemediamode--constants.md).

**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ Каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) с **CIL \_ медиатипесаваилабле**, [**иткаллинфо::p UT \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) с **CIL \_ Медиатипесаваилабле**, [**ITCallInfoChangeEvent:: Get \_ Причина**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (Возвращает [**CALLINFOCHANGE \_ Причина**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) **CIC \_ MEDIATYPE**) [, \_ константы TAPIMEDIATYPE](tapimediatype--constants.md).

 

 
