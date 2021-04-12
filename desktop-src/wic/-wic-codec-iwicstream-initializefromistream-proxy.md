---
description: Функция-посредник для метода Инитиализефромистреам.
ms.assetid: 3ab780bb-7fe7-4abe-9ea7-86f54ea15d91
title: Функция IWICStream_InitializeFromIStream_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICStream_InitializeFromIStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8d80a60d2a142b3c69c03b7352c81bcd0f5fc3ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265865"
---
# <a name="iwicstream_initializefromistream_proxy-function"></a><span data-ttu-id="9d1b5-103">Ивикстреам \_ инитиализефромистреам \_ -функция</span><span class="sxs-lookup"><span data-stu-id="9d1b5-103">IWICStream\_InitializeFromIStream\_Proxy function</span></span>

<span data-ttu-id="9d1b5-104">Функция-посредник для метода [**инитиализефромистреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) .</span><span class="sxs-lookup"><span data-stu-id="9d1b5-104">Proxy function for the [**InitializeFromIStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicstream-initializefromistream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d1b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d1b5-105">Syntax</span></span>


```C++
HRESULT IWICStream_InitializeFromIStream_Proxy(
  _In_ IWICStream *THIS_PTR,
  _In_ IStream    *pIStream
);
```



## <a name="parameters"></a><span data-ttu-id="9d1b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d1b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d1b5-107">*Этот \_* \[ Вход в\]</span><span class="sxs-lookup"><span data-stu-id="9d1b5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d1b5-108">Тип: \**[**ивикстреам**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) \** _</span><span class="sxs-lookup"><span data-stu-id="9d1b5-108">Type: \**[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\** _</span></span>

<span data-ttu-id="9d1b5-109">Указатель на этот объект [_ *ивикстреам* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) .</span><span class="sxs-lookup"><span data-stu-id="9d1b5-109">Pointer to this [_ *IWICStream*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream) object.</span></span>

</dd> <dt>

<span data-ttu-id="9d1b5-110">*пистреам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d1b5-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d1b5-111">Тип: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="9d1b5-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="9d1b5-112">Поток инициализации.</span><span class="sxs-lookup"><span data-stu-id="9d1b5-112">The initialize stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d1b5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d1b5-113">Return value</span></span>

<span data-ttu-id="9d1b5-114">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="9d1b5-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="9d1b5-115">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9d1b5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d1b5-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9d1b5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d1b5-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="9d1b5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9d1b5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9d1b5-118">Requirements</span></span>



| <span data-ttu-id="9d1b5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9d1b5-119">Requirement</span></span> | <span data-ttu-id="9d1b5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9d1b5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d1b5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d1b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d1b5-122">Windows XP с пакетом обновления 2 (SP2), \[ только классические приложения Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d1b5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9d1b5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d1b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d1b5-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d1b5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9d1b5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9d1b5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d1b5-126"><dt>Windowscodecs.dll; </dt> <dt>Винкодек. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d1b5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

