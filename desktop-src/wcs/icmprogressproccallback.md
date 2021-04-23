---
title: Функция обратного вызова ICMProgressProcCallback
description: Функция Икмпрогресспроккаллбакк является предоставляемой приложением функцией обратного вызова, которая сообщает о ходе выполнения и позволяет приложению отменить обработку цвета.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Цветовая система Windows для функции обратного вызова Икмпрогресспроккаллбакк
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721007"
---
# <a name="icmprogressproccallback-callback-function"></a><span data-ttu-id="d9e2a-104">Функция обратного вызова ICMProgressProcCallback</span><span class="sxs-lookup"><span data-stu-id="d9e2a-104">ICMProgressProcCallback callback function</span></span>

<span data-ttu-id="d9e2a-105">Функция **икмпрогресспроккаллбакк** является предоставляемой приложением функцией обратного вызова, которая сообщает о ходе выполнения и позволяет приложению отменить обработку цвета.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-105">The **ICMProgressProcCallback** function is an application-supplied callback function that reports progress and permits the application to cancel color processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e2a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9e2a-106">Syntax</span></span>


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="d9e2a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9e2a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e2a-108">*улмакс*</span><span class="sxs-lookup"><span data-stu-id="d9e2a-108">*ulMax*</span></span> 
</dt> <dd>

<span data-ttu-id="d9e2a-109">Задает максимальное значение счетчика хода выполнения (используется для оценки завершения обработки растрового изображения).</span><span class="sxs-lookup"><span data-stu-id="d9e2a-109">Specifies the maximum value of the progress counter (used to estimate completion of the bitmap processing).</span></span>

</dd> <dt>

<span data-ttu-id="d9e2a-110">*улкуррент*</span><span class="sxs-lookup"><span data-stu-id="d9e2a-110">*ulCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="d9e2a-111">Задает текущее значение счетчика хода выполнения (при делении на максимальное значение) представляет собой приблизительную оценку процента завершения.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-111">Specifies the current value of the progress counter (when divided by the maximum value, provides a rough estimate of percentage of completion).</span></span>

</dd> <dt>

<span data-ttu-id="d9e2a-112">*улкаллбаккдата*</span><span class="sxs-lookup"><span data-stu-id="d9e2a-112">*ulCallbackData*</span></span> 
</dt> <dd>

<span data-ttu-id="d9e2a-113">Указывает данные, передаваемые приложением функции ICM2, которая затем передает ее функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-113">Specifies the data which is passed by the application to an ICM2 function, which then passes it on to the callback function.</span></span> <span data-ttu-id="d9e2a-114">Такие данные можно использовать, например, для указания битовой карты и процесса, о ходе которого сообщается.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-114">Such data can be used, for example, to identify the bitmap and process about which progress is being reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9e2a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9e2a-115">Return value</span></span>

<span data-ttu-id="d9e2a-116">Эта функция возвращает **значение true** , чтобы продолжить обработку растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-116">This function returns **TRUE** to continue bitmap processing.</span></span> <span data-ttu-id="d9e2a-117">Для отмены обработки возвращается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="d9e2a-117">The return value is **FALSE** to cancel processing.</span></span> <span data-ttu-id="d9e2a-118">Если обработка отменена, то вызывающая функция возвращает ноль для обозначения сбоя, хотя выходной буфер может быть заполнен частично.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-118">If processing is canceled, the calling function returns zero to indicate failure, although its output buffer may be partially filled.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9e2a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9e2a-119">Remarks</span></span>

<span data-ttu-id="d9e2a-120">Имя этой функции обратного вызова предоставляется приложением.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-120">The name of this callback function is supplied by the application.</span></span> <span data-ttu-id="d9e2a-121">Ряд функций WCS, включая [**транслатебитмапбитс**](/windows/win32/api/icm/nf-icm-translatebitmapbits) и [**чеккбитмапбитс**](/windows/win32/api/icm/nf-icm-checkbitmapbits), периодически Вызывайте эту функцию.</span><span class="sxs-lookup"><span data-stu-id="d9e2a-121">A number of WCS functions, including [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) and [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), call this function periodically.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e2a-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d9e2a-122">Requirements</span></span>



| <span data-ttu-id="d9e2a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d9e2a-123">Requirement</span></span> | <span data-ttu-id="d9e2a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d9e2a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d9e2a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9e2a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9e2a-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9e2a-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d9e2a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9e2a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9e2a-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9e2a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d9e2a-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9e2a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9e2a-130"><dt>ICM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9e2a-130"><dt>Icm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9e2a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9e2a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e2a-132">Основные понятия управления цветом</span><span class="sxs-lookup"><span data-stu-id="d9e2a-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="d9e2a-133">Функции</span><span class="sxs-lookup"><span data-stu-id="d9e2a-133">Functions</span></span>](functions.md)
</dt> <dt>

[<span data-ttu-id="d9e2a-134">**транслатебитмапбитс**</span><span class="sxs-lookup"><span data-stu-id="d9e2a-134">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[<span data-ttu-id="d9e2a-135">**чеккбитмапбитс**</span><span class="sxs-lookup"><span data-stu-id="d9e2a-135">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
