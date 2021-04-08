---
description: Ниже приведены некоторые общие экземпляры условных операторов. Дополнительные сведения см. в разделе Синтаксис условных инструкций.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Примеры синтаксиса условных операторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991625"
---
# <a name="examples-of-conditional-statement-syntax"></a>Примеры синтаксиса условных операторов

Ниже приведены некоторые общие экземпляры условных операторов. Дополнительные сведения см. в разделе [Синтаксис условных инструкций](conditional-statement-syntax.md).

## <a name="run-action-on-removal"></a>Выполнить действие при удалении.

Дополнительные сведения см. [в разделе действия по обработке условий, выполняемые во время удаления](conditioning-actions-to-run-during-removal.md).

## <a name="run-action-only-if-the-product-has-not-been-installed"></a>Выполнить действие, только если продукт не был установлен.

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a>Выполнить действие, только если продукт будет установлен локально. Не выполнять действие при повторной установке.

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

Термин "&FeatureName = 3" означает, что действием является установка локального компонента. Термин «не (! FeatureName = 3) "означает, что эта функция не установлена локально.

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a>Выполнить действие, только если компонент будет удален.

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

Это условие проверяет только переход компонента из установленного состояния local в состояние отсутствия.

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a>Выполнить действие только в том случае, если компонент был установлен локально, но переходит из состояния.

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

Термин "? Компонетнаме = 3 означает, что компонент установлен локально. Термин "$ComponentName = 2" означает, что состояние действия в компоненте отсутствует. Термин "$ComponentName = 4" означает, что состояние действия в компоненте запускается из источника. Обратите внимание, что состояние действия объявления не является допустимым для компонента.

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a>Выполнить действие только при переустановке компонента.

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a>Выполнить действие только при применении конкретного исправления.

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

Дополнительные сведения см. в разделе "Примечания" на странице свойств [**исправления**](patch.md) .

 

 



