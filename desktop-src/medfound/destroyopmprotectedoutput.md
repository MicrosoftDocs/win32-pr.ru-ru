---
description: Освобождает защищенный выходной объект.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: Функция Дестройопмпротектедаутпут
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682372"
---
# <a name="destroyopmprotectedoutput-function"></a><span data-ttu-id="d1a78-103">Функция Дестройопмпротектедаутпут</span><span class="sxs-lookup"><span data-stu-id="d1a78-103">DestroyOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1a78-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="d1a78-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="d1a78-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d1a78-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="d1a78-106">Освобождает защищенный выходной объект.</span><span class="sxs-lookup"><span data-stu-id="d1a78-106">Releases a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a78-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1a78-107">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a><span data-ttu-id="d1a78-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1a78-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a78-109">*опупмпротектедаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1a78-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1a78-110">Маркер защищенного выходного объекта.</span><span class="sxs-lookup"><span data-stu-id="d1a78-110">A handle to the protected output object.</span></span> <span data-ttu-id="d1a78-111">Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="d1a78-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a78-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1a78-112">Return value</span></span>

<span data-ttu-id="d1a78-113">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="d1a78-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d1a78-114">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="d1a78-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1a78-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1a78-115">Remarks</span></span>

<span data-ttu-id="d1a78-116">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="d1a78-116">This function has no associated import library.</span></span> <span data-ttu-id="d1a78-117">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="d1a78-117">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a78-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d1a78-118">Requirements</span></span>



| <span data-ttu-id="d1a78-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d1a78-119">Requirement</span></span> | <span data-ttu-id="d1a78-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a78-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a78-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1a78-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a78-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1a78-122">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d1a78-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1a78-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a78-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1a78-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d1a78-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1a78-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1a78-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1a78-126"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a78-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1a78-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a78-128">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="d1a78-128">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="d1a78-129">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="d1a78-129">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
