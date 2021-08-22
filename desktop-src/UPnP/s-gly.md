---
title: S (API-интерфейсы UPnP)
description: Содержит термины, связанные с UPnP, которые начинаются с буквы S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459bc1eff834e9bdb4c08b7d372d052faea78f98acc196b21ed7cfd1a2c73abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999514"
---
# <a name="s-upnp-apis"></a>S (API-интерфейсы UPnP)

Содержит термины, связанные с UPnP, которые начинаются с буквы S.

[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [р](h-gly.md) . J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z

<dl> <dt>

<span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**служеб**
</dt> <dd>

Служба — это логическая функциональная единица. Службы предоставляют действия и моделируют некоторые или все состояния физического устройства с помощью переменных состояния.

</dd> <dt>

<span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**Описание службы**
</dt> <dd>

Описание службы — это список действий, предоставляемых службой, и переменные состояния, связанные с действиями.

</dd> <dt>

<span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**Объект службы**
</dt> <dd>

Объект службы является представлением API контрольной точки для службы. Объект службы реализует интерфейс [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .

</dd> <dt>

<span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**Тип службы**
</dt> <dd>

Тип службы — это URN, идентифицирующий службу. Между шаблоном службы UPnP и типом службы существует связь «один к одному». Несколько стандартных типов служб определяются на форуме UPnP. Типы служб представлены в формате urn: schemas-UPnP-org: Service: serviceType: версия. Например, тип службы сканера может быть urn: schemas-UPnP-org: служба: сканер: 1.

Поставщики UPnP могут указывать дополнительные службы. Такие службы обозначаются urn: domain-name: Service: serviceType: версия, где domain-name — это доменное имя, зарегистрированное для поставщика.

</dd> <dt>

<span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**переменная состояния**
</dt> <dd>

Переменная состояния — это часть данных, которая описывает некоторую часть состояния службы.

</dd> </dl>

 

 




