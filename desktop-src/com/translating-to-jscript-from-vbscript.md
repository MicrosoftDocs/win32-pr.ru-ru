---
title: Преобразование в JScript из VBScript
description: Преобразование в JScript из VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773568"
---
# <a name="translating-to-jscript-from-vbscript"></a>Преобразование в JScript из VBScript

В VBScript **для**... **Каждый** цикл выполняет перечисление элементов коллекции. в JScript **для**... **в** Loop выполняет перечисление элементов объекта или массива JScript. Чтобы перечислить коллекцию в JScript, используйте объект перечислителя.

В JScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null. В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.

В JScript массивы можно развертывать динамически, задав новое значение для свойства Length массива. В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .

Функции поддержки VBScript и JScript. Однако VBScript также поддерживает подпрограммы. Подпрограммы похожи на функции, но не возвращают значение.

В JScript учитывается регистр. Язык VBScript не является.

Язык JScript поддерживается как Internet Explorer, так и Netscape Navigator. Netscape Navigator не поддерживает VBScript.

JScript предоставляет объект Error, который может использоваться для перехвата и обработки ошибок. Объект Error является аналогом объекта VBScript Err.

Массивы JScript не являются массивами типа **Variant SAFEARRAY**. Если скрипт получает переменную **SAFEARRAY типа Variant** из COM-объекта или скрипта VBScript, он должен использовать объект VBArray для доступа к переменной **типа SafeArray** .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразование в JScript](translating-to-jscript.md)
</dt> </dl>

 

 




