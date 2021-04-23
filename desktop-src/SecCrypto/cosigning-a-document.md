---
description: Документ может быть подписан более чем одним подписывающий.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Подписывание документа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105684814"
---
# <a name="cosigning-a-document"></a><span data-ttu-id="fb94e-103">Подписывание документа</span><span class="sxs-lookup"><span data-stu-id="fb94e-103">Cosigning a Document</span></span>

<span data-ttu-id="fb94e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fb94e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fb94e-105">Вместо этого используйте платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="fb94e-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="fb94e-106">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="fb94e-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="fb94e-107">Документ может быть подписан более чем одним подписывающий.</span><span class="sxs-lookup"><span data-stu-id="fb94e-107">A document can be signed by more than one signer.</span></span> <span data-ttu-id="fb94e-108">Это происходит, если, например, две или более стороны подписывают контракт или отчет о расходах.</span><span class="sxs-lookup"><span data-stu-id="fb94e-108">This happens when, for instance, two or more parties sign a contract or an expense report.</span></span> <span data-ttu-id="fb94e-109">В следующем примере документ, который уже подписан, получает второй подписывающий.</span><span class="sxs-lookup"><span data-stu-id="fb94e-109">In the following example, a document already signed is received by a second signer.</span></span> <span data-ttu-id="fb94e-110">Этот подписывающий использует метод [**подписывания**](signeddata-cosign.md) , чтобы присоединить дополнительную сигнатуру к документу.</span><span class="sxs-lookup"><span data-stu-id="fb94e-110">This signer uses the [**CoSign**](signeddata-cosign.md) method to attach an additional signature to the document.</span></span>

<span data-ttu-id="fb94e-111">При возникновении любой ошибки CAPICOM в свойстве **Err. Number** возвращается отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="fb94e-111">If any CAPICOM error occurs, a negative value is returned in the **Err.Number** property.</span></span> <span data-ttu-id="fb94e-112">Дополнительные сведения о кодах ошибок CAPICOM см. в [**разделе \_ \_ код ошибки CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="fb94e-112">For more information about CAPICOM error codes, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="fb94e-113">Если код ошибки в свойстве **Err. Number** имеет положительное значение, то эта ошибка является ошибкой Windows.</span><span class="sxs-lookup"><span data-stu-id="fb94e-113">If the error code in the **Err.Number** property is a positive value, then the error is a Windows error.</span></span> <span data-ttu-id="fb94e-114">Дополнительные сведения о кодах ошибок Windows см. в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="fb94e-114">For information about Windows error codes, see Winerror.h.</span></span>

> [!Note]
> <span data-ttu-id="fb94e-115">При соподписании документа также требуется, чтобы у него был доступный [*сертификат*](../secgloss/c-gly.md) с [*закрытым ключом*](../secgloss/p-gly.md) для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="fb94e-115">Cosigning a document also requires that the cosigner have an available [*certificate*](../secgloss/c-gly.md) with a [*private key*](../secgloss/p-gly.md) to create the signature.</span></span> <span data-ttu-id="fb94e-116">Если подписавший не указан в вызове метода [**Sign**](signeddata-sign.md) и в элементе CAPICOM \_ My Store нет сертификата \_ со связанным закрытым ключом, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="fb94e-116">If a signer is not specified in the call of the [**Sign**](signeddata-sign.md) method and there is no certificate in CAPICOM\_MY\_STORE with an associated private key, the method fails.</span></span> <span data-ttu-id="fb94e-117">Если в CAPICOM My Store есть один и только один \_ сертификат \_ со связанным закрытым ключом, используется этот ключ и сертификат.</span><span class="sxs-lookup"><span data-stu-id="fb94e-117">If there is one and only one certificate in CAPICOM\_MY\_STORE with an associated private key, that key and certificate are used.</span></span> <span data-ttu-id="fb94e-118">Если имеется более одного пригодного для использования сертификата, отображается запрос, позволяющий пользователю выбрать нужный сертификат.</span><span class="sxs-lookup"><span data-stu-id="fb94e-118">If there is more than one usable certificate, a prompt is displayed to allow the user to choose the desired certificate.</span></span>
> 
> <span data-ttu-id="fb94e-119">Если метод [**подписывания**](signeddata-cosign.md) используется в веб-приложении, то перед созданием подписи с помощью закрытого ключа этого средства всегда отображается запрос на получение разрешения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fb94e-119">If the [**CoSign**](signeddata-cosign.md) method is used in a web-based application, a prompt is always displayed to get the user's permission before a signature is created by using that signer's private key.</span></span>

 

<span data-ttu-id="fb94e-120">В следующем примере выполняется чтение файлов, содержащих документ, которые должны быть подписаны, и текущих подписей этого документа, подпись соподписана, а новая сигнатура записывается в файл.</span><span class="sxs-lookup"><span data-stu-id="fb94e-120">In the following example, files that contain the document to be signed and the current signatures on that document are read, the signature is cosigned, and the new signature is written to a file.</span></span> <span data-ttu-id="fb94e-121">В примере используется отсоединенная подпись с подписанными данными и подписью в отдельных файлах.</span><span class="sxs-lookup"><span data-stu-id="fb94e-121">The example uses a detached signature with the data signed and the signature in separate files.</span></span>


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
