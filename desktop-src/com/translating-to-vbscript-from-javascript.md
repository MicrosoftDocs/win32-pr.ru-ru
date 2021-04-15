---
title: Преобразование в VBScript из JavaScript
description: Преобразование в VBScript из JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710051"
---
# <a name="translating-to-vbscript-from-javascript"></a>Преобразование в VBScript из JavaScript

В JavaScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null. В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.

В JavaScript массивы можно развертывать динамически, задав новое значение для свойства Length массива. В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .

Функции поддержки VBScript и JavaScript. Однако VBScript также поддерживает подпрограммы. Подпрограммы похожи на функции, за исключением того, что они не возвращают значение.

В языке JavaScript учитывается регистр символов. Язык VBScript не является.

JavaScript поддерживается в разнообразных веб-браузерах, включая Internet Explorer и Netscape Navigator. Netscape Navigator не поддерживает VBScript.

Сценарий VBScript поддерживает обработку ошибок через объект Err. JavaScript в настоящее время не предоставляет средств перехвата и обработки ошибок.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразование в VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




