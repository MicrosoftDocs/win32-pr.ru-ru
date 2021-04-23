---
description: Как создать базовое вспомогательное приложение для IP-адресов.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Создание базового вспомогательного приложения IP-адресов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350265"
---
# <a name="creating-a-basic-ip-helper-application"></a><span data-ttu-id="00fcc-103">Создание базового вспомогательного приложения IP-адресов</span><span class="sxs-lookup"><span data-stu-id="00fcc-103">Creating a Basic IP Helper Application</span></span>

<span data-ttu-id="00fcc-104">**Создание базового вспомогательного приложения IP-адресов**</span><span class="sxs-lookup"><span data-stu-id="00fcc-104">**To create a basic IP Helper application**</span></span>

1.  <span data-ttu-id="00fcc-105">Создайте новый пустой проект.</span><span class="sxs-lookup"><span data-stu-id="00fcc-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="00fcc-106">Добавьте пустой исходный файл C++ в проект.</span><span class="sxs-lookup"><span data-stu-id="00fcc-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="00fcc-107">Убедитесь, что среда сборки ссылается на каталоги include, lib и src пакета средств разработки программного обеспечения (SDK) платформы.</span><span class="sxs-lookup"><span data-stu-id="00fcc-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="00fcc-108">Убедитесь, что среда сборки ссылается на файл вспомогательной библиотеки IP-адресов Ифлпапи. lib и файл библиотеки Winsock WS2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="00fcc-108">Ensure that the build environment links to the IP Helper Library file Iphlpapi.lib and the Winsock Library file WS2\_32.lib.</span></span>
    > [!Note]  
    > <span data-ttu-id="00fcc-109">Некоторые основные функции Winsock используются для возврата значений IP-адресов и других сведений.</span><span class="sxs-lookup"><span data-stu-id="00fcc-109">Some basic Winsock functions are used to return IP address values and other information.</span></span>

     

5.  <span data-ttu-id="00fcc-110">Начните программировать вспомогательное приложение IP.</span><span class="sxs-lookup"><span data-stu-id="00fcc-110">Begin programming the IP Helper application.</span></span> <span data-ttu-id="00fcc-111">Используйте API вспомогательной функции IP, включив файл заголовка модуля поддержки IP.</span><span class="sxs-lookup"><span data-stu-id="00fcc-111">Use the IP Helper API by including the IP Helper header file.</span></span>

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="00fcc-112">Файл заголовка *ифлпапи. h* необходим для приложений, использующих вспомогательные функции IP.</span><span class="sxs-lookup"><span data-stu-id="00fcc-112">The *Iphlpapi.h* header file is required for applications that use the IP Helper functions.</span></span> <span data-ttu-id="00fcc-113">Файл заголовка *ифлпапи. h* автоматически включает другие файлы заголовков с структурами и перечислениями, используемыми вспомогательными функциями IP.</span><span class="sxs-lookup"><span data-stu-id="00fcc-113">The *Iphlpapi.h* header file automatically includes other headers files with structures and enumerations used by the IP Helper functions.</span></span>
    >
    > <span data-ttu-id="00fcc-114">Новые вспомогательные функции IP, появившиеся в Windows Vista и более поздних версиях, определены в файле заголовка *нетиоапи. h* , который автоматически включается в заголовочный файл *ифлпапи. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-114">The new IP Helper functions introduced in Windows Vista and later are defined in the *Netioapi.h* header file which is automatically included by the *Iphlpapi.h* header file.</span></span> <span data-ttu-id="00fcc-115">Файл заголовка *нетиоапи. h* никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="00fcc-115">The *Netioapi.h* header file should never be used directly.</span></span>
    >
    > <span data-ttu-id="00fcc-116">Многие структуры и перечисления, используемые вспомогательными функциями IP, определены в файлах заголовков *ипртрмиб. h*, *ипекспорт. h* и *иптипес. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-116">Many of the structures and enumerations used by IP Helper functions are defined in the *Iprtrmib.h*, *Ipexport.h*, and *Iptypes.h* header files.</span></span> <span data-ttu-id="00fcc-117">Эти файлы заголовков автоматически включаются в файл заголовка *ифлпапи. h* и никогда не должны использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="00fcc-117">These header files are automatically included in the *Iphlpapi.h* header file and should never be used directly.</span></span>
    >
    > <span data-ttu-id="00fcc-118">В пакете средств разработки программного обеспечения Microsoft Windows (SDK), выпущенном для Windows Vista и более поздних версий, изменилась Организация файлов заголовков.</span><span class="sxs-lookup"><span data-stu-id="00fcc-118">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed.</span></span> <span data-ttu-id="00fcc-119">Некоторые структуры теперь определены в файлах заголовков *ипмиб. h*, *ткпмиб. h* и *удпмиб. h* , а не в файле заголовка *ипртрмиб. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-119">Some of the structures are now defined in the *Ipmib.h*, *Tcpmib.h*, and *Udpmib.h* header files, not in the *Iprtrmib.h* header file.</span></span> <span data-ttu-id="00fcc-120">Файл заголовка *ипмиб. h* автоматически включает файл заголовка *Ifmib. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-120">The *Ipmib.h* header file automatically includes the *Ifmib.h* header file.</span></span> <span data-ttu-id="00fcc-121">Обратите внимание, что эти файлы заголовков автоматически включаются в *ипртрмиб. h*, который автоматически включается в заголовочный файл *ифлпапи. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-121">Note that these header files are automatically included in *Iprtrmib.h*, which is automatically included in the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="00fcc-122">Для большинства приложений, использующих API-интерфейсы модуля поддержки IP, требуется заголовочный файл *Winsock2. h* для сокетов Windows 2,0.</span><span class="sxs-lookup"><span data-stu-id="00fcc-122">The *Winsock2.h* header file for Windows Sockets 2.0 is required by most applications using the IP Helper APIs.</span></span> <span data-ttu-id="00fcc-123">Если требуется файл заголовка *Winsock2. h* , \# необходимо поместить строку включения для этого файла перед \# строкой include для файла заголовка *ифлпапи. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-123">When the *Winsock2.h* header file is required, the \#include line for this file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="00fcc-124">Заголовочный файл *Winsock2. h* внутренне включает основные элементы из файла заголовков *Windows. h* , поэтому обычно \# в вспомогательных приложениях IP отсутствует строка include для файла заголовка *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-124">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for *Windows.h* header file in IP Helper applications.</span></span> <span data-ttu-id="00fcc-125">Если \# для файла заголовка *Windows. h* требуется строка include, перед ней следует \# указать макрос define Win32 \_ экономичное \_ и \_ среднее.</span><span class="sxs-lookup"><span data-stu-id="00fcc-125">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="00fcc-126">По историческим причинам заголовок *Windows. h* по умолчанию включает в себя файл заголовка *Winsock. h* для сокетов Windows 1,1.</span><span class="sxs-lookup"><span data-stu-id="00fcc-126">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="00fcc-127">Объявления в файле заголовка *Winsock. h* для сокетов Windows 1,1 будут конфликтовать с объявлениями в файле заголовков *Winsock2. h* , который требуется для Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="00fcc-127">The declarations in the *Winsock.h* header file for Windows Sockets 1.1 will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="00fcc-128">\_Макрос экономичного \_ и \_ среднего значения Win32 предотвращает включение заголовочного файла *Winsock. h* в заголовочный файл *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="00fcc-128">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* header file from being included by the *Windows.h* header file.</span></span> <span data-ttu-id="00fcc-129">Пример, иллюстрирующий это, показан ниже.</span><span class="sxs-lookup"><span data-stu-id="00fcc-129">An example illustrating this is shown below.</span></span>

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="00fcc-130">Это базовое вспомогательное приложение IP использует только некоторые структуры данных IP-адресов и IP-адрес для функций преобразования строк из сокетов Windows 2,0.</span><span class="sxs-lookup"><span data-stu-id="00fcc-130">This basic IP Helper application only uses some IP address data structures and IP address to string conversion functions from Windows Sockets 2.0.</span></span> <span data-ttu-id="00fcc-131">Эти функции сокетов Windows можно использовать без вызова [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) для инициализации ресурсов сокетов Windows и [**всаклеануп**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) по завершении использования этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="00fcc-131">These Windows Sockets functions can be used without calling [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) to initialize Windows Sockets resources and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) when done using these resources.</span></span>
    >
    > <span data-ttu-id="00fcc-132">В вспомогательных приложениях IP, использующих другие функции Winsock, отличные от этих IP-адресов, для строковых функций необходимо вызвать функцию [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) , чтобы инициализировать ресурсы сокетов Windows, прежде чем вызывать функции сокетов Windows и [**всаклеануп**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) при завершении работы приложения с помощью ресурсов сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="00fcc-132">In IP Helper applications that use other Winsock functions other than these IP address to string functions, the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function must be called to initialize Windows Sockets resources before calling any Windows Sockets functions and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) should be called when the application is done using Windows Sockets resources.</span></span>

     

    > [!Note]
    >
    > <span data-ttu-id="00fcc-133">Файл заголовка *stdio. h* необходим для использования различных стандартных функций C в этом базовом вспомогательном приложении IP.</span><span class="sxs-lookup"><span data-stu-id="00fcc-133">The *Stdio.h* header file is required for the use of various standard C functions in this basic IP Helper application.</span></span>

     

    <span data-ttu-id="00fcc-134">Следующий шаг: [Получение сведений с помощью жетнетворкпарамс](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="00fcc-134">Next Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 
