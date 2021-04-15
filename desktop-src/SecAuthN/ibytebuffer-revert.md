---
description: 'Метод revert отменяет все изменения, внесенные в поток транзакций с момента последнего вызова Ибитебуффер:: Commit.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Метод Ибитебуффер:: revert (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263009"
---
# <a name="ibytebufferrevert-method"></a><span data-ttu-id="7d238-103">Метод Ибитебуффер:: revert</span><span class="sxs-lookup"><span data-stu-id="7d238-103">IByteBuffer::Revert method</span></span>

<span data-ttu-id="7d238-104">\[Метод **revert** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7d238-104">\[The **Revert** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d238-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7d238-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7d238-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="7d238-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="7d238-107">Метод **revert** отменяет все изменения, внесенные в поток транзакций с момента последнего вызова [**Ибитебуффер:: Commit**](ibytebuffer-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="7d238-107">The **Revert** method discards all changes that have been made to a transacted stream since the last [**IByteBuffer::Commit**](ibytebuffer-commit.md) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d238-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d238-108">Syntax</span></span>


```C++
HRESULT Revert();
```



## <a name="parameters"></a><span data-ttu-id="7d238-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d238-109">Parameters</span></span>

<span data-ttu-id="7d238-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7d238-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d238-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d238-111">Return value</span></span>

<span data-ttu-id="7d238-112">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7d238-112">The return value is an **HRESULT**.</span></span> <span data-ttu-id="7d238-113">Значение S \_ ОК указывает, что вызов был успешным, и поток был восстановлен до предыдущей версии.</span><span class="sxs-lookup"><span data-stu-id="7d238-113">A value of S\_OK indicates the call was successful and the stream was reverted to its previous version.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d238-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d238-114">Remarks</span></span>

<span data-ttu-id="7d238-115">Этот метод отклоняет изменения, внесенные в поток транзакций с момента последней операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="7d238-115">This method discards changes made to a transacted stream since the last commit operation.</span></span>

## <a name="examples"></a><span data-ttu-id="7d238-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="7d238-116">Examples</span></span>

<span data-ttu-id="7d238-117">В следующем примере показан возврат транзакционного потока к последней операции фиксации.</span><span class="sxs-lookup"><span data-stu-id="7d238-117">The following example shows reverting a transacted stream to the last-committed operation.</span></span>


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a><span data-ttu-id="7d238-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7d238-118">Requirements</span></span>



| <span data-ttu-id="7d238-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7d238-119">Requirement</span></span> | <span data-ttu-id="7d238-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7d238-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d238-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d238-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d238-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7d238-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7d238-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d238-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d238-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d238-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d238-125">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7d238-125">End of client support</span></span><br/>    | <span data-ttu-id="7d238-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d238-126">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7d238-127">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7d238-127">End of server support</span></span><br/>    | <span data-ttu-id="7d238-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d238-128">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7d238-129">Header</span><span class="sxs-lookup"><span data-stu-id="7d238-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d238-130"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d238-130"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d238-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7d238-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d238-132"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7d238-132"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7d238-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7d238-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d238-134"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d238-134"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d238-135">IID</span><span class="sxs-lookup"><span data-stu-id="7d238-135">IID</span></span><br/>                      | <span data-ttu-id="7d238-136">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="7d238-136">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

