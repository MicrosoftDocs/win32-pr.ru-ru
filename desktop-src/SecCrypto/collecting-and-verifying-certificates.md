---
description: В следующем примере сертификаты в локальном хранилище перечисляются и проверяются на допустимость.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Сбор и проверка сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0b160f373d5ade65679fcc4dd87e3c1c86dc4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683162"
---
# <a name="collecting-and-verifying-certificates"></a><span data-ttu-id="d6a70-103">Сбор и проверка сертификатов</span><span class="sxs-lookup"><span data-stu-id="d6a70-103">Collecting and Verifying Certificates</span></span>

<span data-ttu-id="d6a70-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6a70-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d6a70-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="d6a70-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="d6a70-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="d6a70-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="d6a70-107">Часто требуется собрать и проверить группу [*сертификатов*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d6a70-107">Often a group of [*certificates*](../secgloss/c-gly.md) needs to be collected and verified.</span></span> <span data-ttu-id="d6a70-108">Это часто делается для подготовки группы получателей сообщения с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="d6a70-108">This would often be done to prepare a group of recipients for an enveloped message.</span></span> <span data-ttu-id="d6a70-109">В следующем примере сертификаты в локальном хранилище перечисляются и проверяются на допустимость.</span><span class="sxs-lookup"><span data-stu-id="d6a70-109">In the example that follows, the certificates in a local store are enumerated and checked for validity.</span></span> <span data-ttu-id="d6a70-110">Далее открывается хранилище Active Directory для получения и добавления в локальное хранилище новых сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d6a70-110">Next, an Active Directory store is opened to retrieve and add to the local store new certificates.</span></span> <span data-ttu-id="d6a70-111">Сертификаты, полученные из хранилища Active Directory, проверяются на допустимость и, если они действительны, добавляются в локальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="d6a70-111">The certificates retrieved from the active directory store are checked for validity and, if valid, are added to the local store.</span></span> <span data-ttu-id="d6a70-112">Затем оба хранилища закрываются.</span><span class="sxs-lookup"><span data-stu-id="d6a70-112">Both stores are then closed.</span></span>

<span data-ttu-id="d6a70-113">При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="d6a70-113">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="d6a70-114">Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="d6a70-114">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="d6a70-115">Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d6a70-115">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="d6a70-116">В этом примере имя локального хранилища передается в качестве строкового параметра.</span><span class="sxs-lookup"><span data-stu-id="d6a70-116">In this example, the name of the local store is passed in as a string parameter.</span></span> <span data-ttu-id="d6a70-117">Строка, указывающая условия поиска для сертификатов в хранилище Active Directory, также передается в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="d6a70-117">A string indicating the search criteria for certificates in the Active Directory store is also passed in as a parameter.</span></span>


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
