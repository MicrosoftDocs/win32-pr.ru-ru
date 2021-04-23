---
description: Возвращает число объектов Иконтекстлинк в данной коллекции.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'Метод Иконтекстлинкс:: NOCOUNT (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263150"
---
# <a name="icontextlinksgetcount-method"></a><span data-ttu-id="87bc4-103">Метод Иконтекстлинкс:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="87bc4-103">IContextLinks::GetCount method</span></span>

<span data-ttu-id="87bc4-104">Возвращает число объектов [**иконтекстлинк**](icontextlink.md) в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="87bc4-104">Gets the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="87bc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87bc4-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="87bc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87bc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87bc4-107">*пулкаунт* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="87bc4-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="87bc4-108">Число объектов [**иконтекстлинк**](icontextlink.md) , содержащихся в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="87bc4-108">The number of [**IContextLink**](icontextlink.md) objects that are contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87bc4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87bc4-109">Return value</span></span>

<span data-ttu-id="87bc4-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="87bc4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87bc4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="87bc4-111">Requirements</span></span>



| <span data-ttu-id="87bc4-112">Требование</span><span class="sxs-lookup"><span data-stu-id="87bc4-112">Requirement</span></span> | <span data-ttu-id="87bc4-113">Значение</span><span class="sxs-lookup"><span data-stu-id="87bc4-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87bc4-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87bc4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="87bc4-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="87bc4-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="87bc4-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87bc4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="87bc4-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="87bc4-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="87bc4-118">Header</span><span class="sxs-lookup"><span data-stu-id="87bc4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="87bc4-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="87bc4-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="87bc4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="87bc4-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87bc4-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87bc4-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="87bc4-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87bc4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87bc4-123">**иконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="87bc4-123">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="87bc4-124">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="87bc4-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




