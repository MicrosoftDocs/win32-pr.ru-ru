---
description: Переупорядочивает указанный дочерний объект Иконтекстноде по указанному индексу.
ms.assetid: 1cee73af-8d5b-4d5d-bc67-a3ac6f4b2462
title: 'Метод Иконтекстноде:: Мовесубнодетопоситион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.MoveSubNodeToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 398a56cf2c30c93a72e061dfe968de24276888f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692435"
---
# <a name="icontextnodemovesubnodetoposition-method"></a><span data-ttu-id="799e2-103">Метод Иконтекстноде:: Мовесубнодетопоситион</span><span class="sxs-lookup"><span data-stu-id="799e2-103">IContextNode::MoveSubNodeToPosition method</span></span>

<span data-ttu-id="799e2-104">Переупорядочивает указанный дочерний объект [**иконтекстноде**](icontextnode.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="799e2-104">Reorders a specified child [**IContextNode**](icontextnode.md) object to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="799e2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="799e2-105">Syntax</span></span>


```C++
HRESULT MoveSubNodeToPosition(
  [in] IContextNode *pSubnodeToMove,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="799e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="799e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="799e2-107">*псубнодетомове* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="799e2-107">*pSubnodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="799e2-108">Перемещаемый объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="799e2-108">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="799e2-109">*улневиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="799e2-109">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="799e2-110">Индекс для новой позиции подузла.</span><span class="sxs-lookup"><span data-stu-id="799e2-110">The index for the new position of the subnode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="799e2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="799e2-111">Return value</span></span>

<span data-ttu-id="799e2-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="799e2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="799e2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="799e2-113">Remarks</span></span>

<span data-ttu-id="799e2-114">Возвращает **E \_ INVALIDARG** , если *псубнодетомове* не является дочерним узлом этого [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="799e2-114">Returns **E\_INVALIDARG** if *pSubnodeToMove* is not a child node of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="799e2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="799e2-115">Requirements</span></span>



| <span data-ttu-id="799e2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="799e2-116">Requirement</span></span> | <span data-ttu-id="799e2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="799e2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="799e2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="799e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="799e2-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="799e2-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="799e2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="799e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="799e2-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="799e2-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="799e2-122">Header</span><span class="sxs-lookup"><span data-stu-id="799e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="799e2-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="799e2-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="799e2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="799e2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="799e2-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="799e2-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="799e2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="799e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799e2-127">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="799e2-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="799e2-128">**Иконтекстноде:: Креатесубноде**</span><span class="sxs-lookup"><span data-stu-id="799e2-128">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="799e2-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="799e2-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




