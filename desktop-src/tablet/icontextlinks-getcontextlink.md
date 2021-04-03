---
description: Извлекает Иконтекстлинк по указанному индексу.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'Метод Иконтекстлинкс:: Жетконтекстлинк (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145541"
---
# <a name="icontextlinksgetcontextlink-method"></a><span data-ttu-id="02757-103">Метод Иконтекстлинкс:: Жетконтекстлинк</span><span class="sxs-lookup"><span data-stu-id="02757-103">IContextLinks::GetContextLink method</span></span>

<span data-ttu-id="02757-104">Извлекает [**иконтекстлинк**](icontextlink.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="02757-104">Retrieves the [**IContextLink**](icontextlink.md) at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="02757-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02757-105">Syntax</span></span>


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a><span data-ttu-id="02757-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02757-107">*улиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02757-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02757-108">Отсчитываемый от нуля индекс объекта [**иконтекстлинк**](icontextlink.md) , который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="02757-108">The zero-based index of the [**IContextLink**](icontextlink.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="02757-109">*ппконтекстлинк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="02757-109">*ppContextLink* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02757-110">Указатель на объект [**иконтекстлинк**](icontextlink.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="02757-110">A pointer to the [**IContextLink**](icontextlink.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02757-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02757-111">Return value</span></span>

<span data-ttu-id="02757-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="02757-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02757-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02757-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="02757-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстлинк* , когда больше не нужно использовать контекстную ссылку.</span><span class="sxs-lookup"><span data-stu-id="02757-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextLink* when you no longer need to use the context link.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02757-115">Требования</span><span class="sxs-lookup"><span data-stu-id="02757-115">Requirements</span></span>



| <span data-ttu-id="02757-116">Требование</span><span class="sxs-lookup"><span data-stu-id="02757-116">Requirement</span></span> | <span data-ttu-id="02757-117">Значение</span><span class="sxs-lookup"><span data-stu-id="02757-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02757-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02757-118">Minimum supported client</span></span><br/> | <span data-ttu-id="02757-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="02757-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="02757-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02757-120">Minimum supported server</span></span><br/> | <span data-ttu-id="02757-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="02757-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="02757-122">Header</span><span class="sxs-lookup"><span data-stu-id="02757-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="02757-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="02757-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="02757-124">DLL</span><span class="sxs-lookup"><span data-stu-id="02757-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02757-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02757-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="02757-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02757-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02757-127">**иконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="02757-127">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="02757-128">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="02757-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="02757-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="02757-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

