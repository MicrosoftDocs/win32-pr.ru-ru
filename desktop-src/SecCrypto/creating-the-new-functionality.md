---
description: Следующие функции доступны для расширенных функций CryptoAPI.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Создание новых функциональных возможностей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541007"
---
# <a name="creating-the-new-functionality"></a><span data-ttu-id="b3917-103">Создание новых функциональных возможностей</span><span class="sxs-lookup"><span data-stu-id="b3917-103">Creating the New Functionality</span></span>

<span data-ttu-id="b3917-104">Следующие функции доступны для расширенных функций CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="b3917-104">The following functions are among the CryptoAPI functions that can be extended.</span></span>



| <span data-ttu-id="b3917-105">CryptoAPI, функция</span><span class="sxs-lookup"><span data-stu-id="b3917-105">CryptoAPI function</span></span>                                   | <span data-ttu-id="b3917-106">Определение имени функции OID</span><span class="sxs-lookup"><span data-stu-id="b3917-106">OID function name define</span></span>                         | <span data-ttu-id="b3917-107">Строка имени функции OID</span><span class="sxs-lookup"><span data-stu-id="b3917-107">OID function name string</span></span>  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="b3917-108">**CryptEncodeObject**</span><span class="sxs-lookup"><span data-stu-id="b3917-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | <span data-ttu-id="b3917-109">\_Шифрование OID \_ шифрования \_ объекта \_ Func</span><span class="sxs-lookup"><span data-stu-id="b3917-109">CRYPT\_OID\_ENCODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="b3917-110">"Криптдлленкодеобжект"</span><span class="sxs-lookup"><span data-stu-id="b3917-110">"CryptDllEncodeObject"</span></span>    |
| [<span data-ttu-id="b3917-111">**криптдекодеобжект**</span><span class="sxs-lookup"><span data-stu-id="b3917-111">**CryptDecodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | <span data-ttu-id="b3917-112">\_ \_ расшифровка объекта шифрования OID \_ \_ Func</span><span class="sxs-lookup"><span data-stu-id="b3917-112">CRYPT\_OID\_DECODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="b3917-113">"Криптдллдекодеобжект"</span><span class="sxs-lookup"><span data-stu-id="b3917-113">"CryptDllDecodeObject"</span></span>    |
| [<span data-ttu-id="b3917-114">**цертопенсторе**</span><span class="sxs-lookup"><span data-stu-id="b3917-114">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | <span data-ttu-id="b3917-115">ШИФРОВАНИЯ \_ OID \_ Open \_ Store \_ Prov \_ Func</span><span class="sxs-lookup"><span data-stu-id="b3917-115">CRYPT\_OID\_OPEN\_ STORE\_PROV\_FUNC</span></span><br/>  | <span data-ttu-id="b3917-116">"Цертдллопенсторепров"</span><span class="sxs-lookup"><span data-stu-id="b3917-116">"CertDllOpenStoreProv"</span></span>    |
| [<span data-ttu-id="b3917-117">**цертверификтлусаже**</span><span class="sxs-lookup"><span data-stu-id="b3917-117">**CertVerifyCTLUsage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | <span data-ttu-id="b3917-118">способ \_ шифрования \_ OID \_ проверки \_ использования CTL \_ Func</span><span class="sxs-lookup"><span data-stu-id="b3917-118">CRYPT\_OID\_VERIFY\_ CTL\_USAGE\_FUNC</span></span><br/> | <span data-ttu-id="b3917-119">"Цертдллверификтлусаже"</span><span class="sxs-lookup"><span data-stu-id="b3917-119">"CertDllVerifyCTLUsage"</span></span>   |
| [<span data-ttu-id="b3917-120">**цертверифиревокатион**</span><span class="sxs-lookup"><span data-stu-id="b3917-120">**CertVerifyRevocation**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | <span data-ttu-id="b3917-121">\_ \_ подтвердить отзыв проверки \_ отзыва OID \_</span><span class="sxs-lookup"><span data-stu-id="b3917-121">CRYPT\_OID\_VERIFY\_ REVOCATION\_FUNC</span></span><br/> | <span data-ttu-id="b3917-122">"Цертдллверифиревокатион"</span><span class="sxs-lookup"><span data-stu-id="b3917-122">"CertDllVerifyRevocation"</span></span> |



 

<span data-ttu-id="b3917-123">При нормальном использовании с существующим идентификатором объекта и типом кодировки используется код самой функции CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="b3917-123">In normal use with an existing OID and encoding type, the code in the CryptoAPI function, itself, is used.</span></span> <span data-ttu-id="b3917-124">Если одна из этих функций вызывается с идентификатором OID и типом кодировки, которую код в функции CryptoAPI не предназначал для обработки, то в библиотеке DLL должна быть создана новая функция, содержащая новые функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="b3917-124">If one of these functions is called with an OID and encoding type that code in the CryptoAPI function was not designed to handle, a new function, containing the new functionality, must be created in a DLL.</span></span> <span data-ttu-id="b3917-125">Эта библиотека DLL должна быть зарегистрирована в реестре или установлена в памяти.</span><span class="sxs-lookup"><span data-stu-id="b3917-125">That DLL must be registered in the registry or installed in memory.</span></span>

<span data-ttu-id="b3917-126">Когда одна из перечисленных функций вызывается с вновь назначенным идентификатором OID и типом кодирования, используется код в новой библиотеке DLL, а не код, предоставленный как часть функции CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="b3917-126">When one of the listed functions is called with the newly designated OID and encoding type, the code in the new DLL is used rather than the code provided as part of the CryptoAPI function.</span></span>

<span data-ttu-id="b3917-127">Имя вновь разработанной функции может быть именем, указанным в разделе "строка имени функции OID" в предыдущей таблице, или может быть задано другое имя при регистрации нового кода функции.</span><span class="sxs-lookup"><span data-stu-id="b3917-127">The name of the newly developed function can be the name listed under "OID function name string" in the previous table or a different name can be given when the new function code is registered.</span></span>

<span data-ttu-id="b3917-128">Новая функция должна использовать соответствующий прототип.</span><span class="sxs-lookup"><span data-stu-id="b3917-128">The new function must use an appropriate prototype.</span></span> <span data-ttu-id="b3917-129">Во всех случаях, за исключением [**цертопенсторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), этот прототип аналогичен функции CryptoAPI, которая вызывает новую функцию.</span><span class="sxs-lookup"><span data-stu-id="b3917-129">In all cases except for [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), this prototype is the same as the CryptoAPI function that calls the new function.</span></span> <span data-ttu-id="b3917-130">В случае с **цертопенсторе** прототип выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="b3917-130">In the case of **CertOpenStore** the prototype is as follows.</span></span>


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> <span data-ttu-id="b3917-131">Если прототипы не совпадают, системный стек будет поврежден.</span><span class="sxs-lookup"><span data-stu-id="b3917-131">If the prototypes do not match, the system stack will be corrupted.</span></span>

 

<span data-ttu-id="b3917-132">Помимо предоставления кода для новой функции в библиотеке DLL, расширение функциональных возможностей [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) или [**криптдекодеобжект**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) требует определения типа для новой структуры данных C, которая будет помещена в заголовочный файл, включенный при компиляции программы пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3917-132">In addition to providing the code for the new function in a DLL, extending the functionality of [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) or [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requires a type definition for the new C data structure to be placed in a header file included when the user's program is compiled.</span></span>

 

 




