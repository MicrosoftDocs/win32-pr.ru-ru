---
description: Метод Write записывает указанное число из байтов в объект потока, начиная с текущего указателя поиска.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'Метод Ибитебуффер:: Write (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912487"
---
# <a name="ibytebufferwrite-method"></a><span data-ttu-id="dfb3a-103">Метод Ибитебуффер:: Write</span><span class="sxs-lookup"><span data-stu-id="dfb3a-103">IByteBuffer::Write method</span></span>

<span data-ttu-id="dfb3a-104">\[Метод **Write** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dfb3a-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dfb3a-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="dfb3a-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="dfb3a-107">Метод **Write** записывает указанное число из байтов в объект потока, начиная с текущего указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-107">The **Write** method writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb3a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfb3a-108">Syntax</span></span>


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="dfb3a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dfb3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb3a-110">*пбите* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfb3a-110">*pByte* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb3a-111">Адрес буфера, содержащего данные, которые должны быть записаны в поток.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-111">Address of the buffer containing the data that is to be written to the stream.</span></span> <span data-ttu-id="dfb3a-112">Для этого параметра должен быть указан допустимый указатель, даже если значение *CB* равно нулю.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-112">A valid pointer must be provided for this parameter even when *cb* is zero.</span></span>

</dd> <dt>

<span data-ttu-id="dfb3a-113">*CB* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dfb3a-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb3a-114">Число байтов данных, которые необходимо попытаться записать в поток.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-114">Number of bytes of data to attempt to write into the stream.</span></span> <span data-ttu-id="dfb3a-115">Этот параметр может быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-115">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dfb3a-116">*пкбвриттен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dfb3a-116">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb3a-117">Адрес **длинной** переменной, в которой этот метод записывает фактическое число байтов, записанных в объект потока.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-117">Address of a **LONG** variable where this method writes the actual number of bytes written to the stream object.</span></span> <span data-ttu-id="dfb3a-118">Вызывающий объект может установить для этого указателя **значение NULL**. в этом случае этот метод не предоставляет фактическое число записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-118">The caller can set this pointer to **NULL**, in which case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb3a-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dfb3a-119">Return value</span></span>

<span data-ttu-id="dfb3a-120">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="dfb3a-121">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfb3a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfb3a-122">Remarks</span></span>

<span data-ttu-id="dfb3a-123">Метод **ибитебуффер:: Write** записывает указанные данные в объект потока.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-123">The **IByteBuffer::Write** method writes the specified data to a stream object.</span></span> <span data-ttu-id="dfb3a-124">Указатель поиска корректируется на фактическое число записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-124">The seek pointer is adjusted for the number of bytes actually written.</span></span> <span data-ttu-id="dfb3a-125">Число фактически записанных байтов возвращается в параметре *пкбвриттен* .</span><span class="sxs-lookup"><span data-stu-id="dfb3a-125">The number of bytes actually written is returned in the *pcbWritten* parameter.</span></span> <span data-ttu-id="dfb3a-126">Если число байтов равно нулю, операция записи не действует.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-126">If the byte count is zero bytes, the write operation has no effect.</span></span>

<span data-ttu-id="dfb3a-127">Если указатель поиска в текущий момент находится за концом потока, а число байтов не равно нулю, этот метод увеличивает размер потока до указателя поиска и записывает указанные байты, начиная с указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-127">If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer.</span></span> <span data-ttu-id="dfb3a-128">Заполнение байтов, записанное в поток, не инициализируется каким бы то ни было определенным значением.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-128">The fill bytes written to the stream are not initialized to any particular value.</span></span> <span data-ttu-id="dfb3a-129">Это совпадает с поведением конца файла в файловой системе MS-DOS FAT.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-129">This is the same as the end-of-file behavior in the MS-DOS FAT file system.</span></span>

<span data-ttu-id="dfb3a-130">При наличии нулевого числа байтов и указателя поиска за концом потока этот метод не создает байты заполнения для увеличения потока до указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-130">With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer.</span></span> <span data-ttu-id="dfb3a-131">В этом случае необходимо вызвать метод [**ибитебуффер:: SetSize**](ibytebuffer-setsize.md) , чтобы увеличить размер потока и записать байты заполнения.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-131">In this case, you must call the [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) method to increase the size of the stream and write the fill bytes.</span></span>

<span data-ttu-id="dfb3a-132">Параметр *пкбвриттен* может иметь значение, даже если возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-132">The *pcbWritten* parameter can have a value even if an error occurs.</span></span>

<span data-ttu-id="dfb3a-133">В реализации, предоставляемой моделью COM, объекты потока не имеют разреженных объектов.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-133">In the COM-provided implementation, stream objects are not sparse.</span></span> <span data-ttu-id="dfb3a-134">Все байты заполнения в конечном итоге выделяются на диске и назначаются потоку.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-134">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

## <a name="examples"></a><span data-ttu-id="dfb3a-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="dfb3a-135">Examples</span></span>

<span data-ttu-id="dfb3a-136">В следующем примере показана запись байтов в объект потока.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-136">The following example shows writing bytes into the stream object.</span></span>


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a><span data-ttu-id="dfb3a-137">Требования</span><span class="sxs-lookup"><span data-stu-id="dfb3a-137">Requirements</span></span>



| <span data-ttu-id="dfb3a-138">Требование</span><span class="sxs-lookup"><span data-stu-id="dfb3a-138">Requirement</span></span> | <span data-ttu-id="dfb3a-139">Значение</span><span class="sxs-lookup"><span data-stu-id="dfb3a-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb3a-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfb3a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb3a-141">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dfb3a-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dfb3a-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfb3a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb3a-143">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dfb3a-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfb3a-144">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dfb3a-144">End of client support</span></span><br/>    | <span data-ttu-id="dfb3a-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dfb3a-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dfb3a-146">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="dfb3a-146">End of server support</span></span><br/>    | <span data-ttu-id="dfb3a-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dfb3a-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dfb3a-148">Header</span><span class="sxs-lookup"><span data-stu-id="dfb3a-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb3a-149"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb3a-149"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfb3a-150">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dfb3a-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="dfb3a-151"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dfb3a-151"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dfb3a-152">DLL</span><span class="sxs-lookup"><span data-stu-id="dfb3a-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb3a-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfb3a-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dfb3a-154">IID</span><span class="sxs-lookup"><span data-stu-id="dfb3a-154">IID</span></span><br/>                      | <span data-ttu-id="dfb3a-155">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="dfb3a-155">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

