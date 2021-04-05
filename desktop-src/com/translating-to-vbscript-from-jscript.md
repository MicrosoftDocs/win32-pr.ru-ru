---
title: Преобразование в VBScript из JScript
description: Преобразование в VBScript из JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067664"
---
# <a name="translating-to-vbscript-from-jscript"></a>Преобразование в VBScript из JScript

В VBScript **для**... **Каждый** цикл выполняет перечисление элементов коллекции. в JScript **для**... **в** Loop выполняет перечисление элементов объекта или массива JScript. Чтобы перечислить коллекцию в JScript, используйте объект перечислителя.

JScript предоставляет объект Error, который может использоваться для перехвата и обработки ошибок. Объект Error является аналогом объекта VBScript Err.

В JScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null. В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.

В JScript массивы можно развертывать динамически, задав новое значение для свойства Length массива. В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .

Функции поддержки VBScript и JScript. Однако VBScript также поддерживает подпрограммы. Подпрограммы похожи на функции, но не возвращают значение.

В JScript учитывается регистр. Язык VBScript не является.

Язык JScript поддерживается многими веб-браузерами, включая Internet Explorer и Netscape Navigator. Netscape Navigator не поддерживает VBScript.

Массивы JScript не являются массивами типа **Variant SAFEARRAY**. Для доступа к переменной **типа SafeArray Variant** в скрипте JScript должен использоваться объект VBArray. Скрипты VBScript могут напрямую обращаться к переменным **SAFEARRAY типа Variant**.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразование в VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




