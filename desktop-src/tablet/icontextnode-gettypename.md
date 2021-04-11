---
description: Возвращает удобное для чтения имя типа этого Иконтекстноде.
ms.assetid: 02031efd-1e9c-4e96-8dc1-280cc1a6e58f
title: Метод Иконтекстноде::-TypeName (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetTypeName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9d7bc4a24b7abc3ee507d7bda0c547f4c55a787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145514"
---
# <a name="icontextnodegettypename-method"></a><span data-ttu-id="db1d0-103">Метод Иконтекстноде:: имя_типа</span><span class="sxs-lookup"><span data-stu-id="db1d0-103">IContextNode::GetTypeName method</span></span>

<span data-ttu-id="db1d0-104">Возвращает удобное для чтения имя типа этого [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="db1d0-104">Retrieves a human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="db1d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db1d0-105">Syntax</span></span>


```C++
HRESULT GetTypeName(
  [out] BSTR *pbstrContextNodeType
);
```



## <a name="parameters"></a><span data-ttu-id="db1d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db1d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db1d0-107">*пбстрконтекстнодетипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db1d0-107">*pbstrContextNodeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db1d0-108">Понятное для человека имя типа этого [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="db1d0-108">A human-readable type name of this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db1d0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db1d0-109">Return value</span></span>

<span data-ttu-id="db1d0-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="db1d0-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="db1d0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db1d0-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="db1d0-112">Чтобы избежать утечки памяти, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для \* *пбстрконтекстнодетипе* , когда больше не нужно использовать строку.</span><span class="sxs-lookup"><span data-stu-id="db1d0-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrContextNodeType* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="db1d0-113">Например, этот метод устанавливает *пбстрконтекстнодетипе* в значение "инквордноде" для узла рукописного слова (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md) и [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="db1d0-113">For example, this method sets *pbstrContextNodeType* to "InkWordNode" for an ink word node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="db1d0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="db1d0-114">Requirements</span></span>



| <span data-ttu-id="db1d0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="db1d0-115">Requirement</span></span> | <span data-ttu-id="db1d0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="db1d0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db1d0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db1d0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db1d0-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="db1d0-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="db1d0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db1d0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db1d0-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="db1d0-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="db1d0-121">Header</span><span class="sxs-lookup"><span data-stu-id="db1d0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="db1d0-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="db1d0-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="db1d0-123">DLL</span><span class="sxs-lookup"><span data-stu-id="db1d0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db1d0-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db1d0-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="db1d0-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db1d0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db1d0-126">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="db1d0-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="db1d0-127">**Иконтекстноде:: GetType**</span><span class="sxs-lookup"><span data-stu-id="db1d0-127">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="db1d0-128">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="db1d0-128">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="db1d0-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="db1d0-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

