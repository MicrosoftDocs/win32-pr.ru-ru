---
description: Метод CopyTo копирует указанное число байтов из текущего указателя поиска в объекте в текущий указатель поиска в другом объекте.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Метод Ибитебуффер:: CopyTo (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272043"
---
# <a name="ibytebuffercopyto-method"></a><span data-ttu-id="cde9d-103">Метод Ибитебуффер:: CopyTo</span><span class="sxs-lookup"><span data-stu-id="cde9d-103">IByteBuffer::CopyTo method</span></span>

<span data-ttu-id="cde9d-104">\[Метод **CopyTo** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cde9d-104">\[The **CopyTo** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cde9d-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="cde9d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cde9d-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="cde9d-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="cde9d-107">Метод **CopyTo** Копирует указанное число байтов из текущего указателя поиска в объекте в текущий указатель поиска в другом объекте.</span><span class="sxs-lookup"><span data-stu-id="cde9d-107">The **CopyTo** method copies a specified number of bytes from the current seek pointer in the object to the current seek pointer in another object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde9d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cde9d-108">Syntax</span></span>


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="cde9d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cde9d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde9d-110">*пбитебуффер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cde9d-110">*pByteBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde9d-111">Указывает на целевой поток.</span><span class="sxs-lookup"><span data-stu-id="cde9d-111">Points to the destination stream.</span></span> <span data-ttu-id="cde9d-112">Поток, на который указывает *пбитебуффер* , может быть новым потоком или клоном исходного потока.</span><span class="sxs-lookup"><span data-stu-id="cde9d-112">The stream pointed to by *pByteBuffer* can be a new stream or a clone of the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="cde9d-113">*CB* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cde9d-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cde9d-114">Число байтов, которое необходимо скопировать из исходного потока.</span><span class="sxs-lookup"><span data-stu-id="cde9d-114">Number of bytes to copy from the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="cde9d-115">*пкбреад* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cde9d-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cde9d-116">Указатель на расположение, в котором этот метод записывает фактическое число байтов, считанных из источника.</span><span class="sxs-lookup"><span data-stu-id="cde9d-116">Pointer to the location where this method writes the actual number of bytes read from the source.</span></span> <span data-ttu-id="cde9d-117">Можно задать для этого указателя значение **null** , чтобы указать, что вы не заинтересованы в этом значении.</span><span class="sxs-lookup"><span data-stu-id="cde9d-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="cde9d-118">В этом случае этот метод не обеспечивает фактическое число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="cde9d-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="cde9d-119">*пкбвриттен* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cde9d-119">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cde9d-120">Указатель на расположение, в котором этот метод записывает фактическое число байтов, записанных в назначение.</span><span class="sxs-lookup"><span data-stu-id="cde9d-120">Pointer to the location where this method writes the actual number of bytes written to the destination.</span></span> <span data-ttu-id="cde9d-121">Можно задать для этого указателя значение **null** , чтобы указать, что вы не заинтересованы в этом значении.</span><span class="sxs-lookup"><span data-stu-id="cde9d-121">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="cde9d-122">В этом случае этот метод не обеспечивает фактическое число записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="cde9d-122">In this case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde9d-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cde9d-123">Return value</span></span>

<span data-ttu-id="cde9d-124">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cde9d-124">The return value is an **HRESULT**.</span></span> <span data-ttu-id="cde9d-125">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="cde9d-125">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cde9d-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cde9d-126">Remarks</span></span>

<span data-ttu-id="cde9d-127">Этот метод копирует указанные байты из одного потока в другой.</span><span class="sxs-lookup"><span data-stu-id="cde9d-127">This method copies the specified bytes from one stream to another.</span></span> <span data-ttu-id="cde9d-128">Его также можно использовать для копирования потока в себя.</span><span class="sxs-lookup"><span data-stu-id="cde9d-128">It can also be used to copy a stream to itself.</span></span> <span data-ttu-id="cde9d-129">Указатель поиска в каждом экземпляре потока корректируется на количество считанных или записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="cde9d-129">The seek pointer in each stream instance is adjusted for the number of bytes read or written.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde9d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="cde9d-130">Requirements</span></span>



| <span data-ttu-id="cde9d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="cde9d-131">Requirement</span></span> | <span data-ttu-id="cde9d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cde9d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cde9d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cde9d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cde9d-134">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cde9d-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cde9d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cde9d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cde9d-136">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cde9d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cde9d-137">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cde9d-137">End of client support</span></span><br/>    | <span data-ttu-id="cde9d-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cde9d-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cde9d-139">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cde9d-139">End of server support</span></span><br/>    | <span data-ttu-id="cde9d-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cde9d-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cde9d-141">Header</span><span class="sxs-lookup"><span data-stu-id="cde9d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cde9d-142"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde9d-142"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cde9d-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cde9d-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="cde9d-144"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cde9d-144"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cde9d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cde9d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde9d-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde9d-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cde9d-147">IID</span><span class="sxs-lookup"><span data-stu-id="cde9d-147">IID</span></span><br/>                      | <span data-ttu-id="cde9d-148">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="cde9d-148">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

