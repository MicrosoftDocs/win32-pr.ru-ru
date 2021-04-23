---
description: Возвращает размер массива, который должен быть выделен перед вызовом Креатеопмпротектедаутпутс.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: Функция Жетсугжестедопмпротектедаутпутаррайсизе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 87139f0b485ef3c01e5196db85b36faeb662e4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143093"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a><span data-ttu-id="e559f-103">Функция Жетсугжестедопмпротектедаутпутаррайсизе</span><span class="sxs-lookup"><span data-stu-id="e559f-103">GetSuggestedOPMProtectedOutputArraySize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e559f-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="e559f-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e559f-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="e559f-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e559f-106">Возвращает размер массива, который должен быть выделен перед вызовом [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="e559f-106">Gets the size of the array that should be allocated before calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e559f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e559f-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="e559f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e559f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e559f-109">*пстрдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e559f-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e559f-110">Указатель на [**\_ строковую структуру Юникода**](/windows/win32/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e559f-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="e559f-111">*пдвсугжестедопмпротектедаутпутаррайсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e559f-111">*pdwSuggestedOPMProtectedOutputArraySize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e559f-112">Получает размер, который должен быть выделен для массива, в количестве элементов массива.</span><span class="sxs-lookup"><span data-stu-id="e559f-112">Receives the size that should be allocated for the array, in number of array elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e559f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e559f-113">Return value</span></span>

<span data-ttu-id="e559f-114">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="e559f-114">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e559f-115">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e559f-115">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e559f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e559f-116">Remarks</span></span>

<span data-ttu-id="e559f-117">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="e559f-117">This function has no associated import library.</span></span> <span data-ttu-id="e559f-118">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e559f-118">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e559f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e559f-119">Requirements</span></span>



| <span data-ttu-id="e559f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e559f-120">Requirement</span></span> | <span data-ttu-id="e559f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e559f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e559f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e559f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e559f-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e559f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e559f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e559f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e559f-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e559f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e559f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e559f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e559f-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e559f-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e559f-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e559f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e559f-129">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="e559f-129">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e559f-130">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="e559f-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
