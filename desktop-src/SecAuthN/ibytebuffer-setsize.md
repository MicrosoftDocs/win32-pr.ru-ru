---
description: Метод SetSize изменяет размер объекта потока.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'Метод Ибитебуффер:: SetSize (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999304"
---
# <a name="ibytebuffersetsize-method"></a><span data-ttu-id="01d1a-103">Метод Ибитебуффер:: SetSize</span><span class="sxs-lookup"><span data-stu-id="01d1a-103">IByteBuffer::SetSize method</span></span>

<span data-ttu-id="01d1a-104">\[Метод **SetSize** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="01d1a-104">\[The **SetSize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="01d1a-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="01d1a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="01d1a-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="01d1a-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="01d1a-107">Метод **SetSize** изменяет размер объекта потока.</span><span class="sxs-lookup"><span data-stu-id="01d1a-107">The **SetSize** method changes the size of the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d1a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01d1a-108">Syntax</span></span>


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a><span data-ttu-id="01d1a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="01d1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d1a-110">*либневсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01d1a-110">*libNewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d1a-111">Новый размер потока в виде числа байтов</span><span class="sxs-lookup"><span data-stu-id="01d1a-111">New size of the stream as a number of bytes</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d1a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01d1a-112">Return value</span></span>

<span data-ttu-id="01d1a-113">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="01d1a-113">The return value is an **HRESULT**.</span></span> <span data-ttu-id="01d1a-114">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="01d1a-114">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="01d1a-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01d1a-115">Remarks</span></span>

<span data-ttu-id="01d1a-116">Метод **ибитебуффер:: SetSize** изменяет размер объекта потока.</span><span class="sxs-lookup"><span data-stu-id="01d1a-116">The **IByteBuffer::SetSize** method changes the size of the stream object.</span></span> <span data-ttu-id="01d1a-117">Вызовите этот метод, чтобы предварительно выделить место для потока.</span><span class="sxs-lookup"><span data-stu-id="01d1a-117">Call this method to preallocate space for the stream.</span></span> <span data-ttu-id="01d1a-118">Если значение параметра *либневсизе* больше, чем текущий размер потока, поток расширяется до указанного размера путем заполнения промежуточного пространства байтами неопределенного значения.</span><span class="sxs-lookup"><span data-stu-id="01d1a-118">If the *libNewSize* parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value.</span></span> <span data-ttu-id="01d1a-119">Эта операция аналогична методу [**ибитебуффер:: Write**](ibytebuffer-write.md) , если указатель поиска находится за текущим концом потока.</span><span class="sxs-lookup"><span data-stu-id="01d1a-119">This operation is similar to the [**IByteBuffer::Write**](ibytebuffer-write.md) method if the seek pointer is past the current end-of-stream.</span></span>

<span data-ttu-id="01d1a-120">Если параметр *либневсизе* меньше текущего потока, то поток усекается до указанного размера.</span><span class="sxs-lookup"><span data-stu-id="01d1a-120">If the *libNewSize* parameter is smaller than the current stream, then the stream is truncated to the indicated size.</span></span>

<span data-ttu-id="01d1a-121">Изменение размера потока не влияет на указатель поиска.</span><span class="sxs-lookup"><span data-stu-id="01d1a-121">The seek pointer is not affected by the change in stream size.</span></span>

<span data-ttu-id="01d1a-122">Вызов **ибитебуффер:: SetSize** может быть эффективным способом получения большого фрагмента непрерывного пространства.</span><span class="sxs-lookup"><span data-stu-id="01d1a-122">Calling **IByteBuffer::SetSize** can be an effective way of trying to obtain a large chunk of contiguous space.</span></span>

## <a name="examples"></a><span data-ttu-id="01d1a-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="01d1a-123">Examples</span></span>

<span data-ttu-id="01d1a-124">В следующем примере показано задание размера буфера.</span><span class="sxs-lookup"><span data-stu-id="01d1a-124">The following example shows setting the buffer size.</span></span>


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a><span data-ttu-id="01d1a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="01d1a-125">Requirements</span></span>



| <span data-ttu-id="01d1a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="01d1a-126">Requirement</span></span> | <span data-ttu-id="01d1a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="01d1a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01d1a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01d1a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="01d1a-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01d1a-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="01d1a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01d1a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="01d1a-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01d1a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="01d1a-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="01d1a-132">End of client support</span></span><br/>    | <span data-ttu-id="01d1a-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="01d1a-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="01d1a-134">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="01d1a-134">End of server support</span></span><br/>    | <span data-ttu-id="01d1a-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01d1a-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="01d1a-136">Header</span><span class="sxs-lookup"><span data-stu-id="01d1a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="01d1a-137"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="01d1a-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01d1a-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="01d1a-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="01d1a-139"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01d1a-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01d1a-140">DLL</span><span class="sxs-lookup"><span data-stu-id="01d1a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01d1a-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01d1a-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="01d1a-142">IID</span><span class="sxs-lookup"><span data-stu-id="01d1a-142">IID</span></span><br/>                      | <span data-ttu-id="01d1a-143">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="01d1a-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

