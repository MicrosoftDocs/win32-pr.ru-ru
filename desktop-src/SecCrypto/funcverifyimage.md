---
description: Используется поставщиком служб шифрования (CSP) для проверки подписи библиотеки DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: Указатель функции CRYPT_VERIFY_IMAGE (Кспдк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683504"
---
# <a name="crypt_verify_image-function-pointer"></a><span data-ttu-id="676c2-103">\_Проверка шифрования \_ указатель функции изображения</span><span class="sxs-lookup"><span data-stu-id="676c2-103">CRYPT\_VERIFY\_IMAGE function pointer</span></span>

<span data-ttu-id="676c2-104">Функция обратного вызова **функверифимаже** используется [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) для проверки подписи библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="676c2-104">The **FuncVerifyImage** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to verify the signature of a DLL.</span></span>

<span data-ttu-id="676c2-105">Все вспомогательные библиотеки DLL, в которые CSP вызывает вызовы функций, должны быть подписаны аналогичным образом (и с тем же ключом), что и первичная библиотека CSP.</span><span class="sxs-lookup"><span data-stu-id="676c2-105">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="676c2-106">Чтобы обеспечить эту сигнатуру, вспомогательные библиотеки DLL должны динамически загружаться с помощью функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="676c2-106">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="676c2-107">Но перед загрузкой библиотеки DLL необходимо проверить подпись библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="676c2-107">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="676c2-108">CSP выполняет эту проверку, вызывая функцию **функверифимаже** , как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="676c2-108">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

## <a name="syntax"></a><span data-ttu-id="676c2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="676c2-109">Syntax</span></span>


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a><span data-ttu-id="676c2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="676c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="676c2-111">*лпсзимаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="676c2-111">*lpszImage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="676c2-112">Адрес строки, завершающейся нулем, которая содержит путь и имя файла библиотеки DLL для проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="676c2-112">The address of a null-terminated string that contains the path and file name of the DLL to verify the signature for.</span></span>

</dd> <dt>

<span data-ttu-id="676c2-113">*пбсигдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="676c2-113">*pbSigData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="676c2-114">Адрес буфера, содержащего подпись.</span><span class="sxs-lookup"><span data-stu-id="676c2-114">The address of a buffer that contains the signature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="676c2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="676c2-115">Return value</span></span>

<span data-ttu-id="676c2-116">Возвращает **значение true** , если функция завершается успешно, в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="676c2-116">Returns **TRUE** if the function succeeds, **FALSE** if it fails.</span></span>

## <a name="examples"></a><span data-ttu-id="676c2-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="676c2-117">Examples</span></span>

<span data-ttu-id="676c2-118">В следующем примере показано, как использовать функцию обратного вызова **функверифимаже** для проверки подписи библиотеки DLL перед ее загрузкой CSP.</span><span class="sxs-lookup"><span data-stu-id="676c2-118">The following example shows how to use the **FuncVerifyImage** callback function to verify the signature of a DLL before it is loaded by a CSP.</span></span>


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a><span data-ttu-id="676c2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="676c2-119">Requirements</span></span>



| <span data-ttu-id="676c2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="676c2-120">Requirement</span></span> | <span data-ttu-id="676c2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="676c2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="676c2-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="676c2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="676c2-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="676c2-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="676c2-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="676c2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="676c2-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="676c2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="676c2-126">Header</span><span class="sxs-lookup"><span data-stu-id="676c2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="676c2-127"><dt>Кспдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="676c2-127"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="676c2-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="676c2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="676c2-129">**кпаккуиреконтекст**</span><span class="sxs-lookup"><span data-stu-id="676c2-129">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="676c2-130">**втаблепровструк**</span><span class="sxs-lookup"><span data-stu-id="676c2-130">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
