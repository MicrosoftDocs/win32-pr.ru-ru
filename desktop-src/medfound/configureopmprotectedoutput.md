---
description: Настраивает защищенный выходной объект.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: Функция Конфигуреопмпротектедаутпут
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423566"
---
# <a name="configureopmprotectedoutput-function"></a><span data-ttu-id="8e3a2-103">Функция Конфигуреопмпротектедаутпут</span><span class="sxs-lookup"><span data-stu-id="8e3a2-103">ConfigureOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e3a2-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="8e3a2-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="8e3a2-106">Настраивает защищенный выходной объект.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-106">Configures a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e3a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e3a2-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a><span data-ttu-id="8e3a2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e3a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e3a2-109">*опупмпротектедаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a2-110">Маркер защищенного выходного объекта.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-110">A handle to the protected output object.</span></span> <span data-ttu-id="8e3a2-111">Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="8e3a2-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e3a2-112">*ппараметерс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a2-113">Указатель на **дксгкмдт \_ ОПМ Настройка структуры \_ \_ параметров** , которая содержит команду конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-113">A pointer to a **DXGKMDT\_OPM\_CONFIGURE\_PARAMETERS** structure that contains the configuration command.</span></span>

</dd> <dt>

<span data-ttu-id="8e3a2-114">*уладдитионалпараметерссизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-114">*ulAdditionalParametersSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a2-115">Размер буфера *пбаддитионалпараметерс* в байтах.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-115">The size of the *pbAdditionalParameters* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8e3a2-116">*пбаддитионалпараметерс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-116">*pbAdditionalParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e3a2-117">Указатель на буфер, содержащий дополнительные сведения о команде.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-117">A pointer to a buffer that contains additional information for the command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e3a2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e3a2-118">Return value</span></span>

<span data-ttu-id="8e3a2-119">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="8e3a2-120">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="8e3a2-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e3a2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e3a2-121">Remarks</span></span>

<span data-ttu-id="8e3a2-122">Приложения должны вызывать метод [**иопмвидеуутпут:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-122">Applications should call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) instead of calling this function.</span></span>

<span data-ttu-id="8e3a2-123">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-123">This function has no associated import library.</span></span> <span data-ttu-id="8e3a2-124">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="8e3a2-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e3a2-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8e3a2-125">Requirements</span></span>



| <span data-ttu-id="8e3a2-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8e3a2-126">Requirement</span></span> | <span data-ttu-id="8e3a2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8e3a2-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8e3a2-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e3a2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8e3a2-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8e3a2-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e3a2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8e3a2-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e3a2-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8e3a2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8e3a2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e3a2-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e3a2-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e3a2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e3a2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e3a2-135">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="8e3a2-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="8e3a2-136">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="8e3a2-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
