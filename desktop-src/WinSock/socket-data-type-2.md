---
description: В приложениях Winsock дескриптор сокета не является дескриптором файла и должен использоваться с функциями Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Тип данных сокета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347065"
---
# <a name="socket-data-type"></a><span data-ttu-id="955d7-103">Тип данных сокета</span><span class="sxs-lookup"><span data-stu-id="955d7-103">Socket Data Type</span></span>

<span data-ttu-id="955d7-104">В приложениях Winsock дескриптор сокета не является дескриптором файла и должен использоваться с функциями Winsock.</span><span class="sxs-lookup"><span data-stu-id="955d7-104">In Winsock applications, a socket descriptor is not a file descriptor and must be used with the Winsock functions.</span></span>

<span data-ttu-id="955d7-105">В UNIX дескриптор сокета представлен стандартным дескриптором файла.</span><span class="sxs-lookup"><span data-stu-id="955d7-105">In UNIX, a socket descriptor is represented by a standard file descriptor.</span></span> <span data-ttu-id="955d7-106">В результате дескриптор сокета в UNIX может быть передан любой из стандартных функций файлового ввода-вывода (например, чтение и запись).</span><span class="sxs-lookup"><span data-stu-id="955d7-106">As a result, a socket descriptor on UNIX may be passed to any of the standard file I/O functions (read and write, for example).</span></span>

<span data-ttu-id="955d7-107">Кроме того, все дескрипторы в UNIX, включая дескрипторы сокетов, являются мелкими неотрицательными целыми числами, и некоторые приложения делают предположения, что это будет истинно.</span><span class="sxs-lookup"><span data-stu-id="955d7-107">Furthermore, all handles in UNIX, including socket handles, are small, non-negative integers, and some applications make assumptions that this will be true.</span></span>

<span data-ttu-id="955d7-108">Дескрипторы сокетов Windows не имеют ограничений, Кроме того, что значение недопустимый \_ сокет не является допустимым сокетом.</span><span class="sxs-lookup"><span data-stu-id="955d7-108">Windows Sockets handles have no restrictions, other than that the value INVALID\_SOCKET is not a valid socket.</span></span> <span data-ttu-id="955d7-109">Дескрипторы сокетов могут принимать любое значение в диапазоне от 0 до НЕДОПУСТИМого \_ сокета — 1.</span><span class="sxs-lookup"><span data-stu-id="955d7-109">Socket handles may take any value in the range 0 to INVALID\_SOCKET–1.</span></span>

<span data-ttu-id="955d7-110">Поскольку тип **сокета** не подписан, компиляция существующего исходного кода из, например среды UNIX, может привести к предупреждениям компилятора о несоответствии типа данных со знаком и без знака.</span><span class="sxs-lookup"><span data-stu-id="955d7-110">Because the **SOCKET** type is unsigned, compiling existing source code from, for example, a UNIX environment may lead to compiler warnings about signed/unsigned data type mismatches.</span></span>

<span data-ttu-id="955d7-111">Это означает, например, что проверка ошибок, возникающих при возврате функций [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) и [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , не должна выполняться путем сравнения возвращаемого значения со значением – 1 или просмотра отрицательного значения (как общих, так и юридических подходов в UNIX).</span><span class="sxs-lookup"><span data-stu-id="955d7-111">This means, for example, that checking for errors when the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) functions return should not be done by comparing the return value with –1, or seeing if the value is negative (both common and legal approaches in UNIX).</span></span> <span data-ttu-id="955d7-112">Вместо этого приложение должно использовать константу манифеста недопустимый \_ сокет, как определено в файле заголовка *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="955d7-112">Instead, an application should use the manifest constant INVALID\_SOCKET as defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="955d7-113">Пример:</span><span class="sxs-lookup"><span data-stu-id="955d7-113">For example:</span></span>

<span data-ttu-id="955d7-114">Стандартный стиль BSD в UNIX</span><span class="sxs-lookup"><span data-stu-id="955d7-114">Typical BSD UNIX Style</span></span>


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



<span data-ttu-id="955d7-115">Предпочтительный стиль</span><span class="sxs-lookup"><span data-stu-id="955d7-115">Preferred Style</span></span>


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a><span data-ttu-id="955d7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="955d7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="955d7-117">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="955d7-117">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="955d7-118">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="955d7-118">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



