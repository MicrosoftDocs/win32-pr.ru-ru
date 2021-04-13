---
description: Позволяет использовать асинхронное преобразование Media Foundation (MFT).
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: Атрибут MF_TRANSFORM_ASYNC_UNLOCK (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543226"
---
# <a name="mf_transform_async_unlock-attribute"></a><span data-ttu-id="73184-103">\_ \_ Атрибут асинхронного \_ разблокировки MF Transform</span><span class="sxs-lookup"><span data-stu-id="73184-103">MF\_TRANSFORM\_ASYNC\_UNLOCK attribute</span></span>

<span data-ttu-id="73184-104">Позволяет использовать асинхронное преобразование Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="73184-104">Enables the use of an asynchronous Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="73184-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="73184-105">Data type</span></span>

<span data-ttu-id="73184-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="73184-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="73184-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="73184-107">Get/set</span></span>

<span data-ttu-id="73184-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="73184-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="73184-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="73184-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="73184-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73184-110">Remarks</span></span>

<span data-ttu-id="73184-111">Асинхронные МФТС несовместимы с более ранними версиями Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="73184-111">Asynchronous MFTs are not compatible with earlier versions of Microsoft Media Foundation.</span></span> <span data-ttu-id="73184-112">Чтобы предотвратить случайное использование асинхронной таблицы MFT существующими приложениями, для этого атрибута необходимо задать ненулевое значение, прежде чем можно будет использовать асинхронную таблицу MFT.</span><span class="sxs-lookup"><span data-stu-id="73184-112">To prevent existing applications from accidentally using an asynchronous MFT, this attribute must be set to a nonzero value before an asynchronous MFT can be used.</span></span> <span data-ttu-id="73184-113">Конвейер Media Foundation автоматически задает атрибут, так что большинству приложений не требуется использовать этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="73184-113">The Media Foundation pipeline automatically sets the attribute, so that most applications do not need to use this attribute.</span></span> <span data-ttu-id="73184-114">Однако если приложение использует асинхронную таблицу MFT вне Media Foundation конвейера, приложение должно установить этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="73184-114">However, if an application uses an asynchronous MFT outside of the Media Foundation pipeline, the application must set this attribute.</span></span>

<span data-ttu-id="73184-115">Синхронный МФТС не требует этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="73184-115">Synchronous MFTs do not require this attribute.</span></span>

<span data-ttu-id="73184-116">Чтобы проверить, является ли MFT асинхронным, получите значение атрибута [MF \_ Transform \_ Async](mf-transform-async.md) в MFT.</span><span class="sxs-lookup"><span data-stu-id="73184-116">To test whether an MFT is asynchronous, get the value of the [MF\_TRANSFORM\_ASYNC](mf-transform-async.md) attribute on the MFT.</span></span>

## <a name="examples"></a><span data-ttu-id="73184-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="73184-117">Examples</span></span>

<span data-ttu-id="73184-118">Следующий код разблокирует асинхронную основную таблицу.</span><span class="sxs-lookup"><span data-stu-id="73184-118">The following code unlocks an asynchronous MFT.</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="73184-119">Требования</span><span class="sxs-lookup"><span data-stu-id="73184-119">Requirements</span></span>



| <span data-ttu-id="73184-120">Требование</span><span class="sxs-lookup"><span data-stu-id="73184-120">Requirement</span></span> | <span data-ttu-id="73184-121">Значение</span><span class="sxs-lookup"><span data-stu-id="73184-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73184-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73184-122">Minimum supported client</span></span><br/> | <span data-ttu-id="73184-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="73184-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="73184-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73184-124">Minimum supported server</span></span><br/> | <span data-ttu-id="73184-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="73184-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="73184-126">Header</span><span class="sxs-lookup"><span data-stu-id="73184-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="73184-127"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="73184-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73184-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73184-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73184-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73184-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="73184-130">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="73184-130">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="73184-131">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="73184-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




