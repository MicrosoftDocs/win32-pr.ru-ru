---
title: использование командлетов WMI Windows PowerShell для управления облегченным сервером BITS
description: Windows PowerShell предоставляет простой механизм подключения к инструментарий управления Windows (WMI) (WMI) на удаленном компьютере и управления сервером фоновая интеллектуальная служба передачи (BITS) Compact Server.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e82401e80b5e49b7d2b964ec910d15d70aea7ce9c782a0173bef97aa8b3a5c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021082"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a>использование командлетов WMI Windows PowerShell для управления облегченным сервером BITS

Windows PowerShell предоставляет простой механизм подключения к инструментарий управления Windows (WMI) (WMI) на удаленном компьютере и управления сервером фоновая интеллектуальная служба передачи (BITS) Compact Server. Облегченный сервер BITS — это необязательный серверный компонент, который необходимо установить отдельно. Сведения об установке Compact Server см. в документации по [облегченному серверу BITS](bits-compact-server.md) .

1.  Подключение поставщику BITS.

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    Командлет [Get-Credential](/previous-versions//dd315327(v=technet.10)) запрашивает учетные данные пользователя для подключения к удаленному компьютеру и назначает учетные данные объекту $cred.

    Объекты, возвращаемые командлетом [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) , присваиваются переменной $BCS. В предыдущем примере командлет [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) получает класс [битскомпактсерверурлграуп](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) в корневом \\ \\ пространстве имен Microsoft BITS для Server1. Статические методы, предоставляемые классом [битскомпактсерверурлграуп](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) , можно вызывать для объекта $BCS. Дополнительные сведения об удаленном управлении BITS см. в разделе классы поставщиков службы [BITS](/previous-versions/windows/desktop/bitsprov/bits-provider) и поставщика [BITS]( /previous-versions//dd904507(v=vs.85)).

    > [!Note]  
    > Знак ударения-ударения ( \` ) используется для обозначения разрыва строки.

     

2.  Создайте группу URL-адресов на сервере.

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    https://Server1:80/testurlgroupПеременной $URLGroup присваивается строка префикса URL-адреса. Переменная $URLGroup передается методу [креатеурлграуп](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , который создает группу URL-адресов на сервере Server1.

    Можно указать другую группу URL-адресов. Группа URL-адресов должна соответствовать допустимой строке префикса URL-адреса. Дополнительные сведения об префиксах URL-адресов см. в разделе [UrlPrefix strings](../http/urlprefix-strings.md).

3.  Размещение файла в группе URL-адресов.

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    Экземпляр Битскомпактсерверурлграуп, возвращенный командлетом [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) , назначается переменной $bcsObj. Метод [креатеурл](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) вызывается для $bcsObj с суффиксом URL-адреса "url.txt", \\ \\ исходным путем "c: temp \\ \\1.txt" для файла и пустой строкой дескриптора безопасности в качестве параметров. Суффикс "url.txt" добавляется в префикс группы URL-адресов. Клиенты могут скачать файл по следующему адресу: https://Server1:80/testurlgroup/url.txt .

4.  Очистите URL-адрес и группу URL-адресов.

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    Метод **удаления System. Object** удаляет объект $bcsObj.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Облегченный сервер BITS](./bits-compact-server.md)
</dt> <dt>

[Поставщик BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

[Классы поставщиков BITS]( /previous-versions//dd904507(v=vs.85))
</dt> <dt>

[Get-Credential](/previous-versions//dd315327(v=technet.10))
</dt> <dt>

[Get-WmiObject](/previous-versions//dd315295(v=technet.10))
</dt> </dl>

 

 