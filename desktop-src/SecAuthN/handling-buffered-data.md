---
description: Некоторые функции поставщика сети принимают адрес и размер буфера, в который функция помещает структуру данных с переменным размером.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Обработка буферизованных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265814"
---
# <a name="handling-buffered-data"></a><span data-ttu-id="a0b81-103">Обработка буферизованных данных</span><span class="sxs-lookup"><span data-stu-id="a0b81-103">Handling Buffered Data</span></span>

<span data-ttu-id="a0b81-104">Некоторые функции поставщика сети принимают адрес и размер буфера, в который функция помещает структуру данных с переменным размером.</span><span class="sxs-lookup"><span data-stu-id="a0b81-104">Several of the network provider functions take the address and size of a buffer into which the function places a variable-sized data structure.</span></span>

<span data-ttu-id="a0b81-105">В каждом случае используется один и тот же механизм.</span><span class="sxs-lookup"><span data-stu-id="a0b81-105">In each case, the mechanism used is the same.</span></span> <span data-ttu-id="a0b81-106">Вызывающий объект выделяет буфер и передает его адрес в функцию.</span><span class="sxs-lookup"><span data-stu-id="a0b81-106">The caller allocates a buffer and passes its address to the function.</span></span> <span data-ttu-id="a0b81-107">Он также передает адрес **DWORD** , указывающий размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="a0b81-107">It also passes the address of a **DWORD** that specifies the size of the buffer, in bytes.</span></span>

<span data-ttu-id="a0b81-108">Затем функция копирует как часть запрашиваемой структуры данных, так как она может находиться в буфере.</span><span class="sxs-lookup"><span data-stu-id="a0b81-108">The function then copies as much of the requested data structure as it can into the buffer.</span></span> <span data-ttu-id="a0b81-109">Если все данные умещаются в буфер, функция возвращает WN \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a0b81-109">If all of the data fits into the buffer, the function returns WN\_SUCCESS.</span></span> <span data-ttu-id="a0b81-110">Если данные не помещаются в буфер, данные могут остаться неполными, а функция устанавливает \_ ошибку WN more \_ Data.</span><span class="sxs-lookup"><span data-stu-id="a0b81-110">If the data does not fit into the buffer, the data may be left incomplete, and the function sets the WN\_MORE\_DATA error.</span></span> <span data-ttu-id="a0b81-111">В любом случае **параметр DWORD** , указывающий размер буфера, устанавливается равным числу байтов, фактически необходимых для структуры данных.</span><span class="sxs-lookup"><span data-stu-id="a0b81-111">In either case, the **DWORD** indicating the size of the buffer is set to the number of bytes actually required by the data structure.</span></span> <span data-ttu-id="a0b81-112">Таким образом, если переданный буфер был слишком мал и функция завершилась ошибкой, вызывающий объект может выделить новый буфер требуемого размера и вызвать функцию еще раз.</span><span class="sxs-lookup"><span data-stu-id="a0b81-112">This way, if the buffer passed in was too small and the function failed, the caller may allocate a new buffer of the required size and call the function again.</span></span>

<span data-ttu-id="a0b81-113">Когда возвращаемые структуры данных содержат строки переменной длины, отдельные структуры данных обычно содержат указатели на эти строки.</span><span class="sxs-lookup"><span data-stu-id="a0b81-113">When the data structures returned include variable-length strings, the individual data structures typically contain pointers to these strings.</span></span> <span data-ttu-id="a0b81-114">Сами строки также должны размещаться в буфере.</span><span class="sxs-lookup"><span data-stu-id="a0b81-114">The strings themselves should also be placed within the buffer.</span></span> <span data-ttu-id="a0b81-115">Однако важно поместить их в конец буфера.</span><span class="sxs-lookup"><span data-stu-id="a0b81-115">However, it is important to place them at the end of the buffer.</span></span> <span data-ttu-id="a0b81-116">В противном случае они будут выполнять индексирование до n структуры.</span><span class="sxs-lookup"><span data-stu-id="a0b81-116">Otherwise, they will make indexing to the Nth structure impossible.</span></span> <span data-ttu-id="a0b81-117">Иными словами, все структуры располагаются последовательно в начале буфера.</span><span class="sxs-lookup"><span data-stu-id="a0b81-117">In other words, all structures are located contiguously at the beginning of the buffer.</span></span> <span data-ttu-id="a0b81-118">Указатели на строки или данные переменной длины должны быть фактическими указателями, а не смещениями в буфере.</span><span class="sxs-lookup"><span data-stu-id="a0b81-118">Pointers to strings or variable length data must be actual pointers, not offsets into the buffer.</span></span>

<span data-ttu-id="a0b81-119">Если буфер используется для передачи и возврата данных, состоящих только из строк, **параметр DWORD** , указывающий размер буфера, должен быть установлен в общее число символов, которое будет помещаться в эти строки, а не на число байтов.</span><span class="sxs-lookup"><span data-stu-id="a0b81-119">When a buffer is used to pass in and return data that consists only of strings, the **DWORD** specifying the size of the buffer should be set to the total number of characters that will fit in these strings, not to the number of bytes.</span></span>

 

 



