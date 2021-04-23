---
description: Перемещает этот объект Иконтекстноде из коллекции дочерних узлов родительского узла в указанную коллекцию подузлов узла контекста.
ms.assetid: e19ecbe3-f7aa-499c-86a1-236dc9056fd9
title: 'Метод Иконтекстноде:: reparent (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Reparent
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 805b96b2a392a4f7b70aa4ce5913b48ffaf33551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072782"
---
# <a name="icontextnodereparent-method"></a><span data-ttu-id="0c43a-103">Метод Иконтекстноде:: reparent</span><span class="sxs-lookup"><span data-stu-id="0c43a-103">IContextNode::Reparent method</span></span>

<span data-ttu-id="0c43a-104">Перемещает этот объект [**иконтекстноде**](icontextnode.md) из коллекции дочерних узлов родительского узла в указанную коллекцию подузлов узла контекста.</span><span class="sxs-lookup"><span data-stu-id="0c43a-104">Moves this [**IContextNode**](icontextnode.md) object from its parent context node's collection of subnodes to the specified context node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c43a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c43a-105">Syntax</span></span>


```C++
HRESULT Reparent(
  [in] IContextNode *pNewParent
);
```



## <a name="parameters"></a><span data-ttu-id="0c43a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c43a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c43a-107">*пневпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0c43a-107">*pNewParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c43a-108">Новый родительский узел для этого объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="0c43a-108">The new parent node for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c43a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c43a-109">Return value</span></span>

<span data-ttu-id="0c43a-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0c43a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c43a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="0c43a-111">Requirements</span></span>



| <span data-ttu-id="0c43a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="0c43a-112">Requirement</span></span> | <span data-ttu-id="0c43a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0c43a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c43a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c43a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0c43a-115">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0c43a-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0c43a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c43a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0c43a-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c43a-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0c43a-118">Header</span><span class="sxs-lookup"><span data-stu-id="0c43a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c43a-119"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0c43a-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0c43a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0c43a-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c43a-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c43a-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0c43a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c43a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c43a-123">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="0c43a-123">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="0c43a-124">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="0c43a-124">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="0c43a-125">**Иконтекстноде:: Жетсубнодес**</span><span class="sxs-lookup"><span data-stu-id="0c43a-125">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="0c43a-126">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="0c43a-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




