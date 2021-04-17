---
description: Максимальное число сокетов, поддерживаемое определенным поставщиком службы Windows Sockets, зависит от реализации.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Максимальное число поддерживаемых сокетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711024"
---
# <a name="maximum-number-of-sockets-supported"></a><span data-ttu-id="07da1-103">Максимальное число поддерживаемых сокетов</span><span class="sxs-lookup"><span data-stu-id="07da1-103">Maximum Number of Sockets Supported</span></span>

<span data-ttu-id="07da1-104">Максимальное число сокетов, поддерживаемое определенным поставщиком службы Windows Sockets, зависит от реализации.</span><span class="sxs-lookup"><span data-stu-id="07da1-104">The maximum number of sockets supported by a particular Windows Sockets service provider is implementation specific.</span></span> <span data-ttu-id="07da1-105">Поставщик Microsoft WinSock ограничивает максимальное количество сокетов, поддерживаемое только объемом доступной памяти на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="07da1-105">The Microsoft Winsock provider limits the maximum number of sockets supported only by available memory on the local computer.</span></span> <span data-ttu-id="07da1-106">Однако сторонние поставщики Winsock могут иметь ограничения на число поддерживаемых сокетов.</span><span class="sxs-lookup"><span data-stu-id="07da1-106">However, third-party Winsock providers may have limitations on the numbers of sockets supported.</span></span> <span data-ttu-id="07da1-107">Приложение не должно делать никаких предположений о доступности определенного числа сокетов.</span><span class="sxs-lookup"><span data-stu-id="07da1-107">An application should make no assumptions about the availability of a certain number of sockets.</span></span> <span data-ttu-id="07da1-108">Дополнительные сведения об этом разделе см. в разделе [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span><span class="sxs-lookup"><span data-stu-id="07da1-108">For more information on this topic see [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span></span>

## <a name="fd_set-and-select"></a><span data-ttu-id="07da1-109">Демон \_ установки и выбор</span><span class="sxs-lookup"><span data-stu-id="07da1-109">FD\_SET and select</span></span>

<span data-ttu-id="07da1-110">В \_ файле заголовков *Winsock2. h* определено несколько макросов, которые можно использовать для переноса приложений в Windows из среды UNIX.</span><span class="sxs-lookup"><span data-stu-id="07da1-110">A number of FD\_XXX macros are defined in the *Winsock2.h* header file for use in porting applications to Windows from the UNIX environment.</span></span> <span data-ttu-id="07da1-111">Эти макросы используются с функциями [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) и [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) для переноса приложений в Windows.</span><span class="sxs-lookup"><span data-stu-id="07da1-111">These macros are used with the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) and [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions for porting applications to Windows.</span></span> <span data-ttu-id="07da1-112">Максимальное число сокетов, которое может использовать приложение Windows Sockets, не зависит от значения константы манифеста \_ .</span><span class="sxs-lookup"><span data-stu-id="07da1-112">The maximum number of sockets that a Windows Sockets application can use is not affected by the manifest constant FD\_SETSIZE.</span></span> <span data-ttu-id="07da1-113">Это значение, определенное в файле заголовка *Winsock2. h* , используется для конструирования структур [**\_ набора**](/windows/desktop/api/winsock/nf-winsock-fd_set) , используемых с функцией **SELECT** .</span><span class="sxs-lookup"><span data-stu-id="07da1-113">This value defined in the *Winsock2.h* header file is used in constructing the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures used with **select** function.</span></span> <span data-ttu-id="07da1-114">Значение по умолчанию в Winsock2. h — 64.</span><span class="sxs-lookup"><span data-stu-id="07da1-114">The default value in Winsock2.h is 64.</span></span> <span data-ttu-id="07da1-115">Если приложение предназначено для работы с более чем 64 сокетами с помощью функций **SELECT** и **всаполл** , то разработчик должен определить создаваемый манифест \_ в каждом исходном файле перед включением файла заголовка *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="07da1-115">If an application is designed to be capable of working with more than 64 sockets using the **select** and **WSAPoll** functions, the implementor should define the manifest FD\_SETSIZE in every source file before including the *Winsock2.h* header file.</span></span> <span data-ttu-id="07da1-116">Одним из способов это может быть включение определения в параметры компилятора в файле Makefile.</span><span class="sxs-lookup"><span data-stu-id="07da1-116">One way of doing this may be to include the definition within the compiler options in the makefile.</span></span> <span data-ttu-id="07da1-117">Например, можно добавить "-DFD \_ SETSIZE = 128" в качестве параметра командной строки компилятора для Microsoft C++.</span><span class="sxs-lookup"><span data-stu-id="07da1-117">For example, you could add "-DFD\_SETSIZE=128" as an option to the compiler command line for Microsoft C++.</span></span> <span data-ttu-id="07da1-118">Необходимо подчеркнуть, что определение «\ \ \ \ \ "\ \ \_ "» не влияет на фактическое число сокетов, предоставляемых поставщиком услуг Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="07da1-118">It must be emphasized that defining FD\_SETSIZE as a particular value has no effect on the actual number of sockets provided by a Windows Sockets service provider.</span></span> <span data-ttu-id="07da1-119">Это значение влияет только на макросы "ДЕМОна XXX", \_ используемые функциями **SELECT** и **всаполл** .</span><span class="sxs-lookup"><span data-stu-id="07da1-119">This value only affects the FD\_XXX macros used by the **select** and **WSAPoll** functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07da1-120">См. также</span><span class="sxs-lookup"><span data-stu-id="07da1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07da1-121">**Установка ДЕМОна \_**</span><span class="sxs-lookup"><span data-stu-id="07da1-121">**FD\_SET**</span></span>](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[<span data-ttu-id="07da1-122">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="07da1-122">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="07da1-123">**метьте**</span><span class="sxs-lookup"><span data-stu-id="07da1-123">**select**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[<span data-ttu-id="07da1-124">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="07da1-124">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="07da1-125">**Сбой WSAStartup**</span><span class="sxs-lookup"><span data-stu-id="07da1-125">**WSAStartup**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[<span data-ttu-id="07da1-126">**всаполл**</span><span class="sxs-lookup"><span data-stu-id="07da1-126">**WSAPoll**</span></span>](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
