---
description: Функция-посредник для метода Инитиализефроммемори.
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
ms.openlocfilehash: fe034698635a35c098f6466712d17489f301dd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713119"
---
# <a name="iwicstream_initializefrommemory_proxy-function"></a><span data-ttu-id="896a4-103">Ивикстреам \_ инитиализефроммемори \_ -функция</span><span class="sxs-lookup"><span data-stu-id="896a4-103">IWICStream\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="896a4-104">Функция-посредник для метода [**инитиализефроммемори**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="896a4-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="896a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="896a4-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromMemory_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ BYTE       *pbBuffer,
  _In_ DWORD      cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="896a4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="896a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="896a4-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="896a4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896a4-108">Тип: \**[**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="896a4-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="896a4-109">Указатель на этот объект [_ *ивикстреам* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="896a4-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="896a4-110">*пббуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="896a4-110">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896a4-111">Тип: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="896a4-111">Type: \**BYTE\** _</span></span>

<span data-ttu-id="896a4-112">Указатель на буфер, используемый для инициализации потока.</span><span class="sxs-lookup"><span data-stu-id="896a4-112">Pointer to the buffer used to initialize the stream.</span></span>

</dd> <dt>

<span data-ttu-id="896a4-113">_cbBufferSize \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="896a4-113">_cbBufferSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="896a4-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="896a4-114">Type: **DWORD**</span></span>

<span data-ttu-id="896a4-115">Размер буфера.</span><span class="sxs-lookup"><span data-stu-id="896a4-115">The size of buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="896a4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="896a4-116">Return value</span></span>

<span data-ttu-id="896a4-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="896a4-117">Type: **HRESULT**</span></span>

<span data-ttu-id="896a4-118">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="896a4-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="896a4-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="896a4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="896a4-120">Remarks</span><span class="sxs-lookup"><span data-stu-id="896a4-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="896a4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="896a4-121">Requirements</span></span>



| <span data-ttu-id="896a4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="896a4-122">Requirement</span></span> | <span data-ttu-id="896a4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="896a4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="896a4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="896a4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="896a4-125">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="896a4-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="896a4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="896a4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="896a4-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="896a4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="896a4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="896a4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="896a4-129"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="896a4-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




