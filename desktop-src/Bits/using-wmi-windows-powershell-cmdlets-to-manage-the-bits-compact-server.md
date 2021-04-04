---
title: Использование командлетов WMI Windows PowerShell для управления облегченным сервером BITS
description: Windows PowerShell предоставляет простой механизм подключения к инструментарий управления Windows (WMI) (WMI) на удаленном компьютере и управления фоновая интеллектуальная служба передачи (BITS) Compact Server.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987679"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a><span data-ttu-id="df6e8-103">Использование командлетов WMI Windows PowerShell для управления облегченным сервером BITS</span><span class="sxs-lookup"><span data-stu-id="df6e8-103">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>

<span data-ttu-id="df6e8-104">Windows PowerShell предоставляет простой механизм подключения к инструментарий управления Windows (WMI) (WMI) на удаленном компьютере и управления фоновая интеллектуальная служба передачи (BITS) Compact Server.</span><span class="sxs-lookup"><span data-stu-id="df6e8-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer and manage the Background Intelligent Transfer Service (BITS) Compact Server.</span></span> <span data-ttu-id="df6e8-105">Облегченный сервер BITS — это необязательный серверный компонент, который необходимо установить отдельно.</span><span class="sxs-lookup"><span data-stu-id="df6e8-105">The BITS Compact Server is an optional server component that must be installed separately.</span></span> <span data-ttu-id="df6e8-106">Сведения об установке Compact Server см. в документации по [облегченному серверу BITS](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="df6e8-106">For information about installing the Compact Server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="df6e8-107">Подключитесь к поставщику BITS.</span><span class="sxs-lookup"><span data-stu-id="df6e8-107">Connect to the BITS provider.</span></span>

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="df6e8-108">Командлет [Get-Credential](/previous-versions//dd315327(v=technet.10)) запрашивает учетные данные пользователя для подключения к удаленному компьютеру и назначает учетные данные объекту $cred.</span><span class="sxs-lookup"><span data-stu-id="df6e8-108">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="df6e8-109">Объекты, возвращаемые командлетом [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) , присваиваются переменной $BCS.</span><span class="sxs-lookup"><span data-stu-id="df6e8-109">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet are assigned to the $bcs variable.</span></span> <span data-ttu-id="df6e8-110">В предыдущем примере командлет [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) получает класс [битскомпактсерверурлграуп](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) в корневом \\ \\ пространстве имен Microsoft BITS для Server1.</span><span class="sxs-lookup"><span data-stu-id="df6e8-110">In the preceding example, the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet retrieves the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class in the root\\Microsoft\\BITS namespace of Server1.</span></span> <span data-ttu-id="df6e8-111">Статические методы, предоставляемые классом [битскомпактсерверурлграуп](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) , можно вызывать для объекта $BCS.</span><span class="sxs-lookup"><span data-stu-id="df6e8-111">Static methods exposed by the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class can be called on the $bcs object.</span></span> <span data-ttu-id="df6e8-112">Дополнительные сведения об удаленном управлении BITS см. в разделе классы поставщиков службы [BITS](/previous-versions/windows/desktop/bitsprov/bits-provider) и поставщика [BITS]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df6e8-112">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

    > [!Note]  
    > <span data-ttu-id="df6e8-113">Знак ударения-ударения ( \` ) используется для обозначения разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="df6e8-113">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="df6e8-114">Создайте группу URL-адресов на сервере.</span><span class="sxs-lookup"><span data-stu-id="df6e8-114">Create a URL group on the server.</span></span>

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    <span data-ttu-id="df6e8-115"> https://Server1:80/testurlgroupПеременной $URLGroup присваивается строка префикса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="df6e8-115">The "https://Server1:80/testurlgroup" URL prefix string is assigned to the $URLGroup variable.</span></span> <span data-ttu-id="df6e8-116">Переменная $URLGroup передается методу [креатеурлграуп](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , который создает группу URL-адресов на сервере Server1.</span><span class="sxs-lookup"><span data-stu-id="df6e8-116">The $URLGroup variable is passed to the [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) method, which creates the URL group on Server1.</span></span>

    <span data-ttu-id="df6e8-117">Можно указать другую группу URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="df6e8-117">You can specify a different URL group.</span></span> <span data-ttu-id="df6e8-118">Группа URL-адресов должна соответствовать допустимой строке префикса URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="df6e8-118">The URL group must conform to a valid URL prefix string.</span></span> <span data-ttu-id="df6e8-119">Дополнительные сведения об префиксах URL-адресов см. в разделе [UrlPrefix strings](../http/urlprefix-strings.md).</span><span class="sxs-lookup"><span data-stu-id="df6e8-119">For more information about URL prefixes, see [UrlPrefix Strings](../http/urlprefix-strings.md).</span></span>

3.  <span data-ttu-id="df6e8-120">Размещение файла в группе URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="df6e8-120">Host a file on the URL group.</span></span>

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="df6e8-121">Экземпляр Битскомпактсерверурлграуп, возвращенный командлетом [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) , назначается переменной $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="df6e8-121">The BITSCompactServerUrlGroup instance returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet is assigned to the $bcsObj variable.</span></span> <span data-ttu-id="df6e8-122">Метод [креатеурл](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) вызывается для $bcsObj с суффиксом URL-адреса "url.txt", \\ \\ исходным путем "c: temp \\ \\1.txt" для файла и пустой строкой дескриптора безопасности в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="df6e8-122">The [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) method is called for the $bcsObj with the "url.txt" URL suffix, the "c:\\\\temp\\\\1.txt" source path for the file, and an empty security descriptor string as parameters.</span></span> <span data-ttu-id="df6e8-123">Суффикс "url.txt" добавляется в префикс группы URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="df6e8-123">The "url.txt" suffix is added to the URL group prefix.</span></span> <span data-ttu-id="df6e8-124">Клиенты могут скачать файл по следующему адресу: https://Server1:80/testurlgroup/url.txt .</span><span class="sxs-lookup"><span data-stu-id="df6e8-124">Clients can download the file from the following address: https://Server1:80/testurlgroup/url.txt.</span></span>

4.  <span data-ttu-id="df6e8-125">Очистите URL-адрес и группу URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="df6e8-125">Clean up the URL and the URL group.</span></span>

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    <span data-ttu-id="df6e8-126">Метод **удаления System. Object** удаляет объект $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="df6e8-126">The **system.object Delete** method deletes the $bcsObj object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df6e8-127">См. также</span><span class="sxs-lookup"><span data-stu-id="df6e8-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df6e8-128">Облегченный сервер BITS</span><span class="sxs-lookup"><span data-stu-id="df6e8-128">BITS Compact Server</span></span>](./bits-compact-server.md)
</dt> <dt>

[<span data-ttu-id="df6e8-129">Поставщик BITS</span><span class="sxs-lookup"><span data-stu-id="df6e8-129">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

<span data-ttu-id="df6e8-130">[Классы поставщиков BITS]( /previous-versions//dd904507(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df6e8-130">[BITS provider classes]( /previous-versions//dd904507(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="df6e8-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="df6e8-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="df6e8-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="df6e8-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span></span>
</dt> </dl>

 

 