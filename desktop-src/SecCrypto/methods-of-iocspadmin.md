---
description: Следующие методы определяются интерфейсом Иокспадмин. Методы доступа к свойствам не показаны здесь. Сведения о свойствах Иокспадмин см. в разделе Свойства Иокспадмин.
ms.assetid: cbe43e5d-cd1b-467c-a0fd-1ee7cc5adcf7
title: Методы Иокспадмин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecd14d2566c5e80e863ba06e38b2945492f59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343845"
---
# <a name="methods-of-iocspadmin"></a>Методы Иокспадмин

Следующие методы определяются интерфейсом [**иокспадмин**](/windows/desktop/api/certadm/nn-certadm-iocspadmin) . Методы доступа к свойствам не показаны здесь. Сведения о свойствах **иокспадмин** см. в разделе [Свойства иокспадмин](properties-of-iocspadmin.md).



| Метод                                                              | Описание                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getconfiguration)      | Подключается к серверу ответчика Online Certificate Status Protocol (OCSP) и инициализирует объект **окспадмин** с данными конфигурации с сервера.                                                                                                     |
| [**жесашалгорисмс**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-gethashalgorithms)           | Возвращает список имен хэш-алгоритма. Сервер респондента использует один из именованных алгоритмов для подписи ответов OCSP для определенной конфигурации [*центра сертификации*](../secgloss/c-gly.md) (ЦС). |
| [**жетмиролес**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getmyroles)                  | Получает маску доступа для ролей привилегий для пользователя на данном сервере респондента.                                                                                                                                                                                           |
| [**Безопасность**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsecurity)                       | Возвращает сведения о дескрипторе безопасности для сервера респондента.                                                                                                                                                                                                              |
| [**жетсигнингцертификатес**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-getsigningcertificates) | Возвращает сертификаты подписи, доступные на сервере респондента для данного сертификата ЦС.                                                                                                                                                                        |
| [**Проверок**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-ping)                                     | Проверяет DCOM-подключение к службе респондента.                                                                                                                                                                                                                         |
| [**SetConfiguration**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setconfiguration)      | Обновляет службу ответчика с изменениями конфигурации.                                                                                                                                                                                                                   |
| [**SetSecurity**](/windows/desktop/api/Certadm/nf-certadm-iocspadmin-setsecurity)                       | Обновляет сведения о дескрипторе безопасности для сервера ответчика OCSP.                                                                                                                                                                                                     |



 

 

 
