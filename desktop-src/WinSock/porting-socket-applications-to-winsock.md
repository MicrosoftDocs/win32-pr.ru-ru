---
description: В этом разделе описаны рекомендации по переносу Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Перенос приложений сокета в Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711021"
---
# <a name="porting-socket-applications-to-winsock"></a><span data-ttu-id="516a1-103">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="516a1-103">Porting Socket Applications to Winsock</span></span>

<span data-ttu-id="516a1-104">В этом разделе описаны рекомендации по переносу Winsock.</span><span class="sxs-lookup"><span data-stu-id="516a1-104">This section describes Winsock porting considerations.</span></span>

<span data-ttu-id="516a1-105">Существует ограниченное количество случаев, когда сокеты Windows переносят строгое соответствие соглашениям Berkeley, обычно из-за проблем с реализацией в среде Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="516a1-105">There are a limited number of instances where Windows Sockets has diverted from strict adherence to the Berkeley conventions, usually due to implementation difficulties in the Microsoft Windows environment.</span></span>

<span data-ttu-id="516a1-106">Если в сокетах Windows происходит отклонение от соглашений Berkeley, то отклонения заменяются специально и четко.</span><span class="sxs-lookup"><span data-stu-id="516a1-106">When a deviation from Berkeley conventions occurs in Windows Sockets, the deviation is specifically and clearly noted.</span></span> <span data-ttu-id="516a1-107">Например, если функция относится к сокетам Windows, это отклонение указывается с помощью фразы в описании функции, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="516a1-107">For example, if a function is specific to Windows Sockets, that deviation is specified with a phrase in the function description similar to the following:</span></span>

<span data-ttu-id="516a1-108">Функция **\[ имени \]** функции — это расширение для API Windows Sockets 2, относящееся к корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="516a1-108">The **\[function-name\]** function is a Microsoft-specific extension to the Windows Sockets 2 API.</span></span>

<span data-ttu-id="516a1-109">В этом разделе содержатся сведения о переносе приложений сокетов UNIX (BSD) в Winsock:</span><span class="sxs-lookup"><span data-stu-id="516a1-109">This section provides information about porting Berkeley (BSD) UNIX socket applications to Winsock:</span></span>

-   [<span data-ttu-id="516a1-110">Тип данных сокета</span><span class="sxs-lookup"><span data-stu-id="516a1-110">Socket Data Type</span></span>](socket-data-type-2.md)
-   [<span data-ttu-id="516a1-111">Макросы SELECT, ДЕМОна \_ Set и демона \_ xxx</span><span class="sxs-lookup"><span data-stu-id="516a1-111">Select, FD\_SET, and FD\_XXX Macros</span></span>](select-and-fd---2.md)
-   [<span data-ttu-id="516a1-112">Коды ошибок — код возврата, h \_ и всажетластеррор</span><span class="sxs-lookup"><span data-stu-id="516a1-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [<span data-ttu-id="516a1-113">Указатели</span><span class="sxs-lookup"><span data-stu-id="516a1-113">Pointers</span></span>](pointers-2.md)
-   [<span data-ttu-id="516a1-114">Переименованные функции</span><span class="sxs-lookup"><span data-stu-id="516a1-114">Renamed Functions</span></span>](renamed-functions-2.md)
-   [<span data-ttu-id="516a1-115">Максимальное число поддерживаемых сокетов</span><span class="sxs-lookup"><span data-stu-id="516a1-115">Maximum Number of Sockets Supported</span></span>](maximum-number-of-sockets-supported-2.md)
-   [<span data-ttu-id="516a1-116">Включаемые файлы</span><span class="sxs-lookup"><span data-stu-id="516a1-116">Include Files</span></span>](include-files-2.md)
-   [<span data-ttu-id="516a1-117">Возвращаемые значения при сбое функции</span><span class="sxs-lookup"><span data-stu-id="516a1-117">Return Values on Function Failure</span></span>](return-values-on-function-failure-2.md)
-   [<span data-ttu-id="516a1-118">Необработанные сокеты</span><span class="sxs-lookup"><span data-stu-id="516a1-118">Raw Sockets</span></span>](service-provided-raw-sockets-2.md)
-   [<span data-ttu-id="516a1-119">Порядок байтов</span><span class="sxs-lookup"><span data-stu-id="516a1-119">Byte Ordering</span></span>](byte-ordering-2.md)
-   [<span data-ttu-id="516a1-120">Расширенные подпрограммы преобразования Byte-Order</span><span class="sxs-lookup"><span data-stu-id="516a1-120">Extended Byte-Order Conversion Routines</span></span>](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a><span data-ttu-id="516a1-121">См. также</span><span class="sxs-lookup"><span data-stu-id="516a1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="516a1-122">Обработка ошибок Winsock</span><span class="sxs-lookup"><span data-stu-id="516a1-122">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="516a1-123">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="516a1-123">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="516a1-124">Коды ошибок сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="516a1-124">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="516a1-125">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="516a1-125">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



