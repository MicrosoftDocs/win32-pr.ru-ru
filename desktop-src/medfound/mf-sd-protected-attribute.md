---
description: Указывает, содержит ли поток защищенное содержимое.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Атрибут MF_SD_PROTECTED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712909"
---
# <a name="mf_sd_protected-attribute"></a><span data-ttu-id="30b38-103">\_Атрибут MF SD \_ protected</span><span class="sxs-lookup"><span data-stu-id="30b38-103">MF\_SD\_PROTECTED attribute</span></span>

<span data-ttu-id="30b38-104">Указывает, содержит ли поток защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="30b38-104">Indicates whether a stream contains protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="30b38-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="30b38-105">Data type</span></span>

<span data-ttu-id="30b38-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="30b38-106">**UINT32**</span></span>

<span data-ttu-id="30b38-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="30b38-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b38-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30b38-108">Remarks</span></span>

<span data-ttu-id="30b38-109">Этот атрибут применяется к дескрипторам потоков.</span><span class="sxs-lookup"><span data-stu-id="30b38-109">This attribute applies to stream descriptors.</span></span> <span data-ttu-id="30b38-110">Если значение атрибута равно **true**, поток содержит защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="30b38-110">If the value of the attribute is **TRUE**, the stream contains protected content.</span></span> <span data-ttu-id="30b38-111">Если значение равно **false** или атрибут не задан, поток содержит неясное содержимое.</span><span class="sxs-lookup"><span data-stu-id="30b38-111">If the value is **FALSE**, or the attribute is not set, the stream contains clear content.</span></span>

<span data-ttu-id="30b38-112">Вместо того чтобы проверять каждый поток для этого атрибута, можно передать дескриптор представления в функцию [**мфрекуирепротектеденвиронмент**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) .</span><span class="sxs-lookup"><span data-stu-id="30b38-112">Instead of checking each stream for this attribute, you can pass a presentation descriptor to the [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) function.</span></span> <span data-ttu-id="30b38-113">Эта функция проверяет, содержит ли дескриптор презентации защищенные потоки.</span><span class="sxs-lookup"><span data-stu-id="30b38-113">This function tests whether the presentation descriptor contains any protected streams.</span></span>

<span data-ttu-id="30b38-114">Источник мультимедиа должен установить этот атрибут в дескрипторе потока, если для содержимого требуется защищенный путь к носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="30b38-114">A media source should set this attribute on the stream descriptor if the content requires the protected media path (PMP).</span></span>

<span data-ttu-id="30b38-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="30b38-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="30b38-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="30b38-116">Examples</span></span>


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="30b38-117">Требования</span><span class="sxs-lookup"><span data-stu-id="30b38-117">Requirements</span></span>



| <span data-ttu-id="30b38-118">Требование</span><span class="sxs-lookup"><span data-stu-id="30b38-118">Requirement</span></span> | <span data-ttu-id="30b38-119">Значение</span><span class="sxs-lookup"><span data-stu-id="30b38-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="30b38-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30b38-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30b38-121">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="30b38-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="30b38-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30b38-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30b38-123">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="30b38-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="30b38-124">Header</span><span class="sxs-lookup"><span data-stu-id="30b38-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b38-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b38-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b38-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30b38-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b38-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="30b38-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="30b38-128">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="30b38-128">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="30b38-129">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="30b38-129">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="30b38-130">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="30b38-130">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="30b38-131">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="30b38-131">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




