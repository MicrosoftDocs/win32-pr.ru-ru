---
description: Значения флагов СФГАО атрибутов оболочки для элемента можно проверить, чтобы определить, должна ли команда быть включена или отключена.
ms.assetid: 3A539A9D-DB6B-4E3D-AD26-D5309BECEBB1
title: Использование атрибутов элементов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a438c81258677822ca9b940eb9f74366d6226ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909531"
---
# <a name="how-to-use-item-attributes"></a>Использование атрибутов элементов

Значения флагов [**сфгао**](sfgao.md) атрибутов оболочки для элемента можно проверить, чтобы определить, должна ли команда быть включена или отключена.

Чтобы использовать эту функцию атрибута, добавьте в команду следующие значения **reg \_ DWORD** :

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Значение Аттрибутемаск указывает значение [**сфгао**](sfgao.md) для битовых значений маски для проверки.

### <a name="step-2"></a>Шаг 2.

Значение AttributeValue указывает значение [**сфгао**](sfgao.md) для проверяемых битов.

### <a name="step-3"></a>Шаг 3.

Имплиедселектионмодел указывает ноль для глаголов элемента или ненулевое значение для команд в контекстном меню фона.

## <a name="remarks"></a>Примечания

В следующем примере записи реестра Аттрибутемаск имеет значение [**сфгао \_ ReadOnly**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

 

 



