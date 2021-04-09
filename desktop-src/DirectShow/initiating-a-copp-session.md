---
description: Запуск сеанса Копп
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Запуск сеанса Копп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140375"
---
# <a name="initiating-a-copp-session"></a><span data-ttu-id="a34af-103">Запуск сеанса Копп</span><span class="sxs-lookup"><span data-stu-id="a34af-103">Initiating a COPP Session</span></span>

<span data-ttu-id="a34af-104">Чтобы инициировать сеанс протокола Копп, необходимо подготовить *сигнатуру*, которая представляет собой массив, содержащий объединение следующих чисел:</span><span class="sxs-lookup"><span data-stu-id="a34af-104">To initiate a Certified Output Protection Protocol (COPP) session, you must prepare a *signature*, which is an array that contains the concatenation of the following numbers:</span></span>

-   <span data-ttu-id="a34af-105">128-разрядное случайное число, возвращенное драйвером.</span><span class="sxs-lookup"><span data-stu-id="a34af-105">The 128-bit random number returned by the driver.</span></span> <span data-ttu-id="a34af-106">(Это значение отображается как *гуидрандом* при [получении цепочки сертификатов драйвера](obtaining-the-drivers-certificate-chain.md).)</span><span class="sxs-lookup"><span data-stu-id="a34af-106">(This value is shown as *guidRandom* in [Obtaining the Driver's Certificate Chain](obtaining-the-drivers-certificate-chain.md).)</span></span>
-   <span data-ttu-id="a34af-107">128-битный симметричный ключ AES.</span><span class="sxs-lookup"><span data-stu-id="a34af-107">A 128-bit symmetric AES key.</span></span>
-   <span data-ttu-id="a34af-108">32-разрядный начальный порядковый номер для запросов состояния.</span><span class="sxs-lookup"><span data-stu-id="a34af-108">A 32-bit starting sequence number for status requests.</span></span>
-   <span data-ttu-id="a34af-109">32-разрядный начальный порядковый номер для команд Копп.</span><span class="sxs-lookup"><span data-stu-id="a34af-109">A 32-bit starting sequence number for COPP commands.</span></span>

<span data-ttu-id="a34af-110">Создайте симметричный ключ AES следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a34af-110">Generate a symmetric AES key as follows:</span></span>


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



<span data-ttu-id="a34af-111">Функция **криптженкэй** создает симметричный ключ, но ключ по-прежнему ХРАНИТСЯ в CSP.</span><span class="sxs-lookup"><span data-stu-id="a34af-111">The **CryptGenKey** function creates the symmetric key, but the key is still held in the CSP.</span></span> <span data-ttu-id="a34af-112">Чтобы экспортировать ключ в массив байтов, используйте функцию **криптекспорткэй** .</span><span class="sxs-lookup"><span data-stu-id="a34af-112">To export the key into a byte array, use the **CryptExportKey** function.</span></span> <span data-ttu-id="a34af-113">Это причина использования \_ флага для экспорта при вызове **криптженкэй**.</span><span class="sxs-lookup"><span data-stu-id="a34af-113">This is the reason for using the CRYPT\_EXPORTABLE flag when calling **CryptGenKey**.</span></span> <span data-ttu-id="a34af-114">Следующий код экспортирует ключ и копирует его в</span><span class="sxs-lookup"><span data-stu-id="a34af-114">The following code exports the key and copies it into the</span></span>


```
pData
```



<span data-ttu-id="a34af-115">Массив.</span><span class="sxs-lookup"><span data-stu-id="a34af-115">array.</span></span>


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



<span data-ttu-id="a34af-116">Данные, возвращаемые в</span><span class="sxs-lookup"><span data-stu-id="a34af-116">The data returned in</span></span>


```
pData
```



<span data-ttu-id="a34af-117">имеет следующий макет:</span><span class="sxs-lookup"><span data-stu-id="a34af-117">has the following layout:</span></span>


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



<span data-ttu-id="a34af-118">Однако структура, соответствующая этому макету, не определена в заголовках CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a34af-118">However, no structure that matches this layout is defined in the CryptoAPI headers.</span></span> <span data-ttu-id="a34af-119">Можно определить одну или несколько арифметических операций с указателями.</span><span class="sxs-lookup"><span data-stu-id="a34af-119">You can either define one or do some pointer arithmetic.</span></span> <span data-ttu-id="a34af-120">Например, чтобы проверить размер ключа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a34af-120">For example, to verify the size of the key:</span></span>


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



<span data-ttu-id="a34af-121">Чтобы получить указатель на сам ключ, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="a34af-121">To get the pointer to the key itself:</span></span>


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



<span data-ttu-id="a34af-122">Затем создайте 32-разрядное случайное число, которое будет использоваться в качестве начальной последовательности для запросов состояния Копп.</span><span class="sxs-lookup"><span data-stu-id="a34af-122">Next, generate a 32-bit random number to use as the starting sequence for COPP status requests.</span></span> <span data-ttu-id="a34af-123">Рекомендуемый способ создания случайного числа — вызов функции **CryptGenRandom** .</span><span class="sxs-lookup"><span data-stu-id="a34af-123">The recommended way to create a random number is to call the **CryptGenRandom** function.</span></span> <span data-ttu-id="a34af-124">Не используйте функцию **Rand** в библиотеке времени выполнения C, так как она не является действительно случайной.</span><span class="sxs-lookup"><span data-stu-id="a34af-124">Do not use the **rand** function in the C run-time library, because it is not truly random.</span></span> <span data-ttu-id="a34af-125">Создайте второе 32-разрядное случайное число, которое будет использоваться в качестве начальной последовательности команд Копп.</span><span class="sxs-lookup"><span data-stu-id="a34af-125">Generate a second 32-bit random number to use as the starting sequence for COPP commands.</span></span>


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



<span data-ttu-id="a34af-126">Теперь можно подготовить подпись Копп.</span><span class="sxs-lookup"><span data-stu-id="a34af-126">Now you can prepare the COPP signature.</span></span> <span data-ttu-id="a34af-127">Это 256-байтовый массив, определенный как структура [**амкоппсигнатуре**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) .</span><span class="sxs-lookup"><span data-stu-id="a34af-127">This is a 256-byte array, defined as the [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) structure.</span></span> <span data-ttu-id="a34af-128">Инициализирует содержимое массива до нуля.</span><span class="sxs-lookup"><span data-stu-id="a34af-128">Initialize the contents of the array to zero.</span></span> <span data-ttu-id="a34af-129">Затем скопируйте четыре числа в массив — случайное число драйвера, ключ AES, порядковый номер состояния и порядковый номер команды в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="a34af-129">Then copy the four numbers into the array—the driver's random number, the AES key, the status sequence number, and the command sequence number, in that order.</span></span> <span data-ttu-id="a34af-130">Наконец, замените порядок байтов для всего массива.</span><span class="sxs-lookup"><span data-stu-id="a34af-130">Finally, swap the byte order of the entire array.</span></span>

<span data-ttu-id="a34af-131">В соответствии с документацией по **криптенкрипт**:</span><span class="sxs-lookup"><span data-stu-id="a34af-131">According to the documentation for **CryptEncrypt**:</span></span>

<dl> <span data-ttu-id="a34af-132">«Длина данных в виде открытого текста, которую можно зашифровать с помощью вызова **криптенкрипт** с помощью ключа RSA, — это длина модуля ключа минус 11 байт.</span><span class="sxs-lookup"><span data-stu-id="a34af-132">"The length of plaintext data that can be encrypted with a call to **CryptEncrypt** with an RSA key is the length of the key modulus minus eleven bytes.</span></span> <span data-ttu-id="a34af-133">11 байт — это выбранный минимум для заполнения PKCS \# 1.</span><span class="sxs-lookup"><span data-stu-id="a34af-133">The eleven bytes is the chosen minimum for PKCS \#1 padding."</span></span>  
</dl>

<span data-ttu-id="a34af-134">В этом случае значение модуля составляет 256 байт, поэтому максимальная длина сообщения — 245 байт (256 – 11).</span><span class="sxs-lookup"><span data-stu-id="a34af-134">In this case, the modulus is 256 bytes, so the maximum message length is 245 bytes (256 – 11).</span></span> <span data-ttu-id="a34af-135">Структура **амкоппсигнатуре** составляет 256 байт, но значимые данные в сигнатуре — только 40 байт.</span><span class="sxs-lookup"><span data-stu-id="a34af-135">The **AMCOPPSignature** structure is 256 bytes, but the meaningful data in the signature is only 40 bytes.</span></span> <span data-ttu-id="a34af-136">Следующий код шифрует подпись и предоставляет результат в</span><span class="sxs-lookup"><span data-stu-id="a34af-136">The following code encrypts the signature and provides the result in</span></span>


```
CoppSig
```



<span data-ttu-id="a34af-137">.</span><span class="sxs-lookup"><span data-stu-id="a34af-137">.</span></span>


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



<span data-ttu-id="a34af-138">Теперь передайте зашифрованный массив в [**иамцертифиедаутпутпротектион:: сессионсекуенцестарт**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span><span class="sxs-lookup"><span data-stu-id="a34af-138">Now pass the encrypted array to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span></span>


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



<span data-ttu-id="a34af-139">Если этот метод завершился удачно, вы можете отправить драйверу команды Копп и запросы о состоянии.</span><span class="sxs-lookup"><span data-stu-id="a34af-139">If this method succeeds, you are ready to send COPP commands and status requests to the driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a34af-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a34af-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a34af-141">Использование протокола сертифицированной выходной защиты (Копп)</span><span class="sxs-lookup"><span data-stu-id="a34af-141">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



