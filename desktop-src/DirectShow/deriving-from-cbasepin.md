---
description: Наследование от Кбасепин
ms.assetid: ef453bec-e5a9-4185-94e3-f934e748b11f
title: Наследование от Кбасепин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07eb76fc2913152a69ec729f49826e8b35f1524a3841c5e0d3085ea0634f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079264"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**кбасепин**](cbasepin.md)
</dt> </dl>

 

 



