---
description: Эти методы должны быть переопределены производными классами.
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: Чистые виртуальные методы Кмспаддресс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683472"
---
# <a name="cmspaddress-pure-virtual-methods"></a>Чистые виртуальные методы Кмспаддресс

Эти методы должны быть переопределены производными классами.



| Чистые виртуальные методы Кмспаддресс                           | Описание                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**мспаддрессаддреф**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | Частный метод AddRef для адреса.                                                                                                                                                 |
| [**мспаддрессрелеасе**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | Частный метод освобождения для адреса.                                                                                                                                                |
| [**креатемспкалл**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | Вызывается TAPI для создания объекта вызова. Реализация в производном классе должна просто вызывать функцию [**креатемспкаллхелпер**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) .        |
| [**шутдовнмспкалл**](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | Вызывается TAPI для завершения работы объекта вызова. Реализация в производном классе должна просто вызывать функцию [**шутдовнмспкаллхелпер**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) . |
| [**жеткаллмедиатипес**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | Возвращает типы носителей, поддерживаемые MSP.                                                                                                                                                 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**кмспаддресс**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



