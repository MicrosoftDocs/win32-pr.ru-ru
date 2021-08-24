---
description: 'когда приложение выполняет операцию ипропертистораже:: вритемултипле для любого записываемого Windowsного изображения (wia), драйвер WIA выполняет проверку нового значения свойства.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Проверка свойства WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1aca5879dbcb789b7e94a780c8fc99e53b703f6aea74498ae455e8e2ec6b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813054"
---
# <a name="wia-property-validation"></a>Проверка свойства WIA

когда приложение выполняет операцию [ипропертистораже:: вритемултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) для любого записываемого Windowsного изображения (wia), драйвер WIA выполняет проверку нового значения свойства. Запись одного свойства может повлиять на изменение других значений свойств. Приложение считывает все значения свойств после операции записи, чтобы определить, что для всех свойств задано значение, необходимое для приложения.

Несколько свойств можно записать одновременно с помощью операции [ипропертистораже:: вритемултипле](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) . Возможны случаи, когда некоторые назначения свойств конфликтуют. В таких случаях приоритет разрешения конфликтов используется следующим образом:

1.  выявляются \_ IP-адреса с \_ \_ целью по WIA
2.  \_ \_ тип данных WIA IPA
3.  \_глубина IPA \_ WIA
4.  \_ксрес IP-адресов WIA \_
5.  \_ирес IP-адресов WIA \_
6.  \_кспос IP-адресов WIA \_
7.  \_ИПОС IP-адресов WIA \_
8.  \_ксекстент IP-адресов WIA \_
9.  \_екстент IP-адресов WIA \_

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
