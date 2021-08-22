---
title: тримигхтбециклик
description: тримигхтбециклик
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af2f8d93c3b38b52871db031419756507e009f7d8adb369fde9b5b2c154fbec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614443"
---
# <a name="treemightbecyclic"></a>тримигхтбециклик

## <a name="text"></a>Текст

Дерево имеет {0} уровень вложенности. Это может означать, что дерево специальных возможностей является циклическим, и поэтому оно кажется бесконечным.

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Дерево элементов является циклическим, а глубина дерева может быть бесконечной.

Эта проблема вызывает проблемы для людей, которые используют средство чтения с экрана и клавиатуру для навигации, так как в целевом приложении не будет заметного ограничения для обхода элементов.

## <a name="possible-causes"></a>Возможные причины

Несколько элементов или их родителей являются пользовательскими элементами управления, которые не реализуют правильную работу с вкладками. Например, свойство [состояния](state-property.md) MSAA неправильно обновляется.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Рекомендации по проектированию пользовательского интерфейса клавиатуры](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows Рекомендации по взаимодействию с пользователем. клавиатура](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 