---
description: Предоставляет ограничения на использование 64-разрядных значений в составе пути.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Поддержка экземпляра класса для 64-разрядных значений
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674071"
---
# <a name="class-instance-support-for-64-bit-values"></a><span data-ttu-id="d2432-103">Поддержка экземпляра класса для 64-разрядных значений</span><span class="sxs-lookup"><span data-stu-id="d2432-103">Class Instance Support for 64-Bit Values</span></span>

<span data-ttu-id="d2432-104">В качестве части пути можно использовать 64-битное значение ключа со следующими ограничениями.</span><span class="sxs-lookup"><span data-stu-id="d2432-104">You can use a 64-bit key value as part of a path, with the following restrictions:</span></span>

-   <span data-ttu-id="d2432-105">При условии, что диапазон 32-бит не превышает, можно назначать и извлекать значения из ключа так же, как и для 32-разрядного свойства.</span><span class="sxs-lookup"><span data-stu-id="d2432-105">As long as you do not exceed the 32-bit range, you can assign and retrieve values from the key as you would a 32-bit property.</span></span>
-   <span data-ttu-id="d2432-106">После превышения целочисленного значения 0x7FFFFFFF (для типов со знаком), 0x80000000 (для неподписанных типов) или 32 бит, необходимо использовать кавычки.</span><span class="sxs-lookup"><span data-stu-id="d2432-106">After you exceed the integer value of 0x7FFFFFFF (for signed types), 0x80000000 (for unsigned types), or 32 bits, you must use quotation marks.</span></span>
-   <span data-ttu-id="d2432-107">Единственный допустимый путь для 64-разрядного значения находится в свойствах **\_ \_ релпас** или **\_ \_ path** экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d2432-107">The only valid path for a 64-bit value is located in the **\_\_RELPATH** or **\_\_PATH** properties of the instance.</span></span> <span data-ttu-id="d2432-108">Таким образом, Инструментарий WMI не поддерживает шестнадцатеричную нотацию для эквивалентного значения.</span><span class="sxs-lookup"><span data-stu-id="d2432-108">As such, WMI does not support the hexadecimal notation for the equivalent value.</span></span>
-   <span data-ttu-id="d2432-109">Если инструментарий WMI записывает ключ экземпляра в виде отрицательного числа, то для получения экземпляра необходимо использовать исходный номер.</span><span class="sxs-lookup"><span data-stu-id="d2432-109">If WMI records the instance key as a negative number, then you must use the original number to retrieve the instance.</span></span>

<span data-ttu-id="d2432-110">Семантика запросов не затрагивается и работает правильно.</span><span class="sxs-lookup"><span data-stu-id="d2432-110">Query semantics are unaffected and behave as expected.</span></span> <span data-ttu-id="d2432-111">Это поведение влияет только на операции [**path, GetObject и**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) объекта.</span><span class="sxs-lookup"><span data-stu-id="d2432-111">This behavior only affects the object path, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) operations.</span></span>

<span data-ttu-id="d2432-112">В следующем примере показано, что экземпляры класса могут иметь 64-разрядные значения ключа.</span><span class="sxs-lookup"><span data-stu-id="d2432-112">The following example shows that class instances can have 64-bit key values.</span></span>

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



