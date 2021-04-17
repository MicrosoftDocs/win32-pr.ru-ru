---
description: ICE21 проверяет, относится каждый компонент в таблице Component к компоненту. Для проверки этого сопоставления используется таблица Феатурекомпонентс.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663668"
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



| Функция  | Компонент |
|----------|-----------|
| Feature1 | Comp2     |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по ICE](ice-reference.md)
</dt> </dl>

 

 



