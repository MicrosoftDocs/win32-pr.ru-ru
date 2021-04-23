---
title: Установка поставщика
description: Процедура установки поставщика WMI для DNS отличается в зависимости от версии Windows, в которой он установлен.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Система доменных имен, поставщик WMI, установка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774183"
---
# <a name="installing-the-provider"></a><span data-ttu-id="7f08f-104">Установка поставщика</span><span class="sxs-lookup"><span data-stu-id="7f08f-104">Installing the Provider</span></span>

<span data-ttu-id="7f08f-105">Процедура установки поставщика WMI для DNS отличается в зависимости от версии Windows, в которой он установлен.</span><span class="sxs-lookup"><span data-stu-id="7f08f-105">The procedure for installing the DNS WMI Provider differs based on the version of Windows on which it is installed.</span></span> <span data-ttu-id="7f08f-106">В следующей процедуре описывается установка и настройка поставщика WMI для DNS в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7f08f-106">The following procedure describes how to install and set up the DNS WMI Provider on Windows 2000.</span></span> <span data-ttu-id="7f08f-107">Чтобы получить поставщик WMI для Windows 2000, Скачайте следующий файл:</span><span class="sxs-lookup"><span data-stu-id="7f08f-107">To obtain the DNS WMI Provider for Windows 2000, download the following file:</span></span>

<span data-ttu-id="7f08f-108">**Предупреждение:** Файлы поставщика WMI для DNS не взаимозаменяемы.</span><span class="sxs-lookup"><span data-stu-id="7f08f-108">**WARNING:** DNS WMI Provider files are not interchangeable.</span></span> <span data-ttu-id="7f08f-109">DNS-серверам Windows 2000 требуются разные файлы и процедуры, отличные от DNS-серверов Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7f08f-109">Windows 2000 DNS Servers require different files and a different procedure than Windows Server 2003 DNS Servers.</span></span> <span data-ttu-id="7f08f-110">Процедура для каждого из них предоставляется.</span><span class="sxs-lookup"><span data-stu-id="7f08f-110">The procedure for each is provided.</span></span>

<span data-ttu-id="7f08f-111">**Установка поставщика WMI для DNS на сервере Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="7f08f-111">**To install the DNS WMI Provider on Windows 2000 Server**</span></span>

1.  <span data-ttu-id="7f08f-112">Получите поставщик WMI для Windows 2000 из набора ресурсов Windows 2000 Server Resource Kit или скачайте файл Dnsprov.zip из: ftp://ftp.microsoft.com/reskit/win2000/.</span><span class="sxs-lookup"><span data-stu-id="7f08f-112">Obtain the DNS WMI Provider for Windows 2000 from the Windows 2000 Server Resource Kit, or download the file, Dnsprov.zip, from: ftp://ftp.microsoft.com/reskit/win2000/</span></span>
2.  <span data-ttu-id="7f08f-113">Скопируйте файлы поставщика WMI DNS (Dnsprov.dll) и Днссчема. mof в <winntdir> \\ \\ каталог System32 WBEM.</span><span class="sxs-lookup"><span data-stu-id="7f08f-113">Copy the DNS WMI Provider (Dnsprov.dll) and Dnsschema.mof files to the <winntdir>\\system32\\wbem directory.</span></span>
3.  <span data-ttu-id="7f08f-114">Скомпилируйте MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="7f08f-114">Compile the MOF file.</span></span> <span data-ttu-id="7f08f-115">Это настраивает схему в соответствии с сервером.</span><span class="sxs-lookup"><span data-stu-id="7f08f-115">Doing so customizes the schema to match the server.</span></span>

    <span data-ttu-id="7f08f-116">**mofcomp днссчема. mof**</span><span class="sxs-lookup"><span data-stu-id="7f08f-116">**mofcomp dnsschema.mof**</span></span>

4.  <span data-ttu-id="7f08f-117">Зарегистрируйте библиотеку DLL на DNS-сервере.</span><span class="sxs-lookup"><span data-stu-id="7f08f-117">Register the DLL on the DNS Server.</span></span>

    <span data-ttu-id="7f08f-118">**regsvr32 dnsprov.dll**</span><span class="sxs-lookup"><span data-stu-id="7f08f-118">**regsvr32 dnsprov.dll**</span></span>

5.  <span data-ttu-id="7f08f-119">Затем можно использовать сценарии или программы, которые используют поставщик WMI для управления DNS-серверами.</span><span class="sxs-lookup"><span data-stu-id="7f08f-119">Scripts or programs that use the DNS WMI Provider to manage DNS Servers can then be used.</span></span> <span data-ttu-id="7f08f-120">Сценарии и программы можно запускать с DNS-сервера или с клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="7f08f-120">The scripts or programs can be run from either the DNS Server, or from a client computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="7f08f-121">Пакет SDK для инструментария WMI не требуется для запуска поставщика WMI для DNS, но он содержит множество полезных средств.</span><span class="sxs-lookup"><span data-stu-id="7f08f-121">The WMI SDK is not required to run the DNS WMI Provider, but it contains many useful tools.</span></span>

     

<span data-ttu-id="7f08f-122">Поставщик WMI для DNS должен быть установлен на всех управляемых DNS-серверах. Однако сценарии DNS могут выполняться на DNS-сервере или на удаленном узле.</span><span class="sxs-lookup"><span data-stu-id="7f08f-122">The DNS WMI Provider must be installed on any DNS Server to be managed; the DNS scripts, however, can be run on the DNS Server or on a remote host.</span></span>

<span data-ttu-id="7f08f-123">**Установка поставщика WMI для DNS в Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="7f08f-123">**To install the DNS WMI Provider on Windows Server 2003**</span></span>

-   <span data-ttu-id="7f08f-124">Для операционных систем Windows Server 2003 поставщик WMI DNS устанавливается и регистрируется автоматически, и его MOF-файл компилируется при установке службы DNS-сервера.</span><span class="sxs-lookup"><span data-stu-id="7f08f-124">For Windows Server 2003 operating systems, the DNS WMI Provider is automatically installed and registered, and its MOF file is compiled when the DNS Server service is installed.</span></span>

 

 




