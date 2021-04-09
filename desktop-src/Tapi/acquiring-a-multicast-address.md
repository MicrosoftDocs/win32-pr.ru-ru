---
description: В следующем фрагменте кода показано, как запросить и задать адрес многоадресной рассылки для Конференции.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Получение адреса многоадресной рассылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144371"
---
# <a name="acquiring-a-multicast-address"></a>Получение адреса многоадресной рассылки

\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

В следующем фрагменте кода показано, как запросить и задать адрес многоадресной рассылки для Конференции.

В целях простоты этот фрагмент показывает назначение одного адреса многоадресной рассылки одному элементу мультимедиа. В действительности выбор области, запроса адреса многоадресной рассылки и назначения будет выполняться для каждого элемента мультимедиа, участвующего в Конференции.

В этом фрагменте предполагается, что [соединение с сервером ILS](connecting-to-an-ils-server.md) уже выполнено. Приведенные здесь операции будут выполнены в разделе "изменение параметров при необходимости" раздела [Создание объявления конференции](creating-a-conference-announcement.md).


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Многоадресные COM-интерфейсы](multicast-com-interfaces.md)
</dt> <dt>

[**имкастаддрессаллокатион**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[**имкастскопе**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[**имкастлеасеинфо**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[**иенуммкастскопе**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[**итконференцеблоб**](itconferenceblob.md)
</dt> <dt>

[**итсдп**](itsdp.md)
</dt> <dt>

[**итмедиаколлектион**](itmediacollection.md)
</dt> <dt>

[**иенумбстр**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[**итмедиа**](itmedia.md)
</dt> <dt>

[**итконнектион**](itconnection.md)
</dt> </dl>

 

 



