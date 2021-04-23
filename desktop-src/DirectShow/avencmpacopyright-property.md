---
description: Задает значение по умолчанию для бита авторского права в аудиопотока MPEG-1. Это свойство применяется к кодировщикам аудио в формате MPEG.
ms.assetid: 6029c96f-b1dd-402f-9bac-9021bd897ee4
title: Свойство Авенкмпакопиригхт (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4449c41448d59ce673e667be7400d4a713236dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423026"
---
# <a name="avencmpacopyright-property"></a><span data-ttu-id="bb4aa-104">Авенкмпакопиригхт, свойство</span><span class="sxs-lookup"><span data-stu-id="bb4aa-104">AVEncMPACopyright property</span></span>

<span data-ttu-id="bb4aa-105">Задает значение по умолчанию для бита авторского права в аудиопотока MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-105">Specifies the default setting for the copyright bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="bb4aa-106">Это свойство применяется к кодировщикам аудио в формате MPEG.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="bb4aa-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb4aa-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bb4aa-108">Data type</span></span>

<span data-ttu-id="bb4aa-109">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="bb4aa-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="bb4aa-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="bb4aa-110">Property GUID</span></span>

<span data-ttu-id="bb4aa-111">**КОДЕКАПИ \_ авенкмпакопиригхт**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-111">**CODECAPI\_AVEncMPACopyright**</span></span>

## <a name="property-value"></a><span data-ttu-id="bb4aa-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bb4aa-112">Property value</span></span>

<span data-ttu-id="bb4aa-113">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-113">This property can have the following values.</span></span>



| <span data-ttu-id="bb4aa-114">Значение</span><span class="sxs-lookup"><span data-stu-id="bb4aa-114">Value</span></span>          | <span data-ttu-id="bb4aa-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bb4aa-115">Description</span></span>           |
|----------------|-----------------------|
| <span data-ttu-id="bb4aa-116">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="bb4aa-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="bb4aa-117">Бит авторских прав отключен.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-117">Copyright bit is off.</span></span> |
| <span data-ttu-id="bb4aa-118">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="bb4aa-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="bb4aa-119">Бит авторского права включен.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-119">Copyright bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="bb4aa-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb4aa-120">Remarks</span></span>

<span data-ttu-id="bb4aa-121">Кодировщик может переопределить этот параметр на основе содержимого входного потока.</span><span class="sxs-lookup"><span data-stu-id="bb4aa-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb4aa-122">Требования</span><span class="sxs-lookup"><span data-stu-id="bb4aa-122">Requirements</span></span>



| <span data-ttu-id="bb4aa-123">Требование</span><span class="sxs-lookup"><span data-stu-id="bb4aa-123">Requirement</span></span> | <span data-ttu-id="bb4aa-124">Значение</span><span class="sxs-lookup"><span data-stu-id="bb4aa-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4aa-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb4aa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bb4aa-126">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bb4aa-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bb4aa-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb4aa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bb4aa-128">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="bb4aa-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bb4aa-129">Header</span><span class="sxs-lookup"><span data-stu-id="bb4aa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb4aa-130"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb4aa-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb4aa-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb4aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb4aa-132">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="bb4aa-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="bb4aa-133">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="bb4aa-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




