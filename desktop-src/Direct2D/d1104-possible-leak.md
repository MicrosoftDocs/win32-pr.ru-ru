---
title: Возможная утечка D1104
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Фабрика была выпущена, но созданный из нее интерфейс все еще активен. Хотя после выпуска фабрики можно освободить ресурсы, это условие может указывать на утечку памяти.
keywords:
- D1104 возможная утечка Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333555"
---
# <a name="d1104-possible-leak"></a>D1104: возможная утечка

\[ *Фабрика* фабрики \] была выпущена, но интерфейс интерфейса, \[  \] созданный на ее основе, все еще активен. Хотя после выпуска фабрики можно освободить ресурсы, это условие может указывать на утечку памяти.

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="factory"></span><span id="FACTORY"></span>*установлен*
</dt> <dd>

Адрес выпущенной фабрики.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*
</dt> <dd>

Адрес интерфейса, созданного на *фабрике*.

</dd> </dl> 

|             |             |
|-------------|-------------|
| Уровень ошибки | Сведения |



 

## <a name="possible-causes"></a>Возможные причины

Фабрика была выпущена, но созданный из нее интерфейс все еще активен.

 

 




