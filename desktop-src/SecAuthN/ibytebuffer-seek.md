---
description: Метод Seek заменяет указатель поиска на новое расположение относительно начала буфера, до конца буфера или на текущий указатель поиска.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'Метод Ибитебуффер:: Seek (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912488"
---
# <a name="ibytebufferseek-method"></a><span data-ttu-id="a8362-103">Метод Ибитебуффер:: Seek</span><span class="sxs-lookup"><span data-stu-id="a8362-103">IByteBuffer::Seek method</span></span>

<span data-ttu-id="a8362-104">\[Метод **Seek** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a8362-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8362-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a8362-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a8362-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a8362-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="a8362-107">Метод **Seek** заменяет указатель поиска на новое расположение относительно начала буфера, до конца буфера или на текущий указатель поиска.</span><span class="sxs-lookup"><span data-stu-id="a8362-107">The **Seek** method changes the seek pointer to a new location relative to the beginning of the buffer, to the end of the buffer, or to the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8362-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8362-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a><span data-ttu-id="a8362-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8362-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8362-110">*длибмове* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8362-110">*dlibMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8362-111">Смещение, добавляемое в расположение, указанное параметром *dwOrigin*.</span><span class="sxs-lookup"><span data-stu-id="a8362-111">Displacement to be added to the location indicated by *dwOrigin*.</span></span> <span data-ttu-id="a8362-112">Если *dwOrigin* является потоком \_ Seek \_ Set, он интерпретируется как значение без знака, а не как подписанное.</span><span class="sxs-lookup"><span data-stu-id="a8362-112">If *dwOrigin* is STREAM\_SEEK\_SET, this is interpreted as an unsigned value rather than signed.</span></span>

</dd> <dt>

<span data-ttu-id="a8362-113">*dwOrigin* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8362-113">*dwOrigin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8362-114">Указывает источник смещения, указанного в *длибмове*.</span><span class="sxs-lookup"><span data-stu-id="a8362-114">Specifies the origin for the displacement specified in *dlibMove*.</span></span> <span data-ttu-id="a8362-115">Источником может быть одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a8362-115">The origin can be one of the values in the following table.</span></span>



| <span data-ttu-id="a8362-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a8362-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="a8362-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a8362-117">Meaning</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <span data-ttu-id="a8362-118"><dt>**\_набор Seek для потока \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a8362-118"><dt>**STREAM\_SEEK\_SET**</dt></span></span> </dl> | <span data-ttu-id="a8362-119">Новый указатель поиска — это смещение относительно начала потока.</span><span class="sxs-lookup"><span data-stu-id="a8362-119">The new seek pointer is an offset relative to the beginning of the stream.</span></span> <span data-ttu-id="a8362-120">В этом случае параметр *длибмове* является новой позицией поиска относительно начала потока.</span><span class="sxs-lookup"><span data-stu-id="a8362-120">In this case, the *dlibMove* parameter is the new seek position relative to the beginning of the stream.</span></span><br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <span data-ttu-id="a8362-121"><dt>**ПОТОКовый \_ Поиск \_ вал.**</dt></span><span class="sxs-lookup"><span data-stu-id="a8362-121"><dt>**STREAM\_SEEK\_CUR**</dt></span></span> </dl> | <span data-ttu-id="a8362-122">Новый указатель поиска — это смещение относительно текущего расположения указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="a8362-122">The new seek pointer is an offset relative to the current seek pointer location.</span></span> <span data-ttu-id="a8362-123">В этом случае параметр *длибмове* является смещением со знаком из текущей позицией поиска.</span><span class="sxs-lookup"><span data-stu-id="a8362-123">In this case, the *dlibMove* parameter is the signed displacement from the current seek position.</span></span><br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <span data-ttu-id="a8362-124"><dt>**\_Окончание поиска в потоке \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a8362-124"><dt>**STREAM\_SEEK\_END**</dt></span></span> </dl> | <span data-ttu-id="a8362-125">Новый указатель поиска — это смещение относительно конца потока.</span><span class="sxs-lookup"><span data-stu-id="a8362-125">The new seek pointer is an offset relative to the end of the stream.</span></span> <span data-ttu-id="a8362-126">В этом случае параметр *длибмове* является новой позицией поиска относительно конца потока.</span><span class="sxs-lookup"><span data-stu-id="a8362-126">In this case, the *dlibMove* parameter is the new seek position relative to the end of the stream.</span></span><br/>             |



 

</dd> <dt>

<span data-ttu-id="a8362-127">*плибневпоситион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a8362-127">*plibNewPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8362-128">Указатель на расположение, в котором этот метод записывает значение нового указателя поиска с начала потока.</span><span class="sxs-lookup"><span data-stu-id="a8362-128">Pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream.</span></span> <span data-ttu-id="a8362-129">Можно задать для этого указателя значение **null** , чтобы указать, что вы не заинтересованы в этом значении.</span><span class="sxs-lookup"><span data-stu-id="a8362-129">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="a8362-130">В этом случае этот метод не предоставляет новый указатель поиска.</span><span class="sxs-lookup"><span data-stu-id="a8362-130">In this case, this method does not provide the new seek pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8362-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8362-131">Return value</span></span>

<span data-ttu-id="a8362-132">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a8362-132">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a8362-133">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="a8362-133">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8362-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8362-134">Remarks</span></span>

<span data-ttu-id="a8362-135">Метод **Seek** изменяет указатель поиска таким образом, чтобы последующие операции чтения и записи могли выполняться в другом месте в объекте потока.</span><span class="sxs-lookup"><span data-stu-id="a8362-135">The **Seek** method changes the seek pointer so subsequent read and write operations can take place at a different location in the stream object.</span></span> <span data-ttu-id="a8362-136">Поиск перед началом потока является ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a8362-136">It is an error to seek before the beginning of the stream.</span></span> <span data-ttu-id="a8362-137">Однако это не ошибка поиска после конца потока.</span><span class="sxs-lookup"><span data-stu-id="a8362-137">It is not, however, an error to seek past the end of the stream.</span></span> <span data-ttu-id="a8362-138">Поиск после конца потока полезен для последующих операций записи, так как поток в это время будет расширен до позиции поиска непосредственно перед выполнением операции записи.</span><span class="sxs-lookup"><span data-stu-id="a8362-138">Seeking past the end of the stream is useful for subsequent write operations, as the stream will at that time be extended to the seek position immediately before the write operation is done.</span></span>

<span data-ttu-id="a8362-139">Этот метод также можно использовать для получения текущего значения указателя поиска путем вызова этого метода с параметром *dwOrigin* , для которого задано значение Stream \_ Seek \_ cur, а для параметра *длибмове* — значение 0, чтобы указатель поиска не изменялся.</span><span class="sxs-lookup"><span data-stu-id="a8362-139">You can also use this method to obtain the current value of the seek pointer by calling this method with the *dwOrigin* parameter set to STREAM\_SEEK\_CUR and the *dlibMove* parameter set to zero so the seek pointer is not changed.</span></span> <span data-ttu-id="a8362-140">Текущий указатель поиска возвращается в параметре *плибневпоситион* .</span><span class="sxs-lookup"><span data-stu-id="a8362-140">The current seek pointer is returned in the *plibNewPosition* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="a8362-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8362-141">Examples</span></span>

<span data-ttu-id="a8362-142">В следующем примере показано размещение указателя поиска на новом месте.</span><span class="sxs-lookup"><span data-stu-id="a8362-142">The following example shows positioning the seek pointer to a new location.</span></span>


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a><span data-ttu-id="a8362-143">Требования</span><span class="sxs-lookup"><span data-stu-id="a8362-143">Requirements</span></span>



| <span data-ttu-id="a8362-144">Требование</span><span class="sxs-lookup"><span data-stu-id="a8362-144">Requirement</span></span> | <span data-ttu-id="a8362-145">Значение</span><span class="sxs-lookup"><span data-stu-id="a8362-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8362-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8362-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a8362-147">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8362-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a8362-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8362-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a8362-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8362-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a8362-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a8362-150">End of client support</span></span><br/>    | <span data-ttu-id="a8362-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8362-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a8362-152">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a8362-152">End of server support</span></span><br/>    | <span data-ttu-id="a8362-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8362-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a8362-154">Header</span><span class="sxs-lookup"><span data-stu-id="a8362-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8362-155"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8362-155"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8362-156">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a8362-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8362-157"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8362-157"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8362-158">DLL</span><span class="sxs-lookup"><span data-stu-id="a8362-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8362-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8362-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8362-160">IID</span><span class="sxs-lookup"><span data-stu-id="a8362-160">IID</span></span><br/>                      | <span data-ttu-id="a8362-161">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="a8362-161">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

