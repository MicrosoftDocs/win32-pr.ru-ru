---
description: IWICStream_InitializeFromMemory_Proxy функция-прокси для метода Инитиализефроммемори.
ms.assetid: 737526ac-fe79-4d53-83c5-33102f5ac67b
title: Функция IWICStream_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: be3cec08f2ad3970d8860803cfb70970cf7b765b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097132"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="82a21-103">Ивикстреам \_ инитиализефроммемори \_ -функция</span><span class="sxs-lookup"><span data-stu-id="82a21-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="82a21-104">Функция-посредник для метода [**инитиализефроммемори**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="82a21-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82a21-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82a21-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="82a21-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82a21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a21-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="82a21-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a21-108">Тип: **[ **ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span><span class="sxs-lookup"><span data-stu-id="82a21-108">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\***</span></span>

<span data-ttu-id="82a21-109">Указатель на этот объект [**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="82a21-109">Pointer to this [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="82a21-110">*пббуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82a21-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a21-111">Тип: **Byte \***</span><span class="sxs-lookup"><span data-stu-id="82a21-111">Type: **BYTE\***</span></span>

<span data-ttu-id="82a21-112">Указатель на буфер, используемый для инициализации потока.</span><span class="sxs-lookup"><span data-stu-id="82a21-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="82a21-113">*кббуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="82a21-113">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82a21-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="82a21-114">Type: **DWORD**</span></span>

<span data-ttu-id="82a21-115">Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="82a21-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82a21-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82a21-116">Return value</span></span>

<span data-ttu-id="82a21-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="82a21-117">Type: **HRESULT**</span></span>

<span data-ttu-id="82a21-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="82a21-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="82a21-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="82a21-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="82a21-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="82a21-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="82a21-121">Требования</span><span class="sxs-lookup"><span data-stu-id="82a21-121">Requirements</span></span>



| <span data-ttu-id="82a21-122">Требование</span><span class="sxs-lookup"><span data-stu-id="82a21-122">Requirement</span></span> | <span data-ttu-id="82a21-123">Значение</span><span class="sxs-lookup"><span data-stu-id="82a21-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82a21-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82a21-124">Minimum supported client</span></span><br/> | <span data-ttu-id="82a21-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82a21-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="82a21-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82a21-126">Minimum supported server</span></span><br/> | <span data-ttu-id="82a21-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82a21-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="82a21-128">DLL</span><span class="sxs-lookup"><span data-stu-id="82a21-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82a21-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82a21-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




