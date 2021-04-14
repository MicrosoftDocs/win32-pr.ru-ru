---
title: Функция TF_InvalidAssemblyListCacheIfExist
description: Функция TF \_ инвалидассемблилисткачеифексист делает недействительным кэш описания обработчика ввода текста.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- Платформа текстовых служб TF_InvalidAssemblyListCacheIfExist Function
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dd28ab2247fae28af1c5f322832aebe071fab4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533956"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a><span data-ttu-id="729d9-104">TF \_ инвалидассемблилисткачеифексист, функция</span><span class="sxs-lookup"><span data-stu-id="729d9-104">TF\_InvalidAssemblyListCacheIfExist function</span></span>

<span data-ttu-id="729d9-105">Функция **tf \_ инвалидассемблилисткачеифексист** делает недействительным кэш описания обработчика ввода текста.</span><span class="sxs-lookup"><span data-stu-id="729d9-105">The **TF\_InvalidAssemblyListCacheIfExist** function invalidates the text input processor's description cache.</span></span> <span data-ttu-id="729d9-106">Нет необходимости вызывать эту функцию, если для программы установки входного процессора требуется перезагрузка или вход в систему.</span><span class="sxs-lookup"><span data-stu-id="729d9-106">It is not necessary to call this function if the input processor setup program requires you to restart or log on.</span></span> <span data-ttu-id="729d9-107">Кэш действителен до тех пор, пока пользователь не выйдет из системы.</span><span class="sxs-lookup"><span data-stu-id="729d9-107">The cache is valid until the user logs off.</span></span>

## <a name="syntax"></a><span data-ttu-id="729d9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="729d9-108">Syntax</span></span>


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a><span data-ttu-id="729d9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="729d9-109">Parameters</span></span>

<span data-ttu-id="729d9-110">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="729d9-110">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="729d9-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="729d9-111">Return value</span></span>

<span data-ttu-id="729d9-112">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="729d9-112">This function can return one of these values.</span></span>



| <span data-ttu-id="729d9-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="729d9-113">Return code</span></span>                                                                            | <span data-ttu-id="729d9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="729d9-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="729d9-115"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="729d9-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="729d9-116">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="729d9-116">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="729d9-117"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="729d9-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="729d9-118">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="729d9-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="729d9-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="729d9-119">Examples</span></span>

<span data-ttu-id="729d9-120">Нет доступной библиотеки импорта, которая определяет эту функцию, поэтому необходимо получить указатель на эту функцию с помощью [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="729d9-120">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="729d9-121">В следующем примере показано, как получить указатель на эту функцию.</span><span class="sxs-lookup"><span data-stu-id="729d9-121">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="729d9-122">Неправильное использование [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) может нарушить безопасность приложения, загрузив НЕПРАВИЛЬНУЮ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="729d9-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="729d9-123">Сведения о том, как правильно загружать библиотеки DLL с разными версиями Microsoft Windows, см. в статье [Порядок поиска библиотек динамической компоновки](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="729d9-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a><span data-ttu-id="729d9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="729d9-124">Requirements</span></span>



| <span data-ttu-id="729d9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="729d9-125">Requirement</span></span> | <span data-ttu-id="729d9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="729d9-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="729d9-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="729d9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="729d9-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="729d9-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="729d9-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="729d9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="729d9-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="729d9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="729d9-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="729d9-131">Redistributable</span></span><br/>          | <span data-ttu-id="729d9-132">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="729d9-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="729d9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="729d9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="729d9-134"><dt>Msctf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="729d9-134"><dt>Msctf.dll</dt></span></span> </dl> |



 

