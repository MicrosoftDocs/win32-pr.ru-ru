---
description: Метод stat Получает статистические данные из объекта потока.
ms.assetid: 7dfb59e9-143a-402e-990a-a2b35e6443dd
title: 'Метод Ибитебуффер:: stat (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Stat
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bbbf033fc9ad5a25b3bcf5c22028ac1237f46c14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651100"
---
# <a name="ibytebufferstat-method"></a><span data-ttu-id="fa45b-103">Метод Ибитебуффер:: stat</span><span class="sxs-lookup"><span data-stu-id="fa45b-103">IByteBuffer::Stat method</span></span>

<span data-ttu-id="fa45b-104">\[Метод **stat** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fa45b-104">\[The **Stat** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fa45b-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fa45b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fa45b-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="fa45b-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="fa45b-107">Метод **stat** получает статистические данные из объекта потока.</span><span class="sxs-lookup"><span data-stu-id="fa45b-107">The **Stat** method retrieves statistical information from the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa45b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa45b-108">Syntax</span></span>


```C++
HRESULT Stat(
  [out] LPSTATSTRUCT pstatstg,
  [in]  LONG         grfStatFlag
);
```



## <a name="parameters"></a><span data-ttu-id="fa45b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa45b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa45b-110">*пстатстг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fa45b-110">*pstatstg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa45b-111">Указывает на структуру **статструкт** , в которой этот метод помещает сведения об этом объекте потока.</span><span class="sxs-lookup"><span data-stu-id="fa45b-111">Points to a **STATSTRUCT** structure where this method places information about this stream object.</span></span> <span data-ttu-id="fa45b-112">При возникновении ошибки этот указатель имеет **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="fa45b-112">This pointer is **NULL** if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="fa45b-113">*грфстатфлаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa45b-113">*grfStatFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa45b-114">Указывает, что этот метод не возвращает некоторые поля в структуре **статструкт** , тем самым сохраняя операцию выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="fa45b-114">Specifies that this method does not return some of the fields in the **STATSTRUCT** structure, thus saving a memory allocation operation.</span></span> <span data-ttu-id="fa45b-115">Значения берутся из перечисления [**статфлаг**](/windows/win32/api/wtypes/ne-wtypes-statflag)</span><span class="sxs-lookup"><span data-stu-id="fa45b-115">Values are taken from the [**STATFLAG**](/windows/win32/api/wtypes/ne-wtypes-statflag) enumeration</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa45b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa45b-116">Return value</span></span>

<span data-ttu-id="fa45b-117">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fa45b-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="fa45b-118">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="fa45b-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa45b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa45b-119">Remarks</span></span>

<span data-ttu-id="fa45b-120">Метод **ибитебуффер:: stat** получает указатель на структуру **статструкт** , содержащую сведения об этом открытом потоке.</span><span class="sxs-lookup"><span data-stu-id="fa45b-120">The **IByteBuffer::Stat** method retrieves a pointer to the **STATSTRUCT** structure that contains information about this open stream.</span></span>

## <a name="examples"></a><span data-ttu-id="fa45b-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="fa45b-121">Examples</span></span>

<span data-ttu-id="fa45b-122">В следующем примере показано получение статистических данных из потока.</span><span class="sxs-lookup"><span data-stu-id="fa45b-122">The following example shows retrieving statistical information from the stream.</span></span>


```C++
STATSTRUCT  statstr;
HRESULT     hr;

// Retrieve the statistical information.
hr = pIByteBuff->Stat(&statstr,
                      STATFLAG_DEFAULT);
if (FAILED(hr))
  printf("Failed IByteBuffer::Stat\n");
else
  // Use statstr as needed.
```



## <a name="requirements"></a><span data-ttu-id="fa45b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="fa45b-123">Requirements</span></span>



| <span data-ttu-id="fa45b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="fa45b-124">Requirement</span></span> | <span data-ttu-id="fa45b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="fa45b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa45b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa45b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa45b-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fa45b-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fa45b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa45b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa45b-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fa45b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa45b-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="fa45b-130">End of client support</span></span><br/>    | <span data-ttu-id="fa45b-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fa45b-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fa45b-132">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="fa45b-132">End of server support</span></span><br/>    | <span data-ttu-id="fa45b-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa45b-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fa45b-134">Header</span><span class="sxs-lookup"><span data-stu-id="fa45b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa45b-135"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa45b-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa45b-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fa45b-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="fa45b-137"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fa45b-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fa45b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fa45b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa45b-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa45b-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fa45b-140">IID</span><span class="sxs-lookup"><span data-stu-id="fa45b-140">IID</span></span><br/>                      | <span data-ttu-id="fa45b-141">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="fa45b-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

