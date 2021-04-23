---
title: Использование флага/robust
description: Всегда компилируйте IDL-файлы с помощью параметра/robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987649"
---
# <a name="use-the-robust-flag"></a><span data-ttu-id="e9229-103">Использование флага/robust</span><span class="sxs-lookup"><span data-stu-id="e9229-103">Use the /robust Flag</span></span>

<span data-ttu-id="e9229-104">Всегда компилируйте IDL-файлы с помощью параметра [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="e9229-104">Always compile .idl files using the [**/robust**](/windows/desktop/Midl/-robust) switch.</span></span> <span data-ttu-id="e9229-105">С помощью параметра **/robust** создаются дополнительные сведения, позволяющие подсистеме представления данных сети выполнять проверку ошибок во время выполнения для коррелированных аргументов в динамических массивах, объединениях и в указателях интерфейса в приложениях COM и RPC.</span><span class="sxs-lookup"><span data-stu-id="e9229-105">Using the **/robust** switch generates additional information that enables the Network Data Representation (NDR) engine to perform run-time error checking on correlated arguments in dynamic arrays, unions, and in out interface pointers in COM and RPC applications.</span></span> <span data-ttu-id="e9229-106">Если по не удается скомпилировать программное обеспечение с этим флагом, программное обеспечение становится доступным для атак, которые не могут быть защищены в какой-либо другой области.</span><span class="sxs-lookup"><span data-stu-id="e9229-106">If software fails to compile with this flag, the software is so exposed to attacks that no efforts in any other area can protect it.</span></span>

 

 