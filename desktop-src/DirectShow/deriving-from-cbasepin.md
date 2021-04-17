---
description: Наследование от Кбасепин
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Наследование от Кбасепин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ab56da3ae326be175c9519b5248e53fa02b82f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673110"
---
# <a name="deriving-from-cbasepin"></a>Наследование от Кбасепин

Чтобы реализовать ПИН-код с помощью [**кбасепин**](cbasepin.md), необходимо создать производный класс от базового класса и переопределить несколько его методов. Необходимо переопределить следующие методы.

-   [**Кбасепин:: Чеккмедиатипе**](cbasepin-checkmediatype.md)
-   [**Кбасепин:: Жетмедиатипе**](cbasepin-getmediatype.md)

Возможно, потребуется переопределить следующие дополнительные методы:

-   [**Кбасепин:: Active**](cbasepin-active.md)
-   [**Кбасепин:: Бреакконнект**](cbasepin-breakconnect.md)
-   [**Кбасепин:: Чеккконнект**](cbasepin-checkconnect.md)
-   [**Кбасепин:: Комплетеконнект**](cbasepin-completeconnect.md)
-   [**Кбасепин:: EndOfStream**](cbasepin-endofstream.md)
-   [**Кбасепин:: Inactive**](cbasepin-inactive.md)
-   [**Кбасепин:: notify**](cbasepin-notify.md)
-   [**Кбасепин:: Run**](cbasepin-run.md)

Наконец, необходимо реализовать методы [**Ипин:: бегинфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) и [**Ипин:: ендфлуш**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .

Некоторые из этих методов реализуются в базовых классах, производных от **кбасепин**, таких как [**кбасеинпутпин**](cbaseinputpin.md) и [**кбасеаутпутпин**](cbaseoutputpin.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**кбасепин**](cbasepin.md)
</dt> </dl>

 

 



