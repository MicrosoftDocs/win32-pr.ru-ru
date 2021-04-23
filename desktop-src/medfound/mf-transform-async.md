---
description: Указывает, выполняет ли преобразование Media Foundation (MFT) асинхронную обработку.
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: Атрибут MF_TRANSFORM_ASYNC (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811014"
---
# <a name="mf_transform_async-attribute"></a><span data-ttu-id="786d3-103">\_ \_ Асинхронный атрибут преобразования MF</span><span class="sxs-lookup"><span data-stu-id="786d3-103">MF\_TRANSFORM\_ASYNC attribute</span></span>

<span data-ttu-id="786d3-104">Указывает, выполняет ли преобразование Media Foundation (MFT) асинхронную обработку.</span><span class="sxs-lookup"><span data-stu-id="786d3-104">Specifies whether a Media Foundation transform (MFT) performs asynchronous processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="786d3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="786d3-105">Data type</span></span>

<span data-ttu-id="786d3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="786d3-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="786d3-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="786d3-107">Get/set</span></span>

<span data-ttu-id="786d3-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="786d3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="786d3-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="786d3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="786d3-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="786d3-110">Remarks</span></span>

<span data-ttu-id="786d3-111">Атрибут является логическим значением:</span><span class="sxs-lookup"><span data-stu-id="786d3-111">The attribute is a Boolean value:</span></span>

-   <span data-ttu-id="786d3-112">Если атрибут не равен нулю, то MFT выполняет асинхронную обработку.</span><span class="sxs-lookup"><span data-stu-id="786d3-112">If the attribute is nonzero, the MFT performs asynchronous processing.</span></span>
-   <span data-ttu-id="786d3-113">Если атрибут равен 0 или не задан, MFT является синхронным.</span><span class="sxs-lookup"><span data-stu-id="786d3-113">If the attribute is 0 or not set, the MFT is synchronous.</span></span>

<span data-ttu-id="786d3-114">Чтобы получить этот атрибут, сначала вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить хранилище атрибутов MFT.</span><span class="sxs-lookup"><span data-stu-id="786d3-114">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT's attribute store.</span></span> <span data-ttu-id="786d3-115">Если этот метод завершился с ошибкой, вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="786d3-115">If that method succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span> <span data-ttu-id="786d3-116">Если один из двух методов завершается неудачей, MFT является синхронным.</span><span class="sxs-lookup"><span data-stu-id="786d3-116">If either of the two methods fails, the MFT is synchronous.</span></span>

<span data-ttu-id="786d3-117">Для асинхронного МФТС этому атрибуту должно быть присвоено ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="786d3-117">For asynchronous MFTs, this attribute must be set to a nonzero value.</span></span> <span data-ttu-id="786d3-118">Для синхронного МФТС этот атрибут является необязательным, но при его наличии его необходимо задать равным 0.</span><span class="sxs-lookup"><span data-stu-id="786d3-118">For synchronous MFTs, this attribute is optional, but must be set to 0 if present.</span></span>

<span data-ttu-id="786d3-119">Асинхронные МФТС несовместимы с более ранними версиями Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="786d3-119">Asynchronous MFTs are not compatible with earlier versions of Media Foundation.</span></span> <span data-ttu-id="786d3-120">Чтобы использовать асинхронную таблицу MFT, клиент должен задать атрибут [**MF \_ Transform \_ Async \_ reunlock**](mf-transform-async-unlock.md) в MFT.</span><span class="sxs-lookup"><span data-stu-id="786d3-120">To use an asynchronous MFT, the client must set the [**MF\_TRANSFORM\_ASYNC\_UNLOCK**](mf-transform-async-unlock.md) attribute on the MFT.</span></span> <span data-ttu-id="786d3-121">(Microsoft Media Foundation конвейер выполняет этот шаг автоматически.)</span><span class="sxs-lookup"><span data-stu-id="786d3-121">(The Microsoft Media Foundation pipeline performs this step automatically.)</span></span>

## <a name="examples"></a><span data-ttu-id="786d3-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="786d3-122">Examples</span></span>

<span data-ttu-id="786d3-123">Следующий код проверяет, выполняет ли MFT асинхронную обработку.</span><span class="sxs-lookup"><span data-stu-id="786d3-123">The following code tests whether an MFT performs asynchronous processing.</span></span>


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="786d3-124">Требования</span><span class="sxs-lookup"><span data-stu-id="786d3-124">Requirements</span></span>



| <span data-ttu-id="786d3-125">Требование</span><span class="sxs-lookup"><span data-stu-id="786d3-125">Requirement</span></span> | <span data-ttu-id="786d3-126">Значение</span><span class="sxs-lookup"><span data-stu-id="786d3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="786d3-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="786d3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="786d3-128">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="786d3-128">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="786d3-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="786d3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="786d3-130">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="786d3-130">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="786d3-131">Header</span><span class="sxs-lookup"><span data-stu-id="786d3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="786d3-132"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="786d3-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="786d3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="786d3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786d3-134">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="786d3-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="786d3-135">Асинхронный МФТС</span><span class="sxs-lookup"><span data-stu-id="786d3-135">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="786d3-136">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="786d3-136">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="786d3-137">**\_ \_ асинхронное \_ деблокирование преобразования MF**</span><span class="sxs-lookup"><span data-stu-id="786d3-137">**MF\_TRANSFORM\_ASYNC\_UNLOCK**</span></span>](mf-transform-async-unlock.md)
</dt> </dl>

 

 




