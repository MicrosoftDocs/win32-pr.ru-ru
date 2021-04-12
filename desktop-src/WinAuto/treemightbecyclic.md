---
title: тримигхтбециклик
description: тримигхтбециклик
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337668"
---
# <a name="treemightbecyclic"></a>тримигхтбециклик

## <a name="text"></a>Текст

Дерево имеет {0} уровень вложенности. Это может означать, что дерево специальных возможностей является циклическим, и поэтому оно кажется бесконечным.

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Дерево элементов является циклическим, а глубина дерева может быть бесконечной.

Эта проблема вызывает проблемы для людей, которые используют средство чтения с экрана и клавиатуру для навигации, так как в целевом приложении не будет заметного ограничения для обхода элементов.

## <a name="possible-causes"></a>Возможные причины

Несколько элементов или их родителей являются пользовательскими элементами управления, которые не реализуют правильную работу с вкладками. Например, свойство [состояния](state-property.md) MSAA неправильно обновляется.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Рекомендации по проектированию пользовательского интерфейса клавиатуры](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Рекомендации по взаимодействию с пользователем Windows — клавиатура](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 