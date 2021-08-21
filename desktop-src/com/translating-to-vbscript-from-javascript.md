---
title: Преобразование в VBScript из JavaScript
description: Преобразование в VBScript из JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6138a6d13710e87ae2b80c979b208d0360e28501ce5d763546a1605c49f0802a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047742"
---
# <a name="translating-to-vbscript-from-javascript"></a>Преобразование в VBScript из JavaScript

В JavaScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null. В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.

В JavaScript массивы можно развертывать динамически, задав новое значение для свойства Length массива. В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .

Функции поддержки VBScript и JavaScript. Однако VBScript также поддерживает подпрограммы. Подпрограммы похожи на функции, за исключением того, что они не возвращают значение.

В языке JavaScript учитывается регистр символов. Язык VBScript не является.

JavaScript поддерживается в разнообразных веб-браузерах, включая Internet Explorer и Netscape Navigator. Netscape Navigator не поддерживает VBScript.

Сценарий VBScript поддерживает обработку ошибок через объект Err. JavaScript в настоящее время не предоставляет средств перехвата и обработки ошибок.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразование в VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




