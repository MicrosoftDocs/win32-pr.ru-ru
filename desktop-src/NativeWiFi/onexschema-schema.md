---
description: Определяет элементы конфигурации 802.1 X.
ms.assetid: 4755356e-cb4b-4eed-a494-ca0d17f5184f
title: Схема OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9df45ed7981c055e955afe72333a42db99ddb21a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264377"
---
# <a name="onex-schema"></a>Схема OneX

Схема OneX определяет элементы конфигурации 802.1 X. Все элементы схемы OneX применяются к профилям проводного и беспроводного подключения. Список определенных элементов см. в разделе [элементы схемы OneX](onexschema-elements.md).

Корневым элементом профиля 802.1 X является элемент [**OneX**](onexschema-onex-element.md) . Каждый профиль будет иметь только один корневой элемент. Элемент **OneX** находится в `https://www.microsoft.com/networking/OneX/v1` пространстве имен.

Чтобы просмотреть образцы профилей для беспроводных сетей, включающих элементы конфигурации 802.1 X, см. следующие примеры профилей:

-   [Образец профиля начальной загрузки](bootstrap-profile-sample.md)
-   [Пример профиля FIPS](fips-profile-sample.md)
-   [Пример профиля с одним Sign-On](single-sign-on-profile-sample.md)
-   [Пример профиля WPA-Enterprise с PEAP-MSCHAPv2](wpa-enterprise-with-peap-mschapv2-profile-sample.md)
-   [Пример профиля WPA-Enterprise с TLS](wpa-enterprise-with-tls-profile-sample.md)
-   [Пример профиля WPA2-Enterprise с PEAP-MSCHAPv2](wpa2-enterprise-with-peap-mschapv2-profile-sample.md)
-   [Пример профиля WPA2-Enterprise с TLS](wpa2-enterprise-with-tls-profile-sample.md)

Чтобы просмотреть образцы профилей для проводных сетей, содержащих элементы конфигурации 802.1 X, см. следующие примеры профилей:

-   [Пример профиля сертификата компьютера](machine-certificate-profile-sample.md)
-   [Пример профиля PEAP](peap-profile-sample.md)
-   [Пример профиля сертификата смарт-карты](smart-card-certificate-profile-sample.md)

 

 



