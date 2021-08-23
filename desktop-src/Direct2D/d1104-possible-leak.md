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
ms.openlocfilehash: b3c8b49256b3e7009985e9acf6d2b581e2fe436e50325c26f1f7de59cb3b0b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075568"
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

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Уровень ошибки | Информация |



 

## <a name="possible-causes"></a>Возможные причины

Фабрика была выпущена, но созданный из нее интерфейс все еще активен.

 

 




