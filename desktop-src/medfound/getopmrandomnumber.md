---
description: Возвращает 128-битное криптографически защищенное случайное число из защищенного выходного объекта.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: Функция Жетопмрандомнумбер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342452"
---
# <a name="getopmrandomnumber-function"></a><span data-ttu-id="46822-103">Функция Жетопмрандомнумбер</span><span class="sxs-lookup"><span data-stu-id="46822-103">GetOPMRandomNumber function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46822-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="46822-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="46822-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="46822-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="46822-106">Возвращает 128-битное криптографически защищенное случайное число из защищенного выходного объекта.</span><span class="sxs-lookup"><span data-stu-id="46822-106">Gets a 128-bit, cryptographically secure random number from a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="46822-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46822-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a><span data-ttu-id="46822-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46822-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46822-109">*опупмпротектедаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46822-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46822-110">Маркер защищенного выходного объекта.</span><span class="sxs-lookup"><span data-stu-id="46822-110">A handle to the protected output object.</span></span> <span data-ttu-id="46822-111">Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="46822-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="46822-112">*прнрандомнумбер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="46822-112">*prnRandomNumber* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46822-113">Указатель на структуру **\_ \_ случайных \_ чисел дксгкмдт ОПМ** , которая получает случайное число.</span><span class="sxs-lookup"><span data-stu-id="46822-113">A pointer to a **DXGKMDT\_OPM\_RANDOM\_NUMBER** structure that receives the random number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46822-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46822-114">Return value</span></span>

<span data-ttu-id="46822-115">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="46822-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="46822-116">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="46822-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="46822-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46822-117">Remarks</span></span>

<span data-ttu-id="46822-118">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="46822-118">This function has no associated import library.</span></span> <span data-ttu-id="46822-119">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="46822-119">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="46822-120">Требования</span><span class="sxs-lookup"><span data-stu-id="46822-120">Requirements</span></span>



| <span data-ttu-id="46822-121">Требование</span><span class="sxs-lookup"><span data-stu-id="46822-121">Requirement</span></span> | <span data-ttu-id="46822-122">Значение</span><span class="sxs-lookup"><span data-stu-id="46822-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="46822-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46822-123">Minimum supported client</span></span><br/> | <span data-ttu-id="46822-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46822-124">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="46822-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46822-125">Minimum supported server</span></span><br/> | <span data-ttu-id="46822-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46822-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="46822-127">DLL</span><span class="sxs-lookup"><span data-stu-id="46822-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46822-128"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46822-128"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46822-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46822-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46822-130">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="46822-130">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="46822-131">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="46822-131">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
