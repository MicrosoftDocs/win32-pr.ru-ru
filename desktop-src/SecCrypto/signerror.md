---
description: Вызывает функцию GetLastError и преобразует код возврата в значение HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: Функция Сигнеррор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072809"
---
# <a name="signerror-function"></a><span data-ttu-id="c3bbd-103">Функция Сигнеррор</span><span class="sxs-lookup"><span data-stu-id="c3bbd-103">SignError function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3bbd-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-104">This API is deprecated.</span></span> <span data-ttu-id="c3bbd-105">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="c3bbd-106">Функция **сигнеррор** вызывает функцию [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) и преобразует код возврата в **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-106">The **SignError** function calls the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and converts the return code to an **HRESULT**.</span></span>

> [!Note]  
> <span data-ttu-id="c3bbd-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="c3bbd-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c3bbd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3bbd-109">Syntax</span></span>


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a><span data-ttu-id="c3bbd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3bbd-110">Parameters</span></span>

<span data-ttu-id="c3bbd-111">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3bbd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3bbd-112">Return value</span></span>

<span data-ttu-id="c3bbd-113">Если метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-113">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="c3bbd-114">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="c3bbd-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="c3bbd-115">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="c3bbd-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3bbd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c3bbd-116">Requirements</span></span>



| <span data-ttu-id="c3bbd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c3bbd-117">Requirement</span></span> | <span data-ttu-id="c3bbd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c3bbd-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3bbd-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3bbd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c3bbd-120">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c3bbd-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c3bbd-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3bbd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c3bbd-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3bbd-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c3bbd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c3bbd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3bbd-124"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3bbd-124"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
