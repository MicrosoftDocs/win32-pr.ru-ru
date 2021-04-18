---
description: Обработка ошибок в Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Обработка ошибок Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701520"
---
# <a name="handling-winsock-errors"></a><span data-ttu-id="f595f-103">Обработка ошибок Winsock</span><span class="sxs-lookup"><span data-stu-id="f595f-103">Handling Winsock Errors</span></span>

<span data-ttu-id="f595f-104">Большинство функций Windows Sockets 2 не возвращают конкретную причину ошибки, когда функция возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f595f-104">Most Windows Sockets 2 functions do not return the specific cause of an error when the function returns.</span></span> <span data-ttu-id="f595f-105">Некоторые функции Winsock возвращают нулевое значение в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="f595f-105">Some Winsock functions return a value of zero if successful.</span></span> <span data-ttu-id="f595f-106">В противном случае \_ возвращается ошибка сокета (-1), и можно получить конкретный номер ошибки, вызвав функцию [**всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f595f-106">Otherwise, the value SOCKET\_ERROR (-1) is returned and a specific error number can be retrieved by calling the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function.</span></span> <span data-ttu-id="f595f-107">Для функций Winsock, возвращающих маркер, возвращаемое значение НЕДОПУСТИМого \_ сокета (0xFFFF) указывает на ошибку, и конкретный номер ошибки может быть получен путем вызова **всажетластеррор**.</span><span class="sxs-lookup"><span data-stu-id="f595f-107">For Winsock functions that return a handle, a return value of INVALID\_SOCKET (0xffff) indicates an error and a specific error number can be retrieved by calling **WSAGetLastError**.</span></span> <span data-ttu-id="f595f-108">Для функций Winsock, возвращающих указатель, возвращаемое значение **null** указывает на ошибку, а конкретный номер ошибки можно получить, вызвав функцию **всажетластеррор** .</span><span class="sxs-lookup"><span data-stu-id="f595f-108">For Winsock functions that return a pointer, a return value of **NULL** indicates an error and a specific error number can be retrieved by calling the **WSAGetLastError** function.</span></span>

<span data-ttu-id="f595f-109">Код ошибки Winsock можно преобразовать в HRESULT для использования в удаленном вызове процедур (RPC) с помощью HRESULT \_ из \_ Win32.</span><span class="sxs-lookup"><span data-stu-id="f595f-109">A Winsock error code can be converted to an HRESULT for use in a remote procedure call (RPC) using HRESULT\_FROM\_WIN32.</span></span> <span data-ttu-id="f595f-110">В более ранних версиях пакета средств разработки программного обеспечения (SDK) HRESULT \_ из \_ Win32 был определен как макрос в файле заголовка *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="f595f-110">In earlier versions of the Platform Software Development Kit (SDK), HRESULT\_FROM\_WIN32 was defined as a macro in the *Winerror.h* header file.</span></span> <span data-ttu-id="f595f-111">В пакете средств разработки программного обеспечения (SDK) для Microsoft Windows HRESULT \_ из \_ Win32 определяется как встроенная функция в файле заголовка *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="f595f-111">In the Microsoft Windows Software Development Kit (SDK), HRESULT\_FROM\_WIN32 is defined as an inline function in the *Winerror.h* header file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f595f-112">См. также</span><span class="sxs-lookup"><span data-stu-id="f595f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f595f-113">Коды ошибок сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="f595f-113">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



