---
description: Сведения о создании, обмене, импорте и экспорте ключей Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Ключи Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350145"
---
# <a name="diffie-hellman-keys"></a><span data-ttu-id="6ae45-103">Ключи Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="6ae45-103">Diffie-Hellman Keys</span></span>

-   [<span data-ttu-id="6ae45-104">Создание ключей Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="6ae45-104">Generating Diffie-Hellman Keys</span></span>](#generating-diffie-hellman-keys)
-   [<span data-ttu-id="6ae45-105">Обмен ключами Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="6ae45-105">Exchanging Diffie-Hellman Keys</span></span>](#exchanging-diffie-hellman-keys)
-   [<span data-ttu-id="6ae45-106">Экспорт Diffie-Hellman закрытого ключа</span><span class="sxs-lookup"><span data-stu-id="6ae45-106">Exporting a Diffie-Hellman Private Key</span></span>](#exporting-a-diffie-hellman-private-key)
-   [<span data-ttu-id="6ae45-107">Пример кода</span><span class="sxs-lookup"><span data-stu-id="6ae45-107">Example Code</span></span>](#example-code)

## <a name="generating-diffie-hellman-keys"></a><span data-ttu-id="6ae45-108">Создание ключей Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="6ae45-108">Generating Diffie-Hellman Keys</span></span>

<span data-ttu-id="6ae45-109">Чтобы создать ключ Diffie-Hellman, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6ae45-109">To generate a Diffie-Hellman key, perform the following steps:</span></span>

1.  <span data-ttu-id="6ae45-110">Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="6ae45-110">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="6ae45-111">Создайте новый ключ.</span><span class="sxs-lookup"><span data-stu-id="6ae45-111">Generate the new key.</span></span> <span data-ttu-id="6ae45-112">Это можно сделать двумя способами: выполнив генерацию CryptoAPI всех новых значений для G, P и X или используя существующие значения для G и P и создав новое значение для X.</span><span class="sxs-lookup"><span data-stu-id="6ae45-112">There are two ways to accomplish this—by having CryptoAPI generate all new values for G, P, and X or by using existing values for G and P, and generating a new value for X.</span></span>

    <span data-ttu-id="6ae45-113">**Создание ключа путем создания всех новых значений**</span><span class="sxs-lookup"><span data-stu-id="6ae45-113">**To generate the key by generating all new values**</span></span>

    1.  <span data-ttu-id="6ae45-114">Вызовите функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , передав **калг \_ DH \_ SF** (Store and Forward) или **калг \_ DH \_ ефем** (эфемерный) в параметре *алгид* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-114">Call the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function, passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter.</span></span> <span data-ttu-id="6ae45-115">Ключ будет создан с использованием новых случайных значений для G и P, только что вычисленное значение для X, а его маркер будет возвращен в параметре *фкэй* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-115">The key will be generated using new, random values for G and P, a newly calculated value for X, and its handle will be returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="6ae45-116">Теперь новый ключ готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="6ae45-116">The new key is now ready for use.</span></span> <span data-ttu-id="6ae45-117">Значения G и P должны отправляться получателю вместе с ключом (или отсылаться другим методом) при [*обмене ключами*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6ae45-117">The values of G and P must be sent to the recipient along with the key (or sent by some other method) when doing a [*key exchange*](../secgloss/e-gly.md).</span></span>

    <span data-ttu-id="6ae45-118">**Создание ключа с помощью стандартных значений для G и P**</span><span class="sxs-lookup"><span data-stu-id="6ae45-118">**To generate the key by using predefined values for G and P**</span></span>

    1.  <span data-ttu-id="6ae45-119">Вызовите [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , **передав \_ калг \_ DH SF** (хранение и переадресация) или **калг \_ DH \_ ефем** (эфемерный) в параметре *алгид* , а также метод **шифрования \_ прежен** для параметра *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-119">Call [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter and **CRYPT\_PREGEN** for the *dwFlags* parameter.</span></span> <span data-ttu-id="6ae45-120">В параметре *фкэй* будет создан и возвращен маркер ключа.</span><span class="sxs-lookup"><span data-stu-id="6ae45-120">A key handle will be generated and returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="6ae45-121">Инициализируйте [**зашифрованную структуру \_ \_ BLOB-объектов данных**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) , в которой для элемента **pbData** задано значение P.</span><span class="sxs-lookup"><span data-stu-id="6ae45-121">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the P value.</span></span> <span data-ttu-id="6ae45-122">[*BLOB-объект*](../secgloss/b-gly.md) не содержит сведений о заголовках, а элемент **pbData** имеет формат с [*прямым порядком байтов*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae45-122">The [*BLOB*](../secgloss/b-gly.md) contains no header information and the **pbData** member is in [*little-endian*](../secgloss/l-gly.md) format.</span></span>
    3.  <span data-ttu-id="6ae45-123">Значение P задается путем вызова функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , передачи маркера ключа, полученного на шаге a, в параметре *hKey* , флага **\_ P ключевого индикатора** в параметре *Двпарам* и указателя на структуру, содержащую значение P в параметре *pbData* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-123">The value of P is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_P** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of P in the *pbData* parameter.</span></span>
    4.  <span data-ttu-id="6ae45-124">Инициализируйте [**зашифрованную структуру \_ \_ BLOB-объектов данных**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) , в которой для элемента **pbData** задано значение G.</span><span class="sxs-lookup"><span data-stu-id="6ae45-124">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the G value.</span></span> <span data-ttu-id="6ae45-125">BLOB-объект не содержит сведений о заголовках, а элемент **pbData** имеет формат с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="6ae45-125">The BLOB contains no header information and the **pbData** member is in little-endian format.</span></span>
    5.  <span data-ttu-id="6ae45-126">Значение G задается вызовом функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , передачей маркера ключа, полученного на шаге a, в параметре *hKey* , флаг **\_ G** в параметре *Двпарам* и указатель на структуру, содержащую значение G в параметре *pbData* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-126">The value of G is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_G** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of G in the *pbData* parameter.</span></span>
    6.  <span data-ttu-id="6ae45-127">Значение X создается путем вызова функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , передачей маркера ключа, полученного на шаге a, в параметре *hKey* , флаг **\_ X** в параметре *двпарам* и **значение NULL** в параметре *pbData* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-127">The value of X is generated by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_X** flag in the *dwParam* parameter, and **NULL** in the *pbData* parameter.</span></span>
    7.  <span data-ttu-id="6ae45-128">Если все вызовы функции были выполнены, Diffie-Hellman открытый ключ готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="6ae45-128">If all the function calls succeeded, the Diffie-Hellman public key is ready for use.</span></span>

3.  <span data-ttu-id="6ae45-129">Если ключ больше не нужен, удалите его, передав маркер ключа в функцию [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="6ae45-129">When the key is no longer needed, destroy it by passing the key handle to the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

<span data-ttu-id="6ae45-130">Если в предыдущих процедурах был указан **калг \_ DH \_ SF** , значения ключей сохраняются в хранилище при каждом вызове функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="6ae45-130">If **CALG\_DH\_SF** was specified in the previous procedures, the key values are persisted to storage with each call to [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span></span> <span data-ttu-id="6ae45-131">Затем можно получить значения G и P с помощью функции [**криптжеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) .</span><span class="sxs-lookup"><span data-stu-id="6ae45-131">The G and P values can then be retrieved by using the [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) function.</span></span> <span data-ttu-id="6ae45-132">Некоторые поставщики служб шифрования могут иметь жестко запрограммированные значения G и P.</span><span class="sxs-lookup"><span data-stu-id="6ae45-132">Some CSPs may have hard-coded G and P values.</span></span> <span data-ttu-id="6ae45-133">В этом случае возникнет ошибка **\_ фикседпараметер** , если метод **криптсеткэйпарам** вызывается с помощью **ключевого индикатора \_ G** или **ключевого индикатора \_ P** , указанного в параметре *двпарам* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-133">In this case a **NTE\_FIXEDPARAMETER** error will be returned if **CryptSetKeyParam** is called with **KP\_G** or **KP\_P** specified in the *dwParam* parameter.</span></span> <span data-ttu-id="6ae45-134">Если вызывается **криптдестройкэй** , маркер ключа уничтожается, но значения ключа сохраняются в CSP.</span><span class="sxs-lookup"><span data-stu-id="6ae45-134">If **CryptDestroyKey** is called, the handle to the key is destroyed, but the key values are retained in the CSP.</span></span> <span data-ttu-id="6ae45-135">Однако если **калг \_ DH \_ ефем** был указан, то маркер ключа уничтожается, и все значения удаляются из CSP.</span><span class="sxs-lookup"><span data-stu-id="6ae45-135">However, if **CALG\_DH\_EPHEM** was specified, the handle to the key is destroyed, and all values are cleared from the CSP.</span></span>

## <a name="exchanging-diffie-hellman-keys"></a><span data-ttu-id="6ae45-136">Обмен ключами Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="6ae45-136">Exchanging Diffie-Hellman Keys</span></span>

<span data-ttu-id="6ae45-137">Целью алгоритма Diffie-Hellman является возможность создания и совместного использования идентичного секретного ключа сеанса двумя или более сторонами путем предоставления общего доступа к информации по незащищенной сети.</span><span class="sxs-lookup"><span data-stu-id="6ae45-137">The purpose of the Diffie-Hellman algorithm is to make it possible for two or more parties to create and share an identical, secret session key by sharing information over a network that is not secure.</span></span> <span data-ttu-id="6ae45-138">Общие сведения о сети находятся в виде пары значений констант и Diffie-Hellman открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="6ae45-138">The information that gets shared over the network is in the form of a couple of constant values and a Diffie-Hellman public key.</span></span> <span data-ttu-id="6ae45-139">Ниже приведены процессы, используемые двумя сторонами обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="6ae45-139">The process used by two key-exchange parties is as follows:</span></span>

-   <span data-ttu-id="6ae45-140">Обе стороны согласны с Diffie-Hellmanными параметрами, которые являются простыми числами (P) и номером генератора (G).</span><span class="sxs-lookup"><span data-stu-id="6ae45-140">Both parties agree to the Diffie-Hellman parameters which are a prime number (P) and a generator number (G).</span></span>
-   <span data-ttu-id="6ae45-141">Сторона 1 отправляет свой Diffie-Hellman открытый ключ в сторону 2.</span><span class="sxs-lookup"><span data-stu-id="6ae45-141">Party 1 sends its Diffie-Hellman public key to party 2.</span></span>
-   <span data-ttu-id="6ae45-142">Сторона 2 рассчитывает секретный ключ сеанса, используя сведения, содержащиеся в его закрытом ключе и открытом ключе.</span><span class="sxs-lookup"><span data-stu-id="6ae45-142">Party 2 computes the secret session key by using the information contained in its private key and party 1's public key.</span></span>
-   <span data-ttu-id="6ae45-143">Сторона 2 отправляет свой Diffie-Hellman открытый ключ в сторону 1.</span><span class="sxs-lookup"><span data-stu-id="6ae45-143">Party 2 sends its Diffie-Hellman public key to party 1.</span></span>
-   <span data-ttu-id="6ae45-144">Сторона 1 рассчитывает секретный ключ сеанса, используя сведения, содержащиеся в его закрытом ключе и открытом ключе.</span><span class="sxs-lookup"><span data-stu-id="6ae45-144">Party 1 computes the secret session key by using the information contained in its private key and party 2's public key.</span></span>
-   <span data-ttu-id="6ae45-145">Обе стороны теперь имеют одинаковый сеансовый ключ, который можно использовать для шифрования и расшифровки данных.</span><span class="sxs-lookup"><span data-stu-id="6ae45-145">Both parties now have the same session key, which can be used for encrypting and decrypting data.</span></span> <span data-ttu-id="6ae45-146">Шаги, необходимые для этого, показаны в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="6ae45-146">The steps necessary for this are shown in the following procedure.</span></span>

<span data-ttu-id="6ae45-147">**Подготовка Diffie-Hellman открытого ключа к передаче**</span><span class="sxs-lookup"><span data-stu-id="6ae45-147">**To prepare a Diffie-Hellman public key for transmission**</span></span>

1.  <span data-ttu-id="6ae45-148">Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="6ae45-148">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="6ae45-149">Создайте ключ Diffie-Hellman, вызвав функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания нового ключа или вызвав функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) для получения существующего ключа.</span><span class="sxs-lookup"><span data-stu-id="6ae45-149">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="6ae45-150">Получите размер, необходимый для хранения большого двоичного объекта Diffie-Hellman Key, вызвав [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), передав **значение NULL** для параметра *pbData* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-150">Get the size needed to hold the Diffie-Hellman key BLOB by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passing **NULL** for the *pbData* parameter.</span></span> <span data-ttu-id="6ae45-151">Требуемый размер будет возвращен в *пдвдатален*.</span><span class="sxs-lookup"><span data-stu-id="6ae45-151">The required size will be returned in *pdwDataLen*.</span></span>
4.  <span data-ttu-id="6ae45-152">Выделение памяти для большого двоичного объекта ключа.</span><span class="sxs-lookup"><span data-stu-id="6ae45-152">Allocate memory for the key BLOB.</span></span>
5.  <span data-ttu-id="6ae45-153">Создайте Diffie-Hellman [*большой двоичный объект открытого ключа*](../secgloss/p-gly.md) , вызвав функцию [**Криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , передав **публиккэйблоб** в параметре *двблобтипе* и в качестве ключа в Diffie-Hellman ключ в параметре *hKey* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-153">Create a Diffie-Hellman [*public key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PUBLICKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span> <span data-ttu-id="6ae45-154">Этот вызов функции вызывает вычисление значения открытого ключа (G ^ X) mod P.</span><span class="sxs-lookup"><span data-stu-id="6ae45-154">This function call causes the calculation of the public key value, (G^X) mod P.</span></span>
6.  <span data-ttu-id="6ae45-155">Если все предыдущие вызовы функций были успешными, Diffie-Hellman большой двоичный объект открытого ключа теперь готов для кодирования и передачи.</span><span class="sxs-lookup"><span data-stu-id="6ae45-155">If all the preceding function calls were successful, the Diffie-Hellman public key BLOB is now ready to be encoded and transmitted.</span></span>

<span data-ttu-id="6ae45-156">**Импорт Diffie-Hellman открытого ключа и вычисление секретного ключа сеанса**</span><span class="sxs-lookup"><span data-stu-id="6ae45-156">**To import a Diffie-Hellman public key and calculate the secret session key**</span></span>

1.  <span data-ttu-id="6ae45-157">Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="6ae45-157">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="6ae45-158">Создайте ключ Diffie-Hellman, вызвав функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания нового ключа или вызвав функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) для получения существующего ключа.</span><span class="sxs-lookup"><span data-stu-id="6ae45-158">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="6ae45-159">Чтобы импортировать Diffie-Hellman открытый ключ в CSP, вызовите функцию [**криптимпорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , передав указатель на большой двоичный объект открытого ключа в параметре *pbData* , длину большого двоичного объекта в параметре *двдатален* и указатель на Diffie-Hellman ключ в параметре *хпубкэй* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-159">To import the Diffie-Hellman public key into the CSP, call the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function, passing a pointer to the public key BLOB in the *pbData* parameter, the length of the BLOB in the *dwDataLen* parameter, and the handle to the Diffie-Hellman key in the *hPubKey* parameter.</span></span> <span data-ttu-id="6ae45-160">Это приводит к выполнению вычислений (Y ^ X) mod P, что создает общий секретный ключ и завершает [*Обмен ключами*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6ae45-160">This causes the calculation, (Y^X) mod P, to be performed, thus creating the shared, secret key and completing the [*key exchange*](../secgloss/e-gly.md).</span></span> <span data-ttu-id="6ae45-161">Этот вызов функции возвращает маркер нового секретного ключа сеанса в параметре *hKey* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-161">This function call returns a handle to the new, secret, session key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="6ae45-162">На этом этапе импортированный Diffie-Hellman имеет тип **калг \_ агридкэй \_ ANY**.</span><span class="sxs-lookup"><span data-stu-id="6ae45-162">At this point, the imported Diffie-Hellman is of type **CALG\_AGREEDKEY\_ANY**.</span></span> <span data-ttu-id="6ae45-163">Прежде чем ключ можно будет использовать, его необходимо преобразовать в тип ключа сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ae45-163">Before the key can be used, it must be converted into a session key type.</span></span> <span data-ttu-id="6ae45-164">Это достигается путем вызова функции [**криптсеткэйпарам**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) с параметром *двпарам* , установленным в **ключевое \_ алгид** , а *pbData* — указателем на значение [**\_ идентификатора ALG**](alg-id.md) , представляющее ключ сеанса, например **калг \_ RC4**.</span><span class="sxs-lookup"><span data-stu-id="6ae45-164">This is accomplished by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function with *dwParam* set to **KP\_ALGID** and with *pbData* set to a pointer to a [**ALG\_ID**](alg-id.md) value that represents a session key, such as **CALG\_RC4**.</span></span> <span data-ttu-id="6ae45-165">Перед использованием общего ключа в функции [**криптенкрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) или [**криптдекрипт**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) необходимо преобразовать ключ.</span><span class="sxs-lookup"><span data-stu-id="6ae45-165">The key must be converted before using the shared key in the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) or [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span> <span data-ttu-id="6ae45-166">Вызовы любой из этих функций до преобразования типа ключа завершатся ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6ae45-166">Calls made to either of these functions prior to converting the key type will fail.</span></span>
5.  <span data-ttu-id="6ae45-167">Секретный ключ сеанса теперь готов к использованию для шифрования или расшифровки.</span><span class="sxs-lookup"><span data-stu-id="6ae45-167">The secret session key is now ready to be used for encryption or decryption.</span></span>
6.  <span data-ttu-id="6ae45-168">Если ключ больше не нужен, удалите его, вызвав функцию [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="6ae45-168">When the key is no longer needed, destroy the key handle by calling the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

## <a name="exporting-a-diffie-hellman-private-key"></a><span data-ttu-id="6ae45-169">Экспорт Diffie-Hellman закрытого ключа</span><span class="sxs-lookup"><span data-stu-id="6ae45-169">Exporting a Diffie-Hellman Private Key</span></span>

<span data-ttu-id="6ae45-170">Чтобы экспортировать Diffie-Hellman закрытый ключ, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6ae45-170">To export a Diffie-Hellman private key, perform the following steps:</span></span>

1.  <span data-ttu-id="6ae45-171">Вызовите функцию [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) , чтобы получить маркер поставщика служб шифрования Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="6ae45-171">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="6ae45-172">Создайте ключ Diffie-Hellman, вызвав функцию [**криптженкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) для создания нового ключа или вызвав функцию [**криптжетусеркэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) для получения существующего ключа.</span><span class="sxs-lookup"><span data-stu-id="6ae45-172">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="6ae45-173">Создайте Diffie-Hellman [*большой двоичный объект закрытого ключа*](../secgloss/p-gly.md) , вызвав функцию [**Криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , передав **приватекэйблоб** в параметре *двблобтипе* и маркер в ключ Diffie-Hellman в параметре *hKey* .</span><span class="sxs-lookup"><span data-stu-id="6ae45-173">Create a Diffie-Hellman [*private key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PRIVATEKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="6ae45-174">Если маркер ключа больше не нужен, вызовите функцию [**криптдестройкэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) для уничтожения маркера ключа.</span><span class="sxs-lookup"><span data-stu-id="6ae45-174">When the key handle is no longer needed, call the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function to destroy the key handle.</span></span>

## <a name="example-code"></a><span data-ttu-id="6ae45-175">Пример кода</span><span class="sxs-lookup"><span data-stu-id="6ae45-175">Example Code</span></span>

<span data-ttu-id="6ae45-176">В следующем примере показано, как создать, экспортировать, импортировать и использовать ключ Diffie-Hellman для выполнения обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="6ae45-176">The following example shows how to create, export, import, and use a Diffie-Hellman key to perform a key exchange.</span></span>


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
