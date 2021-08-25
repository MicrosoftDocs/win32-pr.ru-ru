---
title: Преобразование в VBScript из JScript
description: Преобразование в VBScript из JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3900ba82b258e6ee19cf06edb2f97247033778da5fcabaffe4a854e66a5fef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992254"
---
# <a name="translating-to-vbscript-from-jscript"></a>Преобразование в VBScript из JScript

В VBScript **для**... **Каждый** цикл выполняет перечисление элементов коллекции. в JScript, **для**... **в** loop выполняет перечисление элементов объекта JScript или массива. чтобы перечислить коллекцию в JScript, используйте объект перечислителя.

JScript предоставляет объект Error, который может использоваться для перехвата и обработки ошибок. Объект Error является аналогом объекта VBScript Err.

в JScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null. В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.

в JScript массивы можно развертывать динамически, задав новое значение для свойства length массива. В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .

функции поддержки VBScript и JScript. Однако VBScript также поддерживает подпрограммы. Подпрограммы похожи на функции, но не возвращают значение.

JScript учитывает регистр. Язык VBScript не является.

JScript поддерживается в разнообразных веб-браузерах, включая Internet Explorer и Netscape navigator. Netscape Navigator не поддерживает VBScript.

массивы JScript не являются массивами типа **VARIANT SAFEARRAY**. скрипт JScript должен использовать объект VBArray для доступа к переменной **SAFEARRAY типа VARIANT**. Скрипты VBScript могут напрямую обращаться к переменным **SAFEARRAY типа Variant**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразование в VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




