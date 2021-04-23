---
description: Описание использования средства SignTool для подписания файла.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Использование средства SignTool для подписания файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155082"
---
# <a name="using-signtool-to-sign-a-file"></a><span data-ttu-id="8c815-103">Использование средства SignTool для подписания файла</span><span class="sxs-lookup"><span data-stu-id="8c815-103">Using SignTool to Sign a File</span></span>

<span data-ttu-id="8c815-104">Следующая команда подписывает файл с именем MyControl.exe с помощью [*сертификата*](../secgloss/c-gly.md) , хранящегося в файле обмена личной информацией (PFX):</span><span class="sxs-lookup"><span data-stu-id="8c815-104">The following command signs the file named MyControl.exe using a [*certificate*](../secgloss/c-gly.md) stored in a Personal Information Exchange (PFX) file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

<span data-ttu-id="8c815-105">Следующая команда подписывает файл с помощью сертификата, хранящегося в защищенном паролем файле PFX:</span><span class="sxs-lookup"><span data-stu-id="8c815-105">The following command signs the file using a certificate stored in a password-protected PFX file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="8c815-106">Убедитесь, что пароль правильно защищен.</span><span class="sxs-lookup"><span data-stu-id="8c815-106">Ensure that you properly protect the password.</span></span>

 

<span data-ttu-id="8c815-107">Файл подписывает следующие команды и отметок времени:</span><span class="sxs-lookup"><span data-stu-id="8c815-107">The following command signs and time stamps the file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="8c815-108">Дополнительные сведения о отметке времени для файла после того, как он уже подписан, см. [в разделе Добавление меток времени к ранее подписанным файлам](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="8c815-108">For information about time stamping a file after it has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span>

 

<span data-ttu-id="8c815-109">Следующая команда подписывает файл с помощью сертификата, расположенного в хранилище My, с именем субъекта издателя компании:</span><span class="sxs-lookup"><span data-stu-id="8c815-109">The following command signs the file using a certificate located in the My store with a subject name of My Company Publisher:</span></span>

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

<span data-ttu-id="8c815-110">Следующая команда подписывает элемент управления ActiveX и предоставляет сведения, отображаемые Internet Explorer, когда пользователю предлагается установить элемент управления:</span><span class="sxs-lookup"><span data-stu-id="8c815-110">The following command signs an ActiveX control and provides information that is displayed by Internet Explorer when the user is prompted to install the control:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

<span data-ttu-id="8c815-111">Следующая команда подписывает файл с помощью сертификата, сведения о [*закрытом ключе*](../secgloss/p-gly.md) которого защищены аппаратным модулем шифрования.</span><span class="sxs-lookup"><span data-stu-id="8c815-111">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="8c815-112">Например, предположим, что сертификат с именем "мой High-Value сертификат" имеет закрытый ключ, установленный в аппаратном модуле шифрования, и сертификат установлен правильно.</span><span class="sxs-lookup"><span data-stu-id="8c815-112">For example purposes, assume that the certificate called "My High-Value Certificate," has a private key installed in a hardware cryptography module, and the certificate is properly installed.</span></span>

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

<span data-ttu-id="8c815-113">Следующая команда подписывает файл с помощью сертификата, сведения о [*закрытом ключе*](../secgloss/p-gly.md) которого защищены аппаратным модулем шифрования.</span><span class="sxs-lookup"><span data-stu-id="8c815-113">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="8c815-114">Для хранилища [*центра сертификации*](../secgloss/c-gly.md) (ЦС) указано хранилище компьютера.</span><span class="sxs-lookup"><span data-stu-id="8c815-114">A computer store is specified for the [*certification authority*](../secgloss/c-gly.md) (CA) store.</span></span>

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

<span data-ttu-id="8c815-115">Следующая команда подписывает файл с помощью сертификата, хранящегося в файле.</span><span class="sxs-lookup"><span data-stu-id="8c815-115">The following command signs the file using a certificate stored in a file.</span></span> <span data-ttu-id="8c815-116">Сведения о закрытом ключе защищаются аппаратным модулем шифрования, а [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP) и [*контейнер ключей*](../secgloss/k-gly.md) задаются по имени.</span><span class="sxs-lookup"><span data-stu-id="8c815-116">The private key information is protected by a hardware cryptography module, and the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP)and [*key container*](../secgloss/k-gly.md) are specified by name.</span></span> <span data-ttu-id="8c815-117">Эта команда полезна, если сертификат установлен неправильно.</span><span class="sxs-lookup"><span data-stu-id="8c815-117">This command is useful if the certificate is not properly installed.</span></span>

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

<span data-ttu-id="8c815-118">Средство [SignTool](signtool.md) возвращает текст командной строки, который указывает результат операции подписывания.</span><span class="sxs-lookup"><span data-stu-id="8c815-118">[SignTool](signtool.md) returns command line text that states the result of the signing operation.</span></span> <span data-ttu-id="8c815-119">Кроме того, средство SignTool возвращает нулевой код выхода для успешного выполнения, один для неудачного выполнения и два для выполнения, которые завершились с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="8c815-119">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="8c815-120">Сведения о проверке подписи файла см. [в разделе Использование средства SignTool для проверки подписи файла](using-signtool-to-verify-a-file-signature.md).</span><span class="sxs-lookup"><span data-stu-id="8c815-120">For information about verifying a file's signature, see [Using SignTool to Verify a File Signature](using-signtool-to-verify-a-file-signature.md).</span></span> <span data-ttu-id="8c815-121">Дополнительные сведения о добавлении метки времени, если файл уже подписан, см. в разделе [Добавление меток времени в ранее подписанные файлы](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="8c815-121">For information about adding a time stamp if the file has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span> <span data-ttu-id="8c815-122">Дополнительные сведения о [SignTool](signtool.md)см. в разделе [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="8c815-122">For additional information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 
