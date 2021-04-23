---
description: Отправляет запрос о состоянии сертифицированного протокола выходной защиты (Копп) в защищенный выходной объект.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: Функция Жеткоппкомпатиблеопминформатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262787"
---
# <a name="getcoppcompatibleopminformation-function"></a><span data-ttu-id="d2530-103">Функция Жеткоппкомпатиблеопминформатион</span><span class="sxs-lookup"><span data-stu-id="d2530-103">GetCOPPCompatibleOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2530-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="d2530-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="d2530-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d2530-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="d2530-106">Отправляет запрос о состоянии сертифицированного протокола выходной защиты (Копп) в защищенный выходной объект.</span><span class="sxs-lookup"><span data-stu-id="d2530-106">Sends a Certified Output Protection Protocol (COPP) status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2530-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2530-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="d2530-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2530-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2530-109">*опупмпротектедаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2530-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2530-110">Маркер защищенного выходного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2530-110">A handle to the protected output object.</span></span> <span data-ttu-id="d2530-111">Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="d2530-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2530-112">*ппараметерс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d2530-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2530-113">Указатель на **дксгкмдт ОПМ, \_ совместимый с Копп, содержит структуру \_ \_ \_ \_ \_ параметров получения сведений** , содержащую входные данные для запроса состояния.</span><span class="sxs-lookup"><span data-stu-id="d2530-113">A pointer to a **DXGKMDT\_OPM\_COPP\_COMPATIBLE\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="d2530-114">*прекуестединформатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d2530-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2530-115">Указатель на **дксгкмдт ОПМ структуру \_ \_ \_ информации** , которая получает результаты запроса состояния.</span><span class="sxs-lookup"><span data-stu-id="d2530-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2530-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2530-116">Return value</span></span>

<span data-ttu-id="d2530-117">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="d2530-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="d2530-118">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="d2530-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2530-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2530-119">Remarks</span></span>

<span data-ttu-id="d2530-120">Приложения должны вызывать метод [**иопмвидеуутпут:: коппкомпатиблежетинформатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="d2530-120">Applications should call [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) instead of calling this function.</span></span>

<span data-ttu-id="d2530-121">Защищенный выходной объект должен быть создан с семантикой Копп.</span><span class="sxs-lookup"><span data-stu-id="d2530-121">The protected output object must be created with COPP semantics.</span></span> <span data-ttu-id="d2530-122">См. [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="d2530-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="d2530-123">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="d2530-123">This function has no associated import library.</span></span> <span data-ttu-id="d2530-124">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="d2530-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2530-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d2530-125">Requirements</span></span>



| <span data-ttu-id="d2530-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d2530-126">Requirement</span></span> | <span data-ttu-id="d2530-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d2530-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d2530-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2530-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d2530-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2530-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d2530-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2530-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d2530-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2530-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d2530-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d2530-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2530-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2530-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2530-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2530-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2530-135">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="d2530-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="d2530-136">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="d2530-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
