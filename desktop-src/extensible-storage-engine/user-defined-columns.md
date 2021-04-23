---
description: 'Дополнительные сведения: определяемые пользователем столбцы'
title: Определяемые пользователем столбцы
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080513"
---
# <a name="user-defined-columns"></a><span data-ttu-id="5a327-103">Определяемые пользователем столбцы</span><span class="sxs-lookup"><span data-stu-id="5a327-103">User Defined Columns</span></span>


<span data-ttu-id="5a327-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5a327-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="user-defined-columns"></a><span data-ttu-id="5a327-105">Определяемые пользователем столбцы</span><span class="sxs-lookup"><span data-stu-id="5a327-105">User Defined Columns</span></span>

<span data-ttu-id="5a327-106">Определяемые пользователем столбцы — это столбцы, значения по умолчанию которых предоставляются функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="5a327-106">User defined columns are columns whose default values are provided by a callback function.</span></span> <span data-ttu-id="5a327-107">Эти столбцы всегда помечаются тегами и задаются значением, вычисленным функцией обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="5a327-107">These columns are always tagged and set to the value computed by the callback function.</span></span> <span data-ttu-id="5a327-108">Это значение должно быть стабильным для каждой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="5a327-108">This value must be stable for each row in the table.</span></span> <span data-ttu-id="5a327-109">Функция обратного вызова используется только в том случае, когда приложению или ядру СУБД необходимо считать значение столбца для данной строки.</span><span class="sxs-lookup"><span data-stu-id="5a327-109">The callback function is only used when either the application or the database engine itself needs to read the value of the column for a given row.</span></span> <span data-ttu-id="5a327-110">Приложение имеет возможность переопределить значение по умолчанию и задать определенное значение в столбце.</span><span class="sxs-lookup"><span data-stu-id="5a327-110">The application has the option to override the default value and set a specific value in the column.</span></span> <span data-ttu-id="5a327-111">Когда значение по умолчанию переопределяется в столбцах, оно использует место в строке, в противном случае в пользовательских столбцах, заданных по умолчанию, не используется место в записи.</span><span class="sxs-lookup"><span data-stu-id="5a327-111">When the default value is overridden in the columns, it uses space in the row, otherwise user defined default columns do not use space in the record.</span></span>

<span data-ttu-id="5a327-112">Параметр "пользовательские значения по умолчанию" задается в элементе **грбит** структуры [JET_COLUMNDEF](./jet-columndef-structure.md) в вызове [жетаддколумн](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="5a327-112">User defined defaults option is set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="5a327-113">Параметр *пвдефаулт* функции [жетаддколумн](./jetaddcolumn-function.md) указывает на структуру [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , которая содержит имя функции обратного вызова в элементе **сзкаллбакк** и данные, передаваемые обратному вызову в элементе **пбусердата** .</span><span class="sxs-lookup"><span data-stu-id="5a327-113">The *pvDefault* parameter of the [JetAddColumn](./jetaddcolumn-function.md) function points to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure, that contains the name of the callback function in the **szCallback** member, and the data that is passed to the callback in the **pbUserData** member.</span></span>
