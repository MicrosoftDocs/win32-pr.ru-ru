---
description: Метод Initialize подготавливает объект Ибитебуффер для использования. Этот метод должен быть вызван до вызова любых других методов в интерфейсе Ибитебуффер.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Метод Ибитебуффер:: Initialize (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647621"
---
# <a name="ibytebufferinitialize-method"></a><span data-ttu-id="5672c-104">Метод Ибитебуффер:: Initialize</span><span class="sxs-lookup"><span data-stu-id="5672c-104">IByteBuffer::Initialize method</span></span>

<span data-ttu-id="5672c-105">\[Метод **Initialize** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="5672c-105">\[The **Initialize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5672c-106">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="5672c-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="5672c-107">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="5672c-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="5672c-108">Метод **Initialize** подготавливает объект [**ибитебуффер**](ibytebuffer.md) для использования.</span><span class="sxs-lookup"><span data-stu-id="5672c-108">The **Initialize** method prepares the [**IByteBuffer**](ibytebuffer.md) object for use.</span></span> <span data-ttu-id="5672c-109">Этот метод должен быть вызван до вызова любых других методов в интерфейсе **ибитебуффер** .</span><span class="sxs-lookup"><span data-stu-id="5672c-109">This method must be called prior to calling any other methods in the **IByteBuffer** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5672c-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5672c-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a><span data-ttu-id="5672c-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5672c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5672c-112">*лсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5672c-112">*lSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5672c-113">Начальный размер (в байтах) данных, которые должен содержать поток.</span><span class="sxs-lookup"><span data-stu-id="5672c-113">Initial size, in bytes, of the data the stream is to contain.</span></span>

</dd> <dt>

<span data-ttu-id="5672c-114">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5672c-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5672c-115">Если не **равно NULL**, начальные данные для записи в поток.</span><span class="sxs-lookup"><span data-stu-id="5672c-115">If not **NULL**, the initial data to write to the stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5672c-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5672c-116">Return value</span></span>

<span data-ttu-id="5672c-117">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5672c-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="5672c-118">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="5672c-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5672c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5672c-119">Remarks</span></span>

<span data-ttu-id="5672c-120">При использовании нового потока [**ибитебуффер**](ibytebuffer.md) Вызывайте этот метод перед использованием любого из других методов **ибитебуффер** .</span><span class="sxs-lookup"><span data-stu-id="5672c-120">When using a new [**IByteBuffer**](ibytebuffer.md) stream, call this method prior to using any of the other **IByteBuffer** methods.</span></span>

## <a name="examples"></a><span data-ttu-id="5672c-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="5672c-121">Examples</span></span>

<span data-ttu-id="5672c-122">В следующем примере показана инициализация объекта [**ибитебуффер**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5672c-122">The following example shows initializing the [**IByteBuffer**](ibytebuffer.md) object.</span></span>


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a><span data-ttu-id="5672c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="5672c-123">Requirements</span></span>



| <span data-ttu-id="5672c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="5672c-124">Requirement</span></span> | <span data-ttu-id="5672c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="5672c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5672c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5672c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5672c-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5672c-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5672c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5672c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5672c-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5672c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5672c-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="5672c-130">End of client support</span></span><br/>    | <span data-ttu-id="5672c-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="5672c-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="5672c-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="5672c-132">End of server support</span></span><br/>    | <span data-ttu-id="5672c-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5672c-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="5672c-134">Header</span><span class="sxs-lookup"><span data-stu-id="5672c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5672c-135"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="5672c-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5672c-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5672c-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="5672c-137"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5672c-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5672c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5672c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5672c-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5672c-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5672c-140">IID</span><span class="sxs-lookup"><span data-stu-id="5672c-140">IID</span></span><br/>                      | <span data-ttu-id="5672c-141">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="5672c-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

