---
title: начало работы со сценариями для ADSI
description: Сценарии удобно использовать для системных администраторов, желающих создавать пакетные скрипты для часто используемых задач.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- начало работы со сценариями для ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a85a9ea110ca80f45c3a0f0f1917e8d25c08ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986101"
---
# <a name="getting-started-with-scripting-for-adsi"></a><span data-ttu-id="7dfa0-104">начало работы со сценариями для ADSI</span><span class="sxs-lookup"><span data-stu-id="7dfa0-104">Getting Started with Scripting for ADSI</span></span>

<span data-ttu-id="7dfa0-105">Сценарии удобно использовать для системных администраторов, желающих создавать пакетные скрипты для часто используемых задач.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-105">Scripting is useful for system administrators who want to create batch scripts for frequently used tasks.</span></span>

<span data-ttu-id="7dfa0-106">Для запуска сценариев с помощью ADSI необходимо иметь компьютер под управлением Windows или войти в домен, содержащий данные для учетных записей компьютеров в каталоге.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-106">To start scripting with ADSI, you must have a computer that runs Windows or be logged on to a domain that contains data for computer accounts in the directory.</span></span>

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a><span data-ttu-id="7dfa0-107">Простой пример создания сценариев: Поиск имен и расположения учетных записей компьютеров</span><span class="sxs-lookup"><span data-stu-id="7dfa0-107">A Simple Scripting Sample: Finding Names and Locations of Computer Accounts</span></span>

<span data-ttu-id="7dfa0-108">Создайте новый текстовый файл с помощью текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-108">Create a new text file using a text editor.</span></span> <span data-ttu-id="7dfa0-109">В следующем примере кода показано, как найти имена и расположения учетных записей компьютеров.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-109">The following code example shows how to find names and locations of computer accounts.</span></span>


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



<span data-ttu-id="7dfa0-110">Сохраните файл как First.vbs.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-110">Save the file as First.vbs.</span></span> <span data-ttu-id="7dfa0-111">Измените строку, которая начинается с "Обжкомманд. CommandText", чтобы изменить путь к домену.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-111">Modify the line that begins with "objCommand.CommandText" to change the path to your domain.</span></span> <span data-ttu-id="7dfa0-112">В командной строке введите **cscript First.vbs** для командной строки или First.vbs для сценариев Windows.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-112">At the command prompt, type **cscript First.vbs** for a command line or First.vbs for Windows scripting.</span></span> <span data-ttu-id="7dfa0-113">Результаты должны возвращаться в командной строке.</span><span class="sxs-lookup"><span data-stu-id="7dfa0-113">The results should be returned in the command prompt.</span></span>

<span data-ttu-id="7dfa0-114">Дополнительные сведения о скриптах для ADSI см. в разделе [Active Directorying Service Interfaces Scripting](adsi-scripting-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="7dfa0-114">For more information about scripting for ADSI, see [Active Directory Service Interfaces Scripting](adsi-scripting-tutorial.md).</span></span>

 

 




