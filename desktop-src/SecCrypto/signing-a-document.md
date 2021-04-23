---
description: Подпись обычно используется для подписи текста и сохранения этого подписанного текста в файл. Подписанный текст также может быть отправлен через Интернет. Подписанное сообщение находится в \# формате PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Подписание документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662116"
---
# <a name="signing-a-document"></a><span data-ttu-id="a1188-105">Подписание документа</span><span class="sxs-lookup"><span data-stu-id="a1188-105">Signing a Document</span></span>

<span data-ttu-id="a1188-106">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1188-106">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a1188-107">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="a1188-107">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="a1188-108">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="a1188-108">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="a1188-109">Подпись обычно используется для подписи текста и сохранения этого подписанного текста в файл.</span><span class="sxs-lookup"><span data-stu-id="a1188-109">A standard use of a signature is to sign a text and save that signed text to a file.</span></span> <span data-ttu-id="a1188-110">Подписанный текст также может быть отправлен через Интернет.</span><span class="sxs-lookup"><span data-stu-id="a1188-110">The signed text could also be sent over the Internet.</span></span> <span data-ttu-id="a1188-111">Подписанное сообщение находится в \# формате PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="a1188-111">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="a1188-112">В этом примере подпись создается для отсоединенного содержимого (если содержимое не включено в подпись).</span><span class="sxs-lookup"><span data-stu-id="a1188-112">In this example, the signature is created for detached content (when the content is not included with the signature).</span></span> <span data-ttu-id="a1188-113">Отсоединенная сигнатура чаще всего используется, если получатель подписи имеет копию точного подписанного текста.</span><span class="sxs-lookup"><span data-stu-id="a1188-113">A detached signature would most often be used if the recipient of the signature has a copy of the exact signed text.</span></span> <span data-ttu-id="a1188-114">В приведенном ниже примере исходное сообщение и отсоединенная подпись записываются в отдельные файлы.</span><span class="sxs-lookup"><span data-stu-id="a1188-114">In the example below, the original message and the detached signature are written to separate files.</span></span>

<span data-ttu-id="a1188-115">При любой ошибке CAPICOM возвращается отрицательное десятичное значение **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="a1188-115">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="a1188-116">Дополнительные сведения см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="a1188-116">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="a1188-117">Сведения о положительных десятичных значениях **Err. Number** см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="a1188-117">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="a1188-118">При создании подписи используется [*закрытый ключ*](../secgloss/p-gly.md)подписывающий.</span><span class="sxs-lookup"><span data-stu-id="a1188-118">Creating a signature uses the signer's [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="a1188-119">Подпись можно создать, только если доступен сертификат подписавший с соответствующим закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="a1188-119">A signature can only be created if the signer's certificate with an associated private key is available.</span></span> <span data-ttu-id="a1188-120">В этом примере метода **Sign** не указан подписывающий.</span><span class="sxs-lookup"><span data-stu-id="a1188-120">This example of the **Sign** method does not specify a signer.</span></span> <span data-ttu-id="a1188-121">Если подписавший не указан и ни один из сертификатов в элементе **CAPICOM \_ My \_ Store** не имеет связанного закрытого ключа, то метод **Sign** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a1188-121">If a signer is not specified and no certificate in **CAPICOM\_MY\_STORE** has an associated private key, the **Sign** method fails.</span></span> <span data-ttu-id="a1188-122">Если один и только один сертификат в элементе **CAPICOM \_ My \_ Store** имеет связанный закрытый ключ, то для создания подписи используется этот сертификат и его закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="a1188-122">If one and only one certificate in **CAPICOM\_MY\_STORE** has an associated private key, that certificate and its private key is used to create the signature.</span></span> <span data-ttu-id="a1188-123">Если несколько сертификатов в хранилище **CAPICOM \_ My \_ Store** имеют связанный закрытый ключ, появляется диалоговое окно, и пользователь может выбрать сертификат, который будет использоваться для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="a1188-123">If more than one certificate in the **CAPICOM\_MY\_STORE** store has an associated private key, a dialog box appears and the user can choose the certificate to be used to create the signature.</span></span>

<span data-ttu-id="a1188-124">Когда веб-приложение использует метод **Sign** , всегда отображается запрос, а перед подписью, использующей закрытый ключ этого пользователя, требуется разрешение.</span><span class="sxs-lookup"><span data-stu-id="a1188-124">When a web-based application uses the **Sign** method, a prompt is always displayed and the user's permission is required before a signature that uses that signer's private key is created.</span></span>


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a><span data-ttu-id="a1188-125">См. также</span><span class="sxs-lookup"><span data-stu-id="a1188-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1188-126">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="a1188-126">**Store.Open**</span></span>](store-open.md)
</dt> <dt>

[<span data-ttu-id="a1188-127">**Подписавший. сертификат**</span><span class="sxs-lookup"><span data-stu-id="a1188-127">**Signer.Certificate**</span></span>](signer-certificate.md)
</dt> <dt>

[<span data-ttu-id="a1188-128">**attribute**</span><span class="sxs-lookup"><span data-stu-id="a1188-128">**Attribute**</span></span>](attribute.md)
</dt> <dt>

[<span data-ttu-id="a1188-129">**сигнеддата**</span><span class="sxs-lookup"><span data-stu-id="a1188-129">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
