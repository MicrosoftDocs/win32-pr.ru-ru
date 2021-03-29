---
title: Изменение объекта ADSI из ADO
description: ADSI для Windows 2000 и клиент DS включают в себя поставщик OLE DB только для чтения. Это означает, что вы не можете в настоящее время выполнить инструкцию UPDATE в диалекте SQL.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Изменение объекта ADSI из ADO ADSI
- Интерфейс ADSI объектов данных ActiveX, изменение объекта ADSI из ADO
- ADSI ADSI, пример кода C/C++, изменение объекта ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772944"
---
# <a name="modifying-an-adsi-object-from-ado"></a><span data-ttu-id="768df-107">Изменение объекта ADSI из ADO</span><span class="sxs-lookup"><span data-stu-id="768df-107">Modifying an ADSI Object from ADO</span></span>

<span data-ttu-id="768df-108">ADSI для Windows 2000 и клиент DS включают в себя поставщик OLE DB только для чтения.</span><span class="sxs-lookup"><span data-stu-id="768df-108">ADSI for Windows 2000 and DS Client includes a read-only OLE DB provider.</span></span> <span data-ttu-id="768df-109">Это означает, что вы не можете в настоящее время выполнить инструкцию UPDATE в диалекте SQL.</span><span class="sxs-lookup"><span data-stu-id="768df-109">This means that you cannot, at present, issue the UPDATE statement in the SQL dialect.</span></span>

<span data-ttu-id="768df-110">**Изменение объекта, возвращаемого запросом ADO**</span><span class="sxs-lookup"><span data-stu-id="768df-110">**To modify an object returned from an ADO query**</span></span>

1.  <span data-ttu-id="768df-111">Запросите значение **ADsPath** при указании имени атрибута, как в «SELECT ADsPath,...».</span><span class="sxs-lookup"><span data-stu-id="768df-111">Request the **ADsPath** when specifying an attribute name, as in "SELECT ADsPath, ..."</span></span>
2.  <span data-ttu-id="768df-112">Выполните запрос и получите атрибут **ADsPath** .</span><span class="sxs-lookup"><span data-stu-id="768df-112">Execute the query and get the **ADsPath** attribute.</span></span>
3.  <span data-ttu-id="768df-113">Выполните привязку к набору записей с помощью **ADsPath** и измените атрибуты.</span><span class="sxs-lookup"><span data-stu-id="768df-113">Bind to the record set using **ADsPath**, and modify the attributes.</span></span>

<span data-ttu-id="768df-114">В следующем примере кода показано, как изменить объект ADSI после выполнения шагов, описанных в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="768df-114">The following code example shows how to modify an ADSI object after performing the steps outlined in the preceding example.</span></span>


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




