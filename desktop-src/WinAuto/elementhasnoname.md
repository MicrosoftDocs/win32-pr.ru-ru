---
title: елеменсаснонаме
description: елеменсаснонаме
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332659"
---
# <a name="elementhasnoname"></a>елеменсаснонаме

## <a name="text"></a>Текст

У элемента нет имени

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

У элемента нет имени. Например, элемент не имеет реализованного Аккнаме и возвращается пустая строка, если метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) используется для получения имени MSAA элемента.

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку элемент может быть неверно идентифицирован пользователю.

## <a name="possible-causes"></a>Возможные причины

-   У элемента или его родителя нет имени или метки.
-   Элементу назначается [**аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) , предлагающий элементу имя.
-   Элемент, имеющий фокус, не должен получать фокус. Например, метка или отключенный элемент управления.
-   Фокус получен на невидимый элемент управления.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Свойство Name](name-property.md)
</dt> </dl>

 

 




