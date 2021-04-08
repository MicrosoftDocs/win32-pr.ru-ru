---
title: Оператор разрешения области в C++
description: Оператор разрешения области в C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888439"
---
# <a name="the-scope-resolution-operator-in-c"></a>Оператор разрешения области в C++

Два двоеточия (::) используются в C++ в качестве оператора *разрешения области* . Этот оператор обеспечивает большую свободу при именовании переменных, позволяя различать переменные с одинаковыми именами. Например, класс *MyFile:: Read* относится к методу *Read* класса *MyFile* объектов, а не к *йоурфиле:: Read*, который ссылается на метод *Read* в классе *йоурфиле* .

 

 




