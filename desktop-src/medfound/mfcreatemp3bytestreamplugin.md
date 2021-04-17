---
description: Создает обработчик потока байтов для источника мультимедиа MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: Функция MFCreateMP3ByteStreamPlugin
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656549"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a><span data-ttu-id="bdd7c-103">Функция MFCreateMP3ByteStreamPlugin</span><span class="sxs-lookup"><span data-stu-id="bdd7c-103">MFCreateMP3ByteStreamPlugin function</span></span>

<span data-ttu-id="bdd7c-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-104">\[This API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bdd7c-105">Вместо этого приложения должны использовать [сопоставитель источников](source-resolver.md) для создания источника мультимедиа в формате MP3.\]</span><span class="sxs-lookup"><span data-stu-id="bdd7c-105">Instead, applications should use the [Source Resolver](source-resolver.md) to create the MP3 media source.\]</span></span>

<span data-ttu-id="bdd7c-106">Создает обработчик потока байтов для источника мультимедиа MP3.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-106">Creates a byte-stream handler for the MP3 media source.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd7c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdd7c-107">Syntax</span></span>


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a><span data-ttu-id="bdd7c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdd7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdd7c-109">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bdd7c-109">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd7c-110">Идентификатор IID запрошенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-110">The interface identifier (IID) of the requested interface.</span></span> <span data-ttu-id="bdd7c-111">Задайте для этого параметра значение **IID \_ имфбитестреамхандлер** , чтобы получить указатель на интерфейс [**имфбитестреамхандлер**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .</span><span class="sxs-lookup"><span data-stu-id="bdd7c-111">Set this parameter to **IID\_IMFByteStreamHandler** to receive a pointer to the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span>

</dd> <dt>

<span data-ttu-id="bdd7c-112">*ппвхандлер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bdd7c-112">*ppvHandler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdd7c-113">Получает указатель на интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-113">Receives a pointer to the interface.</span></span> <span data-ttu-id="bdd7c-114">Вызывающий объект должен освободить интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-114">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdd7c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdd7c-115">Return value</span></span>

<span data-ttu-id="bdd7c-116">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bdd7c-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bdd7c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdd7c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdd7c-118">Remarks</span></span>

<span data-ttu-id="bdd7c-119">Эта функция не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-119">This function has no associated import library.</span></span> <span data-ttu-id="bdd7c-120">Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к mf.dll.</span><span class="sxs-lookup"><span data-stu-id="bdd7c-120">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to mf.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd7c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="bdd7c-121">Requirements</span></span>



| <span data-ttu-id="bdd7c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="bdd7c-122">Requirement</span></span> | <span data-ttu-id="bdd7c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="bdd7c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bdd7c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdd7c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bdd7c-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bdd7c-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bdd7c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdd7c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bdd7c-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bdd7c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bdd7c-128">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bdd7c-128">End of client support</span></span><br/>    | <span data-ttu-id="bdd7c-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bdd7c-129">Windows Vista</span></span><br/>                             |
| <span data-ttu-id="bdd7c-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="bdd7c-130">End of server support</span></span><br/>    | <span data-ttu-id="bdd7c-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdd7c-131">Windows Server 2008</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="bdd7c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdd7c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd7c-133">Функции Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bdd7c-133">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> <dt>

[<span data-ttu-id="bdd7c-134">Обработчики схем и обработчики Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="bdd7c-134">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="bdd7c-135">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="bdd7c-135">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
