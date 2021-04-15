---
description: Тип носителя (или режим) описывает тип передаваемых данных, например интерактивный речевой ввод. Данный сеанс связи может содержать несколько типов носителей.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Тип носителя для сеанса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547375"
---
# <a name="media-type-for-a-session"></a>Тип носителя для сеанса

Тип носителя (или режим) описывает тип передаваемых данных, например интерактивный речевой ввод. Данный сеанс связи может содержать несколько типов носителей.

Поставщики услуг предоставляют интерфейсу TAPI и приложениям тип или типы носителей, которые они поддерживают. Сведения о получении этих данных см. в разделе Общие сведения о [типе носителя](media-type-ovr.md) устройства.

**Интерфейс TAPI 2. x:** См. раздел [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**линесетмедиамоде**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**линемонитормедиа**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**Line \_ монитормедиа**](./line-monitormedia.md) сообщение, [ \_ константы линемедиамоде](./linemediamode--constants.md).

**Интерфейс TAPI 3. x:** См. раздел [**иткаллинфо:: Get \_ Каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) с **CIL \_ медиатипесаваилабле**, [**иткаллинфо::p UT \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) с **CIL \_ Медиатипесаваилабле**, [**ITCallInfoChangeEvent:: Get \_ Причина**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (Возвращает [**CALLINFOCHANGE \_ Причина**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) **CIC \_ MEDIATYPE**) [, \_ константы TAPIMEDIATYPE](tapimediatype--constants.md).

 

 
