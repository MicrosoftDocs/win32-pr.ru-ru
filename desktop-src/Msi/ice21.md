---
description: ICE21 проверяет, относится каждый компонент в таблице Component к компоненту. Для проверки этого сопоставления используется таблица Феатурекомпонентс.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c5c517bd41c7d777f327606b3672f90b57a821dbbef028fa985acd043e6768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529034"
---
# <a name="ice21"></a>ICE21

ICE21 проверяет, относится каждый компонент в [таблице Component](component-table.md) к компоненту. Для проверки этого сопоставления используется [Таблица феатурекомпонентс](featurecomponents-table.md) .

## <a name="result"></a>Результат

ICE21 отправляет сообщение об ошибке, если пакет установки содержит компонент, который не принадлежит к компоненту.

## <a name="example"></a>Пример

В следующем примере ICE21 отправляет сообщение об ошибке, уведомляющее о том, что компонент comp1 не сопоставлен ни с одной функцией.

[Таблица Component](component-table.md) (частичная)



| Компонент |
|-----------|
| Comp1     |
| Comp2     |



 

[Таблица феатурекомпонентс](featurecomponents-table.md) (частичная)



| Компонент  | Компонент |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



