---
description: Метод Read считывает указанное число байтов из объекта buffer в память, начиная с текущего указателя поиска.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'Метод Ибитебуффер:: Read (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272038"
---
# <a name="ibytebufferread-method"></a><span data-ttu-id="4b560-103">Метод Ибитебуффер:: Read</span><span class="sxs-lookup"><span data-stu-id="4b560-103">IByteBuffer::Read method</span></span>

<span data-ttu-id="4b560-104">\[Метод **Read** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4b560-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4b560-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4b560-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b560-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="4b560-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4b560-107">Метод **Read** считывает указанное число байтов из объекта buffer в память, начиная с текущего указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="4b560-107">The **Read** method reads a specified number of bytes from the buffer object into memory starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b560-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b560-108">Syntax</span></span>


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="4b560-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b560-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b560-110">*пбите* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4b560-110">*pByte* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b560-111">Указывает на буфер, в который считываются потоковые данные.</span><span class="sxs-lookup"><span data-stu-id="4b560-111">Points to the buffer into which the stream data is read.</span></span> <span data-ttu-id="4b560-112">Если возникает ошибка, это значение равно **null**.</span><span class="sxs-lookup"><span data-stu-id="4b560-112">If an error occurs, this value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4b560-113">*CB* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b560-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b560-114">Число байтов данных, которые необходимо попытаться считать из объекта потока.</span><span class="sxs-lookup"><span data-stu-id="4b560-114">Number of bytes of data to attempt to read from the stream object.</span></span>

</dd> <dt>

<span data-ttu-id="4b560-115">*пкбреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4b560-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b560-116">Адрес **длинной** переменной, которая получает фактическое число байтов, считанных из объекта потока.</span><span class="sxs-lookup"><span data-stu-id="4b560-116">Address of a **LONG** variable that receives the actual number of bytes read from the stream object.</span></span> <span data-ttu-id="4b560-117">Можно задать для этого указателя значение **null** , чтобы указать, что вы не заинтересованы в этом значении.</span><span class="sxs-lookup"><span data-stu-id="4b560-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="4b560-118">В этом случае этот метод не обеспечивает фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="4b560-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b560-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b560-119">Return value</span></span>

<span data-ttu-id="4b560-120">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4b560-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4b560-121">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="4b560-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b560-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b560-122">Remarks</span></span>

<span data-ttu-id="4b560-123">Этот метод считывает байты из этого объекта потока в память.</span><span class="sxs-lookup"><span data-stu-id="4b560-123">This method reads bytes from this stream object into memory.</span></span> <span data-ttu-id="4b560-124">Объект потока должен быть открыт в \_ режиме чтения стгм.</span><span class="sxs-lookup"><span data-stu-id="4b560-124">The stream object must be opened in STGM\_READ mode.</span></span> <span data-ttu-id="4b560-125">Этот метод корректирует указатель поиска на фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="4b560-125">This method adjusts the seek pointer by the actual number of bytes read.</span></span>

<span data-ttu-id="4b560-126">Число фактически считанных байтов также возвращается в параметре *пкбреад* .</span><span class="sxs-lookup"><span data-stu-id="4b560-126">The number of bytes actually read is also returned in the *pcbRead* parameter.</span></span>

<span data-ttu-id="4b560-127">Примечания для тех, кто вызывает этот метод</span><span class="sxs-lookup"><span data-stu-id="4b560-127">Notes to Callers</span></span>

<span data-ttu-id="4b560-128">Фактическое число считанных байтов может быть меньше, чем число запрошенных байтов, если возникла ошибка или достигнут конец потока во время операции чтения.</span><span class="sxs-lookup"><span data-stu-id="4b560-128">The actual number of bytes read can be fewer than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.</span></span>

<span data-ttu-id="4b560-129">Некоторые реализации могут возвращать ошибку, если в процессе чтения достигнут конец потока.</span><span class="sxs-lookup"><span data-stu-id="4b560-129">Some implementations might return an error if the end of the stream is reached during the read.</span></span> <span data-ttu-id="4b560-130">Необходимо подготовиться к работе с возвращаемыми ошибками или \_ возвратами ОК при завершении операций чтения потока.</span><span class="sxs-lookup"><span data-stu-id="4b560-130">You must be prepared to deal with the error return or S\_OK return values on end of stream reads.</span></span>

## <a name="examples"></a><span data-ttu-id="4b560-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="4b560-131">Examples</span></span>

<span data-ttu-id="4b560-132">В следующем примере показано чтение байтов из буфера.</span><span class="sxs-lookup"><span data-stu-id="4b560-132">The following example shows reading bytes from the buffer.</span></span>


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="4b560-133">Требования</span><span class="sxs-lookup"><span data-stu-id="4b560-133">Requirements</span></span>



| <span data-ttu-id="4b560-134">Требование</span><span class="sxs-lookup"><span data-stu-id="4b560-134">Requirement</span></span> | <span data-ttu-id="4b560-135">Значение</span><span class="sxs-lookup"><span data-stu-id="4b560-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b560-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b560-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4b560-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b560-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4b560-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b560-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4b560-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b560-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b560-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4b560-140">End of client support</span></span><br/>    | <span data-ttu-id="4b560-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4b560-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4b560-142">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4b560-142">End of server support</span></span><br/>    | <span data-ttu-id="4b560-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4b560-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4b560-144">Header</span><span class="sxs-lookup"><span data-stu-id="4b560-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b560-145"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b560-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b560-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4b560-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="4b560-147"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4b560-147"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4b560-148">DLL</span><span class="sxs-lookup"><span data-stu-id="4b560-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b560-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b560-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4b560-150">IID</span><span class="sxs-lookup"><span data-stu-id="4b560-150">IID</span></span><br/>                      | <span data-ttu-id="4b560-151">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="4b560-151">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

