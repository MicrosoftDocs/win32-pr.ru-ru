---
description: Указывает значение, которое принимает свойство в определенный момент времени.
ms.assetid: 117868b7-65e5-4b3b-9e50-4106ee6a65d0
title: Структура DEXTER_PARAM (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_PARAM
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 22b0f6ef0a91f9a6d9163a03c17f6e86ee8b5f4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651996"
---
# <a name="dexter_param-structure"></a><span data-ttu-id="5596b-103">\_Структура param Декстер</span><span class="sxs-lookup"><span data-stu-id="5596b-103">DEXTER\_PARAM structure</span></span>

> [!Note]  
> <span data-ttu-id="5596b-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="5596b-104">\[Deprecated.</span></span> <span data-ttu-id="5596b-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5596b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5596b-106">Указывает значение, которое принимает свойство в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="5596b-106">Specifies the value that a property assumes at a given time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5596b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5596b-107">Syntax</span></span>


```C++
typedef struct {
  BSTR   Name;
  DISPID dispID;
  LONG   nValues;
} DEXTER_PARAM;
```



## <a name="members"></a><span data-ttu-id="5596b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5596b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5596b-109">**Name**</span><span class="sxs-lookup"><span data-stu-id="5596b-109">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="5596b-110">Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="5596b-110">Name of the property.</span></span>

</dd> <dt>

<span data-ttu-id="5596b-111">**dispID**</span><span class="sxs-lookup"><span data-stu-id="5596b-111">**dispID**</span></span>
</dt> <dd>

<span data-ttu-id="5596b-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5596b-112">Reserved.</span></span> <span data-ttu-id="5596b-113">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="5596b-113">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5596b-114">**Значения**</span><span class="sxs-lookup"><span data-stu-id="5596b-114">**nValues**</span></span>
</dt> <dd>

<span data-ttu-id="5596b-115">Количество значений, которые предполагает свойство.</span><span class="sxs-lookup"><span data-stu-id="5596b-115">Number of values that the property assumes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5596b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5596b-116">Remarks</span></span>

<span data-ttu-id="5596b-117">Объект должен поддерживать интерфейс **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="5596b-117">The object must support the **IDispatch** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5596b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5596b-118">Requirements</span></span>



| <span data-ttu-id="5596b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5596b-119">Requirement</span></span> | <span data-ttu-id="5596b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5596b-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5596b-121">Header</span><span class="sxs-lookup"><span data-stu-id="5596b-121">Header</span></span><br/> | <dl> <span data-ttu-id="5596b-122"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="5596b-122"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5596b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5596b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5596b-124">**ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="5596b-124">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="5596b-125">**\_значение Декстер**</span><span class="sxs-lookup"><span data-stu-id="5596b-125">**DEXTER\_VALUE**</span></span>](dexter-value.md)
</dt> </dl>

 

 




