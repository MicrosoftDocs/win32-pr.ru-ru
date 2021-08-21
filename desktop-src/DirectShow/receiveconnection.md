---
description: рецеивеконнектион
ms.assetid: 90a6a09a-95e1-4adf-8e0b-269f971aaa67
title: рецеивеконнектион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a8a91cbf9870d6c53592ff823f710eb5875fa939592309425df0a0bca6f0e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072768"
---
# <a name="receiveconnection"></a>рецеивеконнектион

Этот механизм позволяет выходному закреплениям предложить изменение формата для его подчиненного однорангового узла, если для нового формата требуется больший буфер. Закрепление вывода выполняет следующие действия:

1.  Вызывает [**Ипин:: рецеивеконнектион**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) для входного ПИН-кода нисходящего входа.
2.  Если операция `ReceiveConnection` выполнена, вызывается [**имеминпутпин:: нотифяллокатор**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) для входного ПИН-кода.

Кроме того, для изменения размеров буфера может потребоваться вызвать [**имемаллокатор:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) , а затем открепить и повторно зафиксировать распределитель. Перед изменением размера буфера обязательно Доставьте все ожидающие выборки в старом формате.

Некоторые декодеры MPEG-2 используют этот механизм для переключения между выходными данными MPEG-1 и MPEG-2, а также при изменении размера видео.

 

 



