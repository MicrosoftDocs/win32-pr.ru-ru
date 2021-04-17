---
description: Создает экземпляр подсистемы захвата.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Функция Мфкреатекаптурингине
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711278"
---
# <a name="mfcreatecaptureengine-function"></a><span data-ttu-id="0f3fe-103">Функция Мфкреатекаптурингине</span><span class="sxs-lookup"><span data-stu-id="0f3fe-103">MFCreateCaptureEngine function</span></span>

<span data-ttu-id="0f3fe-104">\[Мфкреатекаптурингине не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-104">\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="0f3fe-105">\]</span><span class="sxs-lookup"><span data-stu-id="0f3fe-105">\]</span></span>

<span data-ttu-id="0f3fe-106">Создает экземпляр подсистемы захвата.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-106">Creates an instance of the capture engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3fe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f3fe-107">Syntax</span></span>


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a><span data-ttu-id="0f3fe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0f3fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3fe-109">*ппкаптурингине* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0f3fe-109">*ppCaptureEngine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3fe-110">Получает указатель на интерфейс [**имфкаптурингине**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) .</span><span class="sxs-lookup"><span data-stu-id="0f3fe-110">Receives a pointer to the [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) interface.</span></span> <span data-ttu-id="0f3fe-111">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-111">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f3fe-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0f3fe-112">Return value</span></span>

<span data-ttu-id="0f3fe-113">Если функция завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-113">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="0f3fe-114">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f3fe-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f3fe-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f3fe-115">Remarks</span></span>

<span data-ttu-id="0f3fe-116">Эта функция не имеет связанной библиотеки импорта и не объявлена в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="0f3fe-116">This function has no associated import library and is not declared in a public header file.</span></span> <span data-ttu-id="0f3fe-117">Для динамической привязки к MFCaptureEngine.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0f3fe-117">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to MFCaptureEngine.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f3fe-118">Требования</span><span class="sxs-lookup"><span data-stu-id="0f3fe-118">Requirements</span></span>



| <span data-ttu-id="0f3fe-119">Требование</span><span class="sxs-lookup"><span data-stu-id="0f3fe-119">Requirement</span></span> | <span data-ttu-id="0f3fe-120">Значение</span><span class="sxs-lookup"><span data-stu-id="0f3fe-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3fe-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f3fe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3fe-122">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0f3fe-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0f3fe-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f3fe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3fe-124">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f3fe-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f3fe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3fe-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3fe-126"><dt>MFCaptureEngine.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3fe-126"><dt>MFCaptureEngine.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f3fe-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f3fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3fe-128">Функции Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f3fe-128">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
