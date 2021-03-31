---
description: Извлекает тип отношения, представляемого этим Иконтекстлинк.
ms.assetid: 03c13eba-1493-4fb7-b684-f15147e5a0eb
title: 'Метод Иконтекстлинк:: Жетконтекстлинкдиректион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLink.GetContextLinkDirection
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 47ad3e6c8d28126c010e5cc1c1419b99d9cde4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263152"
---
# <a name="icontextlinkgetcontextlinkdirection-method"></a><span data-ttu-id="7494f-103">Метод Иконтекстлинк:: Жетконтекстлинкдиректион</span><span class="sxs-lookup"><span data-stu-id="7494f-103">IContextLink::GetContextLinkDirection method</span></span>

<span data-ttu-id="7494f-104">Извлекает тип отношения, представляемого этим [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="7494f-104">Retrieves the type of relationship this [**IContextLink**](icontextlink.md) represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="7494f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7494f-105">Syntax</span></span>


```C++
HRESULT GetContextLinkDirection(
  [out] ContextLinkDirection *pContextLinkDirection
);
```



## <a name="parameters"></a><span data-ttu-id="7494f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7494f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7494f-107">*пконтекстлинкдиректион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7494f-107">*pContextLinkDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7494f-108">Направление, которое представляет этот [**иконтекстлинк**](icontextlink.md) .</span><span class="sxs-lookup"><span data-stu-id="7494f-108">The direction this [**IContextLink**](icontextlink.md) represents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7494f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7494f-109">Return value</span></span>

<span data-ttu-id="7494f-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7494f-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7494f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="7494f-111">Requirements</span></span>



| <span data-ttu-id="7494f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="7494f-112">Requirement</span></span> | <span data-ttu-id="7494f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7494f-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7494f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7494f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7494f-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7494f-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7494f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7494f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7494f-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7494f-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7494f-118">Header</span><span class="sxs-lookup"><span data-stu-id="7494f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7494f-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7494f-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7494f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7494f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7494f-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7494f-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7494f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7494f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7494f-123">**иконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="7494f-123">**IContextLink**</span></span>](icontextlink.md)
</dt> <dt>

[<span data-ttu-id="7494f-124">**контекстлинкдиректион**</span><span class="sxs-lookup"><span data-stu-id="7494f-124">**ContextLinkDirection**</span></span>](contextlinkdirection.md)
</dt> <dt>

[<span data-ttu-id="7494f-125">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="7494f-125">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




