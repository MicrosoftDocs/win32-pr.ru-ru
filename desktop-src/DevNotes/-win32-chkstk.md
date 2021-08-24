---
description: Вызывается компилятором, если в функции имеется более одной страницы локальных переменных.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk подпрограммы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b129b73801c6c18b63b10ac61898ee13a9c5d4f1f0422678bbfe5af82d5b44f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538842"
---
# <a name="_chkstk-routine"></a>\_подпрограммы чкстк

Вызывается компилятором, если в функции имеется более одной страницы локальных переменных.

## <a name="remarks"></a>Remarks

\_подпрограммы чкстк — это вспомогательная подпрограммы для компилятора C. Для компиляторов x86 \_ подпрограммы чкстк вызываются, когда локальные переменные превышают 4000 байтов; для компиляторов x64 это 8 КБ.

 

 



