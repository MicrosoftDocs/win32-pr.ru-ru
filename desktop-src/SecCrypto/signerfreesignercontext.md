---
description: Освобождает \_ структуру контекста подписи, выделенную предыдущим вызовом функции сигнерсигнекс.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: Функция Сигнерфрисигнерконтекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663811"
---
# <a name="signerfreesignercontext-function"></a><span data-ttu-id="7392c-103">Функция Сигнерфрисигнерконтекст</span><span class="sxs-lookup"><span data-stu-id="7392c-103">SignerFreeSignerContext function</span></span>

<span data-ttu-id="7392c-104">Функция **сигнерфрисигнерконтекст** освобождает структуру [**\_ контекста подписи**](signer-context.md) , выделенную предыдущим вызовом функции [**сигнерсигнекс**](signersignex.md) .</span><span class="sxs-lookup"><span data-stu-id="7392c-104">The **SignerFreeSignerContext** function frees a [**SIGNER\_CONTEXT**](signer-context.md) structure allocated by a previous call to the [**SignerSignEx**](signersignex.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="7392c-105">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="7392c-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="7392c-106">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="7392c-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7392c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7392c-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="7392c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7392c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7392c-109">*псигнерконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7392c-109">*pSignerContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7392c-110">Указатель на структуру [**\_ контекста подписи**](signer-context.md) для освобождения.</span><span class="sxs-lookup"><span data-stu-id="7392c-110">A pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7392c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7392c-111">Return value</span></span>

<span data-ttu-id="7392c-112">Если функция завершается успешно, функция возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="7392c-112">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="7392c-113">Если функция завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="7392c-113">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="7392c-114">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="7392c-114">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7392c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="7392c-115">Requirements</span></span>



| <span data-ttu-id="7392c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="7392c-116">Requirement</span></span> | <span data-ttu-id="7392c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7392c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7392c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7392c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7392c-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7392c-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7392c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7392c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7392c-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7392c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7392c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7392c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7392c-123"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7392c-123"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7392c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7392c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7392c-125">**контекст подписи \_**</span><span class="sxs-lookup"><span data-stu-id="7392c-125">**SIGNER\_CONTEXT**</span></span>](signer-context.md)
</dt> <dt>

[<span data-ttu-id="7392c-126">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="7392c-126">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
