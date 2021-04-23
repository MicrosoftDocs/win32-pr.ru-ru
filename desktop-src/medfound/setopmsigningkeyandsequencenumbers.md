---
description: Задает ключ подписи и два порядковых номера для защищенного выходного объекта.
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: Функция Сетопмсигнингкэйандсекуенценумберс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263487"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a><span data-ttu-id="3a05a-103">Функция Сетопмсигнингкэйандсекуенценумберс</span><span class="sxs-lookup"><span data-stu-id="3a05a-103">SetOPMSigningKeyAndSequenceNumbers function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a05a-104">Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера.</span><span class="sxs-lookup"><span data-stu-id="3a05a-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="3a05a-105">Приложения не должны вызывать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="3a05a-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="3a05a-106">Задает ключ подписи и два порядковых номера для защищенного выходного объекта.</span><span class="sxs-lookup"><span data-stu-id="3a05a-106">Sets the signing key and two sequence numbers on a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a05a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a05a-107">Syntax</span></span>


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="3a05a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a05a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a05a-109">*опупмпротектедаутпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3a05a-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a05a-110">Маркер защищенного выходного объекта.</span><span class="sxs-lookup"><span data-stu-id="3a05a-110">A handle to the protected output object.</span></span> <span data-ttu-id="3a05a-111">Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="3a05a-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="3a05a-112">*ппараметерс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3a05a-112">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a05a-113">Указатель на структуру [**\_ \_ зашифрованных \_ параметров дксгкмдт ОПМ**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) , которая содержит массив из 256 байт.</span><span class="sxs-lookup"><span data-stu-id="3a05a-113">A pointer to a [**DXGKMDT\_OPM\_ENCRYPTED\_PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) structure that contains a 256-byte array.</span></span> <span data-ttu-id="3a05a-114">Дополнительные сведения об инициализации этого массива см. в разделе [дксгкддиопмсетсигнингкэйандсекуенценумберс](https://msdn.microsoft.com/library/aa906703.aspx).</span><span class="sxs-lookup"><span data-stu-id="3a05a-114">For more information about how to initialize this array, see [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a05a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a05a-115">Return value</span></span>

<span data-ttu-id="3a05a-116">Если метод завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="3a05a-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="3a05a-117">В противном случае возвращается код ошибки **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="3a05a-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a05a-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a05a-118">Remarks</span></span>

<span data-ttu-id="3a05a-119">Приложения должны вызывать метод [**иопмвидеуутпут:: финишинитиализатион**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) вместо вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="3a05a-119">Applications should call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) instead of calling this function.</span></span>

<span data-ttu-id="3a05a-120">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="3a05a-120">This function has no associated import library.</span></span> <span data-ttu-id="3a05a-121">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="3a05a-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a05a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3a05a-122">Requirements</span></span>



| <span data-ttu-id="3a05a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3a05a-123">Requirement</span></span> | <span data-ttu-id="3a05a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3a05a-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3a05a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a05a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3a05a-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a05a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3a05a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a05a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3a05a-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a05a-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3a05a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3a05a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a05a-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a05a-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a05a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a05a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a05a-132">Функции ОПМ</span><span class="sxs-lookup"><span data-stu-id="3a05a-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="3a05a-133">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="3a05a-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
