---
description: Создает защищенные выходные объекты для устройства вывода.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Функция Креатеопмпротектедаутпутс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539617"
---
# <a name="createopmprotectedoutputs-function"></a><span data-ttu-id="ed602-103">Функция Креатеопмпротектедаутпутс</span><span class="sxs-lookup"><span data-stu-id="ed602-103">CreateOPMProtectedOutputs function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed602-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="ed602-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="ed602-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="ed602-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="ed602-106">Создает защищенные выходные объекты для устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="ed602-106">Creates protected output objects for a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed602-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed602-107">Syntax</span></span>


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a><span data-ttu-id="ed602-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed602-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed602-109">*пстрдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed602-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed602-110">Указатель на [**\_ строковую структуру Юникода**](/windows/win32/api/subauth/ns-subauth-unicode_string) , содержащую имя устройства вывода, которое возвращается функцией [**жетмониторинфо**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ed602-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="ed602-111">*вос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed602-111">*vos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed602-112">Член перечисления **\_ \_ \_ \_ семантики вывода видео дксгкмдт ОПМ** , указывающий, будет ли защищенный выход иметь семантику (Копп) или семантику ОПМ.</span><span class="sxs-lookup"><span data-stu-id="ed602-112">A member of the **DXGKMDT\_OPM\_VIDEO\_OUTPUT\_SEMANTICS** enumeration, specifying whether the protected output will have Certified Output Protection Protocol (COPP) semantics or OPM semantics.</span></span>

</dd> <dt>

<span data-ttu-id="ed602-113">*двопмпротектедаутпутаррайсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ed602-113">*dwOPMProtectedOutputArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed602-114">Число элементов в массиве *похопмпротектедаутпутаррай* .</span><span class="sxs-lookup"><span data-stu-id="ed602-114">The number of elements in the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="ed602-115">*пдвнумопмпротектедаутпутсинаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ed602-115">*pdwNumOPMProtectedOutputsInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed602-116">Получает число элементов, которые функция копирует в массив *похопмпротектедаутпутаррай* .</span><span class="sxs-lookup"><span data-stu-id="ed602-116">Receives the number of items that the function copies to the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="ed602-117">*похопмпротектедаутпутаррай* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ed602-117">*pohOPMProtectedOutputArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed602-118">Массив, который получает дескрипторы для защищенных выходных объектов.</span><span class="sxs-lookup"><span data-stu-id="ed602-118">An array that receives handles to the protected output objects.</span></span> <span data-ttu-id="ed602-119">Каждый обработчик должен быть освобожден путем вызова [**дестройопмпротектедаутпут**](destroyopmprotectedoutput.md).</span><span class="sxs-lookup"><span data-stu-id="ed602-119">Each handle must be released by calling [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed602-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed602-120">Return value</span></span>

<span data-ttu-id="ed602-121">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="ed602-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="ed602-122">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="ed602-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed602-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed602-123">Remarks</span></span>

<span data-ttu-id="ed602-124">Вместо использования этой функции приложения должны вызывать одну из следующих функций:</span><span class="sxs-lookup"><span data-stu-id="ed602-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="ed602-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="ed602-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [<span data-ttu-id="ed602-126">**опмжетвидеуутпутсфромхмонитор**</span><span class="sxs-lookup"><span data-stu-id="ed602-126">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

<span data-ttu-id="ed602-127">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="ed602-127">This function has no associated import library.</span></span> <span data-ttu-id="ed602-128">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="ed602-128">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed602-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ed602-129">Requirements</span></span>



| <span data-ttu-id="ed602-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ed602-130">Requirement</span></span> | <span data-ttu-id="ed602-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ed602-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed602-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed602-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ed602-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed602-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ed602-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed602-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ed602-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed602-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ed602-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ed602-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed602-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed602-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed602-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed602-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed602-139">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="ed602-139">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="ed602-140">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="ed602-140">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
