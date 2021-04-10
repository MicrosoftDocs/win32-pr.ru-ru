---
description: Как создать базовое приложение Windows Sockets (Winsock).
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Создание базового приложения Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145088"
---
# <a name="creating-a-basic-winsock-application"></a><span data-ttu-id="61986-103">Создание базового приложения Winsock</span><span class="sxs-lookup"><span data-stu-id="61986-103">Creating a Basic Winsock Application</span></span>

<span data-ttu-id="61986-104">**Создание базового приложения Winsock**</span><span class="sxs-lookup"><span data-stu-id="61986-104">**To create a basic Winsock application**</span></span>

1.  <span data-ttu-id="61986-105">Создайте новый пустой проект.</span><span class="sxs-lookup"><span data-stu-id="61986-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="61986-106">Добавьте пустой исходный файл C++ в проект.</span><span class="sxs-lookup"><span data-stu-id="61986-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="61986-107">Убедитесь, что среда сборки относится к каталогам include, lib и src пакета средств разработки программного обеспечения (SDK) для Microsoft Windows или пакета SDK более ранней платформы.</span><span class="sxs-lookup"><span data-stu-id="61986-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Microsoft Windows Software Development Kit (SDK) or the earlier Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="61986-108">Убедитесь, что среда сборки ссылается на файл библиотеки Winsock Ws2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="61986-108">Ensure that the build environment links to the Winsock Library file Ws2\_32.lib.</span></span> <span data-ttu-id="61986-109">Приложения, использующие Winsock, должны быть связаны с \_ файлом библиотеки Ws2 32. lib.</span><span class="sxs-lookup"><span data-stu-id="61986-109">Applications that use Winsock must be linked with the Ws2\_32.lib library file.</span></span> <span data-ttu-id="61986-110">\#Комментарий директивы pragma указывает компоновщику, что требуется файл *Ws2 \_ 32. lib* .</span><span class="sxs-lookup"><span data-stu-id="61986-110">The \#pragma comment indicates to the linker that the *Ws2\_32.lib* file is needed.</span></span>
5.  <span data-ttu-id="61986-111">Начните программировать приложение Winsock.</span><span class="sxs-lookup"><span data-stu-id="61986-111">Begin programming the Winsock application.</span></span> <span data-ttu-id="61986-112">Используйте API Winsock, включив файлы заголовков Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="61986-112">Use the Winsock API by including the Winsock 2 header files.</span></span> <span data-ttu-id="61986-113">Файл заголовка *Winsock2. h* содержит большинство функций, структур и определений Winsock.</span><span class="sxs-lookup"><span data-stu-id="61986-113">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="61986-114">Файл заголовка *Ws2tcpip. h* содержит определения, появившиеся в документе о приложении WinSock 2 Protocol-Specific для TCP/IP, который включает более новые функции и структуры, используемые для получения IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="61986-114">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span>
    > [!Note]  
    > <span data-ttu-id="61986-115">Stdio. h используется для стандартных входных и выходных данных, особенно для функции **printf ()** .</span><span class="sxs-lookup"><span data-stu-id="61986-115">Stdio.h is used for standard input and output, specifically the **printf()** function.</span></span>

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> <span data-ttu-id="61986-116">Файл заголовка *ифлпапи. h* необходим, если приложение использует API-интерфейсы вспомогательного приложения IP.</span><span class="sxs-lookup"><span data-stu-id="61986-116">The *Iphlpapi.h* header file is required if an application is using the IP Helper APIs.</span></span> <span data-ttu-id="61986-117">Если требуется файл заголовка *ифлпапи. h* , \# необходимо поместить строку include для заголовочного файла *Winsock2. h* перед \# строкой include для заголовочного файла *ифлпапи. h* .</span><span class="sxs-lookup"><span data-stu-id="61986-117">When the *Iphlpapi.h* header file is required, the \#include line for the *Winsock2.h* header file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
>
> <span data-ttu-id="61986-118">Заголовочный файл *Winsock2. h* внутренне включает основные элементы из файла заголовков *Windows. h* , поэтому \# в приложениях Winsock обычно отсутствует строка include для файла заголовка *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="61986-118">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="61986-119">Если \# для файла заголовка *Windows. h* требуется строка include, перед ней следует \# указать макрос define Win32 \_ экономичное \_ и \_ среднее.</span><span class="sxs-lookup"><span data-stu-id="61986-119">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="61986-120">По историческим причинам заголовок *Windows. h* по умолчанию включает в себя файл заголовка *Winsock. h* для сокетов Windows 1,1.</span><span class="sxs-lookup"><span data-stu-id="61986-120">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="61986-121">Объявления в файле заголовка *Winsock. h* конфликтуют с объявлениями в файле заголовка *Winsock2. h* , который требуется для сокетов Windows 2,0.</span><span class="sxs-lookup"><span data-stu-id="61986-121">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="61986-122">\_Макрос экономичного \_ и \_ среднего значения Win32 предотвращает включение *библиотеки Winsock. h* в заголовок *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="61986-122">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="61986-123">Пример, иллюстрирующий это, показан ниже.</span><span class="sxs-lookup"><span data-stu-id="61986-123">An example illustrating this is shown below.</span></span>

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



<span data-ttu-id="61986-124">Следующий шаг: [Инициализация Winsock](initializing-winsock.md)</span><span class="sxs-lookup"><span data-stu-id="61986-124">Next Step: [Initializing Winsock](initializing-winsock.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="61986-125">См. также</span><span class="sxs-lookup"><span data-stu-id="61986-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61986-126">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="61986-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="61986-127">О серверах и клиентах</span><span class="sxs-lookup"><span data-stu-id="61986-127">About Servers and Clients</span></span>](about-clients-and-servers.md)
</dt> </dl>

 

 



