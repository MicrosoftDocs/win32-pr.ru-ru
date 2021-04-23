---
description: Метод Clone создает новый объект со своим собственным указателем поиска, который ссылается на те же байты, что и исходный объект Ибитебуффер.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'Метод Ибитебуффер:: Clone (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265813"
---
# <a name="ibytebufferclone-method"></a><span data-ttu-id="e79f6-103">Метод Ибитебуффер:: Clone</span><span class="sxs-lookup"><span data-stu-id="e79f6-103">IByteBuffer::Clone method</span></span>

<span data-ttu-id="e79f6-104">\[Метод **clone** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e79f6-104">\[The **Clone** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e79f6-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e79f6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e79f6-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="e79f6-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="e79f6-107">Метод **clone** создает новый объект со своим собственным указателем поиска, который ссылается на те же байты, что и исходный объект [**ибитебуффер**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e79f6-107">The **Clone** method creates a new object with its own seek pointer that references the same bytes as the original [**IByteBuffer**](ibytebuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e79f6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e79f6-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="e79f6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e79f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e79f6-110">*ппбитебуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e79f6-110">*ppByteBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e79f6-111">При успешном выполнении указывает на расположение указателя [**ибитебуффер**](ibytebuffer.md) на новый объект потока.</span><span class="sxs-lookup"><span data-stu-id="e79f6-111">When successful, points to the location of an [**IByteBuffer**](ibytebuffer.md) pointer to the new stream object.</span></span> <span data-ttu-id="e79f6-112">Завершив использование указателя **ибитебуффер** , выпустите его, вызвав функцию [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="e79f6-112">When you have finished using the **IByteBuffer** pointer, release it by calling the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) function.</span></span> <span data-ttu-id="e79f6-113">Если возникает ошибка, этот параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e79f6-113">If an error occurs, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e79f6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e79f6-114">Return value</span></span>

<span data-ttu-id="e79f6-115">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e79f6-115">The return value is an **HRESULT**.</span></span> <span data-ttu-id="e79f6-116">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="e79f6-116">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e79f6-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e79f6-117">Remarks</span></span>

<span data-ttu-id="e79f6-118">Этот метод создает новый объект потока для доступа к тем же байтам, но с помощью отдельного указателя поиска.</span><span class="sxs-lookup"><span data-stu-id="e79f6-118">This method creates a new stream object for accessing the same bytes but using a separate seek pointer.</span></span> <span data-ttu-id="e79f6-119">Новый объект потока видит те же данные, что и исходный объект потока.</span><span class="sxs-lookup"><span data-stu-id="e79f6-119">The new stream object sees the same data as the source stream object.</span></span> <span data-ttu-id="e79f6-120">Изменения, записанные в один объект, сразу же отображаются в другом.</span><span class="sxs-lookup"><span data-stu-id="e79f6-120">Changes written to one object are immediately visible in the other.</span></span> <span data-ttu-id="e79f6-121">Блокировка диапазона является общей для объектов потока.</span><span class="sxs-lookup"><span data-stu-id="e79f6-121">Range locking is shared between the stream objects.</span></span>

<span data-ttu-id="e79f6-122">Начальное значение указателя поиска в экземпляре клонированного потока совпадает с текущим параметром указателя поиска в исходном потоке во время операции клонирования.</span><span class="sxs-lookup"><span data-stu-id="e79f6-122">The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.</span></span>

## <a name="examples"></a><span data-ttu-id="e79f6-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="e79f6-123">Examples</span></span>

<span data-ttu-id="e79f6-124">В следующем примере показана клонирование интерфейса [**ибитебуффер**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e79f6-124">The following example shows cloning the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a><span data-ttu-id="e79f6-125">Требования</span><span class="sxs-lookup"><span data-stu-id="e79f6-125">Requirements</span></span>



| <span data-ttu-id="e79f6-126">Требование</span><span class="sxs-lookup"><span data-stu-id="e79f6-126">Requirement</span></span> | <span data-ttu-id="e79f6-127">Значение</span><span class="sxs-lookup"><span data-stu-id="e79f6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e79f6-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e79f6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e79f6-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e79f6-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e79f6-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e79f6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e79f6-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e79f6-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e79f6-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e79f6-132">End of client support</span></span><br/>    | <span data-ttu-id="e79f6-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e79f6-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="e79f6-134">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e79f6-134">End of server support</span></span><br/>    | <span data-ttu-id="e79f6-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e79f6-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="e79f6-136">Header</span><span class="sxs-lookup"><span data-stu-id="e79f6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e79f6-137"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e79f6-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e79f6-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e79f6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="e79f6-139"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e79f6-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e79f6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e79f6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e79f6-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e79f6-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e79f6-142">IID</span><span class="sxs-lookup"><span data-stu-id="e79f6-142">IID</span></span><br/>                      | <span data-ttu-id="e79f6-143">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="e79f6-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

