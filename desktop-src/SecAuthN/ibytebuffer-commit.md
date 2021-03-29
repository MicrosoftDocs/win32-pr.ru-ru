---
description: Метод Commit гарантирует, что все изменения, внесенные в объект, Открытый в режиме транзакций, будут отражены в родительском хранилище.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'Метод Ибитебуффер:: Commit (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647545"
---
# <a name="ibytebuffercommit-method"></a><span data-ttu-id="d93b0-103">Метод Ибитебуффер:: Commit</span><span class="sxs-lookup"><span data-stu-id="d93b0-103">IByteBuffer::Commit method</span></span>

<span data-ttu-id="d93b0-104">\[Метод **commit** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="d93b0-104">\[The **Commit** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d93b0-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d93b0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d93b0-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="d93b0-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="d93b0-107">Метод **commit** гарантирует, что все изменения, внесенные в объект, Открытый в режиме транзакций, будут отражены в родительском хранилище.</span><span class="sxs-lookup"><span data-stu-id="d93b0-107">The **Commit** method ensures that any changes made to an object open in transacted mode are reflected in the parent storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93b0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d93b0-108">Syntax</span></span>


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d93b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d93b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d93b0-110">*грфкоммитфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d93b0-110">*grfCommitFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d93b0-111">Необходимо проследить за фиксацией изменений объекта-потока.</span><span class="sxs-lookup"><span data-stu-id="d93b0-111">Controls how the changes for the stream object are committed.</span></span> <span data-ttu-id="d93b0-112">Определение этих значений см. в описании перечисления СТГК.</span><span class="sxs-lookup"><span data-stu-id="d93b0-112">For a definition of these values, see the STGC enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d93b0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d93b0-113">Return value</span></span>

<span data-ttu-id="d93b0-114">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d93b0-114">The return value is an **HRESULT**.</span></span> <span data-ttu-id="d93b0-115">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="d93b0-115">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d93b0-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d93b0-116">Remarks</span></span>

<span data-ttu-id="d93b0-117">Этот метод гарантирует, что изменения в объекте потока, открытом в режиме транзакций, отражаются в родительском хранилище.</span><span class="sxs-lookup"><span data-stu-id="d93b0-117">This method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage.</span></span> <span data-ttu-id="d93b0-118">Изменения, внесенные в поток с момента его открытия или последней фиксации, отражаются в родительском объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="d93b0-118">Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object.</span></span> <span data-ttu-id="d93b0-119">Если родительский элемент открыт в режиме транзакций, родительский элемент по-прежнему может вернуться в более позднее время отката изменений в этом объекте потока.</span><span class="sxs-lookup"><span data-stu-id="d93b0-119">If the parent is opened in transacted mode, the parent may still revert at a later time rolling back the changes to this stream object.</span></span> <span data-ttu-id="d93b0-120">Реализация составного файла не поддерживает открытие потоков в режиме транзакций, поэтому этот метод имеет практически небольшой результат, чем очистка буферов памяти.</span><span class="sxs-lookup"><span data-stu-id="d93b0-120">The compound file implementation does not support opening streams in transacted mode, so this method has very little effect other than to flush memory buffers.</span></span>

## <a name="examples"></a><span data-ttu-id="d93b0-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="d93b0-121">Examples</span></span>

<span data-ttu-id="d93b0-122">В следующем примере показаны фиксации изменений в хранилище.</span><span class="sxs-lookup"><span data-stu-id="d93b0-122">The following example shows committing changes to storage.</span></span>


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a><span data-ttu-id="d93b0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d93b0-123">Requirements</span></span>



| <span data-ttu-id="d93b0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d93b0-124">Requirement</span></span> | <span data-ttu-id="d93b0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d93b0-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d93b0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d93b0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d93b0-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d93b0-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d93b0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d93b0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d93b0-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d93b0-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d93b0-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d93b0-130">End of client support</span></span><br/>    | <span data-ttu-id="d93b0-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d93b0-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="d93b0-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d93b0-132">End of server support</span></span><br/>    | <span data-ttu-id="d93b0-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d93b0-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="d93b0-134">Header</span><span class="sxs-lookup"><span data-stu-id="d93b0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d93b0-135"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d93b0-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d93b0-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d93b0-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="d93b0-137"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d93b0-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d93b0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d93b0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d93b0-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d93b0-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d93b0-140">IID</span><span class="sxs-lookup"><span data-stu-id="d93b0-140">IID</span></span><br/>                      | <span data-ttu-id="d93b0-141">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="d93b0-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

