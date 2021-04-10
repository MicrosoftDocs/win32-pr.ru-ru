---
description: Функция noframes возвращает маркер в заданный кадр в пределах записи.
ms.assetid: d40bc364-0028-4006-a6c2-6ee100366ba3
title: Функция noframes (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f79e7fa6fc4e79f4dea804769cc9d51b8096860
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143789"
---
# <a name="getframe-function"></a><span data-ttu-id="6618e-103">Функция NOFRAMES</span><span class="sxs-lookup"><span data-stu-id="6618e-103">GetFrame function</span></span>

<span data-ttu-id="6618e-104">Функция **noframes** возвращает маркер в заданный кадр в пределах записи.</span><span class="sxs-lookup"><span data-stu-id="6618e-104">The **GetFrame** function returns a handle to a given frame within a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6618e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6618e-105">Syntax</span></span>


```C++
HFRAME WINAPI GetFrame(
  _In_ HCAPTURE hCapture,
  _In_ DWORD    FrameNumber
);
```



## <a name="parameters"></a><span data-ttu-id="6618e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6618e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6618e-107">*хкаптуре* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6618e-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6618e-108">Обработчик для записи.</span><span class="sxs-lookup"><span data-stu-id="6618e-108">Handle to a capture.</span></span> <span data-ttu-id="6618e-109">Чтобы получить маркер записи, вызовите функцию [жетфрамекаптурехандле](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="6618e-109">To obtain the capture handle, call the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="6618e-110">*Фраменумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6618e-110">*FrameNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6618e-111">Число (от нуля) кадра.</span><span class="sxs-lookup"><span data-stu-id="6618e-111">Number (zero-based) of the frame.</span></span> <span data-ttu-id="6618e-112">Номер первого кадра в записи равен нулю.</span><span class="sxs-lookup"><span data-stu-id="6618e-112">The number of the first frame in a capture is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6618e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6618e-113">Return value</span></span>

<span data-ttu-id="6618e-114">Если функция выполнена успешно, возвращаемое значение является обработкой кадра.</span><span class="sxs-lookup"><span data-stu-id="6618e-114">If the function is successful, the return value is a handle to the frame.</span></span>

<span data-ttu-id="6618e-115">Если функция завершилась неудачно (т. е. Если *хкаптуре* является недопустимым или номер кадра выходит за пределы диапазона), возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="6618e-115">If the function is unsuccessful (that is, if *hCapture* is invalid, or the frame number is out of range), the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6618e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6618e-116">Remarks</span></span>

<span data-ttu-id="6618e-117">Используйте функцию **noframes** для получения маркера кадра, необходимого при размещении экземпляров свойства.</span><span class="sxs-lookup"><span data-stu-id="6618e-117">Use the **GetFrame** function to obtain the frame handle needed when locating instances of a property.</span></span> <span data-ttu-id="6618e-118">Функции, используемые для размещения экземпляров свойств, — это [финдпропертинстанце](findpropertyinstance.md) , которые находят первый экземпляр, и [финдпропертинстанцерестарт](findpropertyinstancerestart.md) , который находит следующий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="6618e-118">The functions used to locate property instances are [FindPropertyInstance](findpropertyinstance.md) which locates the first instance, and [FindPropertyInstanceRestart](findpropertyinstancerestart.md) which locates the next instance.</span></span>

<span data-ttu-id="6618e-119">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **noframes** .</span><span class="sxs-lookup"><span data-stu-id="6618e-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrame** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6618e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6618e-120">Requirements</span></span>



| <span data-ttu-id="6618e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6618e-121">Requirement</span></span> | <span data-ttu-id="6618e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6618e-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6618e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6618e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6618e-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6618e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6618e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6618e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6618e-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6618e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6618e-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6618e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6618e-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6618e-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="6618e-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6618e-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6618e-130"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6618e-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="6618e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6618e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6618e-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6618e-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6618e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6618e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6618e-134">финдпропертинстанце</span><span class="sxs-lookup"><span data-stu-id="6618e-134">FindPropertyInstance</span></span>](findpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="6618e-135">финдпропертинстанцерестарт</span><span class="sxs-lookup"><span data-stu-id="6618e-135">FindPropertyInstanceRestart</span></span>](findpropertyinstancerestart.md)
</dt> </dl>

 

 




