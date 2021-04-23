---
description: Сертификаты можно добавлять или удалять из хранилищ сертификатов, если хранилище открыто с разрешением на чтение и запись.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Добавление сертификатов в хранилище сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545671"
---
# <a name="adding-certificates-to-a-certificate-store"></a><span data-ttu-id="83dc2-103">Добавление сертификатов в хранилище сертификатов</span><span class="sxs-lookup"><span data-stu-id="83dc2-103">Adding Certificates to a Certificate Store</span></span>

<span data-ttu-id="83dc2-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83dc2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="83dc2-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="83dc2-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="83dc2-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="83dc2-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="83dc2-107">[*Сертификаты*](../secgloss/c-gly.md) можно добавлять или удалять из [*хранилищ сертификатов*](../secgloss/c-gly.md) , если хранилище открыто с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="83dc2-107">[*Certificates*](../secgloss/c-gly.md) can be added to or removed from [*certificate stores*](../secgloss/c-gly.md) if the store is opened with read/write permission.</span></span> <span data-ttu-id="83dc2-108">Разрешения на чтение и запись не предоставлены Active Directory хранилищам.</span><span class="sxs-lookup"><span data-stu-id="83dc2-108">Read/write permission is not granted to Active Directory stores.</span></span> <span data-ttu-id="83dc2-109">Хотя сертификаты могут быть добавлены или удалены из хранилищ памяти, изменения в хранилищах памяти не сохраняются между сеансами.</span><span class="sxs-lookup"><span data-stu-id="83dc2-109">While certificates can be added to or removed from memory stores, changes in memory stores are not persisted between sessions.</span></span>

<span data-ttu-id="83dc2-110">Сертификаты можно добавить в хранилище сертификатов, открытое с разрешением на чтение и запись, с помощью метода **Add** .</span><span class="sxs-lookup"><span data-stu-id="83dc2-110">Certificates can be added to a certificate store that is opened with read/write permission by using the **Add** method.</span></span> <span data-ttu-id="83dc2-111">Сертификат можно удалить из хранилища сертификатов, открытого с разрешением на чтение и запись, с помощью метода **Remove** .</span><span class="sxs-lookup"><span data-stu-id="83dc2-111">A certificate can be removed from a certificate store that is opened with read/write permission by using the **Remove** method.</span></span> <span data-ttu-id="83dc2-112">Новые магазины можно создавать и сохранять в \_ расположениях "CAPICOM Current \_ User" и " \_ CAPICOM \_ Local \_ Machine Store" \_ .</span><span class="sxs-lookup"><span data-stu-id="83dc2-112">New stores can be created and saved in the CAPICOM\_CURRENT\_USER\_STORE and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="83dc2-113">Вновь созданные хранилища в любом из этих расположений можно открыть с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="83dc2-113">Newly created stores in either of these locations can be opened with read/write permission.</span></span>

<span data-ttu-id="83dc2-114">В следующем примере открыто два хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="83dc2-114">In the following example, two certificate stores are opened.</span></span> <span data-ttu-id="83dc2-115">Сертификаты субъектов с фамилиями, начинающимися с F, извлекаются из хранилища Active Directory.</span><span class="sxs-lookup"><span data-stu-id="83dc2-115">Certificates of subjects with last names beginning with F are retrieved from the Active Directory store.</span></span> <span data-ttu-id="83dc2-116">В этом случае хранилище CAPICOM \_ Current \_ User Store \_ , CAPICOM CA Store, \_ \_ открывается как хранилище для чтения и записи, а первый сертификат из коллекции сертификатов в хранилище Active Directory добавляется в сертификаты в \_ хранилище CAPICOM CA \_ .</span><span class="sxs-lookup"><span data-stu-id="83dc2-116">The CAPICOM\_CURRENT\_USER\_STORE, CAPICOM\_CA\_STORE store is then opened as a read/write store and the first certificate from the collection of certificates in the Active Directory store is added to the certificates in the CAPICOM\_CA\_STORE.</span></span>

<span data-ttu-id="83dc2-117">В демонстрационных целях в примере показано открытие магазинов в расположениях "CAPICOM \_ Memory \_ Store", "CAPICOM \_ Current \_ user \_ Store" и "CAPICOM \_ Local \_ Machine Store" \_ .</span><span class="sxs-lookup"><span data-stu-id="83dc2-117">For demonstration purposes, the example shows the opening of stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="83dc2-118">В примере показано, как экспортировать все сертификаты из открытого хранилища, записать экспортированные сертификаты в файл, прочитать их обратно и импортировать в другое хранилище.</span><span class="sxs-lookup"><span data-stu-id="83dc2-118">The example shows exporting all certificates from an open store, writing the exported certificates to a file, reading them back in, and importing them into a different store.</span></span> <span data-ttu-id="83dc2-119">Вновь импортированные сертификаты будут перечислены и отображены.</span><span class="sxs-lookup"><span data-stu-id="83dc2-119">The newly imported certificates are them enumerated and displayed.</span></span>

<span data-ttu-id="83dc2-120">При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="83dc2-120">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="83dc2-121">Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="83dc2-121">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="83dc2-122">Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="83dc2-122">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="83dc2-123">В следующем примере показано открытие хранилищ сертификатов с помощью раннего связывания в объявлении объектов **хранилища** и при создании экземпляра этих объектов.</span><span class="sxs-lookup"><span data-stu-id="83dc2-123">The following example shows opening certificate stores using early binding in the declaration of the **Store** objects and in creating an instance of those objects.</span></span>


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
