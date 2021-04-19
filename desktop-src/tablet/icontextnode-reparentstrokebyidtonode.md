---
description: Перемещает данные штриха из этого Иконтекстнодеа в указанный Иконтекстноде.
ms.assetid: 583f2de9-d32e-4177-83d1-4abbd0f9f960
title: 'Метод Иконтекстноде:: Репарентстрокебидтоноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ReparentStrokeByIdToNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3984153a0551de999563b8775ceb5acba1696e39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692434"
---
# <a name="icontextnodereparentstrokebyidtonode-method"></a><span data-ttu-id="df523-103">Метод Иконтекстноде:: Репарентстрокебидтоноде</span><span class="sxs-lookup"><span data-stu-id="df523-103">IContextNode::ReparentStrokeByIdToNode method</span></span>

<span data-ttu-id="df523-104">Перемещает данные штриха из этого [**иконтекстнодеа**](icontextnode.md) в указанный **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="df523-104">Moves stroke data from this [**IContextNode**](icontextnode.md) to the specified **IContextNode**.</span></span>

## <a name="syntax"></a><span data-ttu-id="df523-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df523-105">Syntax</span></span>


```C++
HRESULT ReparentStrokeByIdToNode(
  [in] LONG         lStrokeId,
  [in] IContextNode *pContextNodeDestination
);
```



## <a name="parameters"></a><span data-ttu-id="df523-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="df523-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df523-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df523-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df523-108">Идентификатор перемещаемого штриха.</span><span class="sxs-lookup"><span data-stu-id="df523-108">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="df523-109">*пконтекстнодедестинатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="df523-109">*pContextNodeDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df523-110">Объект [**иконтекстноде**](icontextnode.md) , в который перемещаются данные штриха.</span><span class="sxs-lookup"><span data-stu-id="df523-110">The [**IContextNode**](icontextnode.md) object to which to move the stroke data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df523-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df523-111">Return value</span></span>

<span data-ttu-id="df523-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="df523-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="df523-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df523-113">Remarks</span></span>

<span data-ttu-id="df523-114">Указанный объект [**иконтекстноде**](icontextnode.md) должен принадлежать к одному из следующих типов из [типов узлов контекста](context-node-types.md) константы: **инкворд**, **инкдравинг**, **инкбуллет** или **унклассифиединк**.</span><span class="sxs-lookup"><span data-stu-id="df523-114">The specified [**IContextNode**](icontextnode.md) object must be one of the following types from the [Context Node Types](context-node-types.md) constants: **InkWord**, **InkDrawing**, **InkBullet**, or **UnclassifiedInk**.</span></span> <span data-ttu-id="df523-115">Попытка переместить штрих в любой другой тип объекта **иконтекстноде** приводит к возвращению значения **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="df523-115">Attempting to move a stroke to any other type of **IContextNode** object results in a return value of **E\_INVALIDARG**.</span></span>

<span data-ttu-id="df523-116">Этот метод может быть вызван из любого объекта [**иконтекстноде**](icontextnode.md) , включая нерукописные конечные **иконтекстноде** объекты.</span><span class="sxs-lookup"><span data-stu-id="df523-116">This method can be called from any [**IContextNode**](icontextnode.md) object, including non-ink leaf **IContextNode** objects.</span></span> <span data-ttu-id="df523-117">На указанный росчерк должен ссылаться один из потомков этого объекта **иконтекстноде** или возвращен **\_ INVALIDARG E** .</span><span class="sxs-lookup"><span data-stu-id="df523-117">The specified stroke must be referenced by one of the descendants of this **IContextNode** object or **E\_INVALIDARG** is returned.</span></span>

<span data-ttu-id="df523-118">Если [**иконтекстноде**](icontextnode.md) или **иконтекстноде** в *пконтекстнодедестинатион* подтвержден, возвращается **E \_ INVALIDARG** (см. [**иконтекстноде:: Confirm**](icontextnode-isconfirmed.md)).</span><span class="sxs-lookup"><span data-stu-id="df523-118">If either this [**IContextNode**](icontextnode.md) or the **IContextNode** in *pContextNodeDestination* is confirmed, **E\_INVALIDARG** is returned (see [**IContextNode::IsConfirmed**](icontextnode-isconfirmed.md)).</span></span>

<span data-ttu-id="df523-119">Анализатор рукописного ввода не удаляет пустые контекстные узлы из дерева результатов в ответ на этот метод.</span><span class="sxs-lookup"><span data-stu-id="df523-119">The ink analyzer does not delete empty context nodes from its results tree in response to this method.</span></span>

-   <span data-ttu-id="df523-120">Конечный узел рукописного ввода, который не ссылается на данные росчерка, является пустым узлом.</span><span class="sxs-lookup"><span data-stu-id="df523-120">An ink leaf node that does not reference any stroke data is an empty node.</span></span>
-   <span data-ttu-id="df523-121">Узел контейнера, не ссылающийся на какие-либо дочерние узлы, является пустым узлом.</span><span class="sxs-lookup"><span data-stu-id="df523-121">A container node that does not reference any child nodes is an empty node.</span></span>

<span data-ttu-id="df523-122">Пустой узел создает ошибки, если он находится в дереве во время операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="df523-122">An empty node generates errors if it is in the tree during an ink analysis operation.</span></span> <span data-ttu-id="df523-123">Чтобы удалить узел из дерева анализатора рукописного ввода, вызовите метод [**иконтекстноде::D елетесубноде**](icontextnode-deletesubnode.md) родительского узла (см. [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md)).</span><span class="sxs-lookup"><span data-stu-id="df523-123">To remove a node from the ink analyzer's tree, call the parent node's [**IContextNode::DeleteSubNode**](icontextnode-deletesubnode.md) method (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="df523-124">Требования</span><span class="sxs-lookup"><span data-stu-id="df523-124">Requirements</span></span>



| <span data-ttu-id="df523-125">Требование</span><span class="sxs-lookup"><span data-stu-id="df523-125">Requirement</span></span> | <span data-ttu-id="df523-126">Значение</span><span class="sxs-lookup"><span data-stu-id="df523-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df523-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df523-127">Minimum supported client</span></span><br/> | <span data-ttu-id="df523-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="df523-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="df523-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df523-129">Minimum supported server</span></span><br/> | <span data-ttu-id="df523-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="df523-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="df523-131">Header</span><span class="sxs-lookup"><span data-stu-id="df523-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="df523-132"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="df523-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="df523-133">DLL</span><span class="sxs-lookup"><span data-stu-id="df523-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df523-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df523-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="df523-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df523-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df523-136">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="df523-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="df523-137">**Иконтекстноде:: Сетстрокес**</span><span class="sxs-lookup"><span data-stu-id="df523-137">**IContextNode::SetStrokes**</span></span>](icontextnode-setstrokes.md)
</dt> <dt>

[<span data-ttu-id="df523-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="df523-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




