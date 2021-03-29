---
description: Задает значение по умолчанию для исходного бита в аудиопотока MPEG-1. Это свойство применяется к кодировщикам аудио в формате MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Свойство Авенкмпаоригиналбитстреам (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894898"
---
# <a name="avencmpaoriginalbitstream-property"></a><span data-ttu-id="4123d-104">Авенкмпаоригиналбитстреам, свойство</span><span class="sxs-lookup"><span data-stu-id="4123d-104">AVEncMPAOriginalBitstream property</span></span>

<span data-ttu-id="4123d-105">Задает значение по умолчанию для исходного бита в аудиопотока MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="4123d-105">Specifies the default setting for the original bit in the MPEG-1 audio stream.</span></span> <span data-ttu-id="4123d-106">Это свойство применяется к кодировщикам аудио в формате MPEG.</span><span class="sxs-lookup"><span data-stu-id="4123d-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="4123d-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4123d-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="4123d-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4123d-108">Data type</span></span>

<span data-ttu-id="4123d-109">**Вариант \_ BOOL** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="4123d-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="4123d-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="4123d-110">Property GUID</span></span>

<span data-ttu-id="4123d-111">**КОДЕКАПИ \_ авенкмпаоригиналбитстреам**</span><span class="sxs-lookup"><span data-stu-id="4123d-111">**CODECAPI\_AVEncMPAOriginalBitstream**</span></span>

## <a name="property-value"></a><span data-ttu-id="4123d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4123d-112">Property value</span></span>

<span data-ttu-id="4123d-113">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="4123d-113">This property can have the following values.</span></span>



| <span data-ttu-id="4123d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4123d-114">Value</span></span>          | <span data-ttu-id="4123d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="4123d-115">Description</span></span>          |
|----------------|----------------------|
| <span data-ttu-id="4123d-116">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="4123d-116">VARIANT\_FALSE</span></span> | <span data-ttu-id="4123d-117">Исходный бит отключен.</span><span class="sxs-lookup"><span data-stu-id="4123d-117">Original bit is off.</span></span> |
| <span data-ttu-id="4123d-118">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="4123d-118">VARIANT\_TRUE</span></span>  | <span data-ttu-id="4123d-119">Исходный бит включен.</span><span class="sxs-lookup"><span data-stu-id="4123d-119">Original bit is on.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="4123d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4123d-120">Remarks</span></span>

<span data-ttu-id="4123d-121">Кодировщик может переопределить этот параметр на основе содержимого входного потока.</span><span class="sxs-lookup"><span data-stu-id="4123d-121">The encoder might override this setting, based on the contents of the input stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="4123d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4123d-122">Requirements</span></span>



| <span data-ttu-id="4123d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4123d-123">Requirement</span></span> | <span data-ttu-id="4123d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4123d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4123d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4123d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4123d-126">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4123d-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="4123d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4123d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4123d-128">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="4123d-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4123d-129">Header</span><span class="sxs-lookup"><span data-stu-id="4123d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4123d-130"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="4123d-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4123d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4123d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4123d-132">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="4123d-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="4123d-133">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="4123d-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




