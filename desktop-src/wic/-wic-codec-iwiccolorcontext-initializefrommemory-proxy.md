---
description: Функция-посредник для метода Инитиализефроммемори.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: Функция IWICColorContext_InitializeFromMemory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 32c3c24902b6c3157b9776d84c5a8eea47cce43e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702398"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a><span data-ttu-id="7502c-103">Ивикколорконтекст \_ инитиализефроммемори \_ -функция</span><span class="sxs-lookup"><span data-stu-id="7502c-103">IWICColorContext\_InitializeFromMemory\_Proxy function</span></span>

<span data-ttu-id="7502c-104">Функция-посредник для метода [**инитиализефроммемори**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="7502c-104">Proxy function for the [**InitializeFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7502c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7502c-105">Syntax</span></span>


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="7502c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7502c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7502c-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="7502c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7502c-108">Тип: \**[**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) \** _</span><span class="sxs-lookup"><span data-stu-id="7502c-108">Type: \**[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\** _</span></span>

</dd> <dt>

<span data-ttu-id="7502c-109">_pbBuffer \* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="7502c-109">_pbBuffer\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7502c-110">Тип: \**const байт \** _</span><span class="sxs-lookup"><span data-stu-id="7502c-110">Type: \**const BYTE\** _</span></span>

<span data-ttu-id="7502c-111">Буфер, используемый для инициализации [_ *ивикколорконтекст* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span><span class="sxs-lookup"><span data-stu-id="7502c-111">The buffer used to initialize the [_ *IWICColorContext*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="7502c-112">*кббуфферсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7502c-112">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7502c-113">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="7502c-113">Type: **UINT**</span></span>

<span data-ttu-id="7502c-114">Размер буфера *пббуффер* .</span><span class="sxs-lookup"><span data-stu-id="7502c-114">The size of the *pbBuffer* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7502c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7502c-115">Return value</span></span>

<span data-ttu-id="7502c-116">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7502c-116">Type: **HRESULT**</span></span>

<span data-ttu-id="7502c-117">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7502c-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7502c-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7502c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7502c-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="7502c-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7502c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7502c-120">Requirements</span></span>



| <span data-ttu-id="7502c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7502c-121">Requirement</span></span> | <span data-ttu-id="7502c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7502c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7502c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7502c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7502c-124">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7502c-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="7502c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7502c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7502c-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7502c-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="7502c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7502c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7502c-128"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7502c-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




