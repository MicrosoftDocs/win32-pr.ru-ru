---
description: Создает объект Иконтекстнодес.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'Метод Иинканализер:: Креатеконтекстнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711117"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a><span data-ttu-id="36350-103">Метод Иинканализер:: Креатеконтекстнодес</span><span class="sxs-lookup"><span data-stu-id="36350-103">IInkAnalyzer::CreateContextNodes method</span></span>

<span data-ttu-id="36350-104">Создает объект [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="36350-104">Creates an [**IContextNodes**](icontextnodes.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="36350-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36350-105">Syntax</span></span>


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="36350-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36350-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36350-107">*ппконтекстнодес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="36350-107">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36350-108">Указатель на объект [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="36350-108">A pointer to the [**IContextNodes**](icontextnodes.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36350-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36350-109">Return value</span></span>

<span data-ttu-id="36350-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="36350-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="36350-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36350-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="36350-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодес* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="36350-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodes* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="36350-113">Используйте этот метод, чтобы создать пустую коллекцию [**иконтекстнодес**](icontextnodes.md) , связанную с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="36350-113">Use this method to create an empty [**IContextNodes**](icontextnodes.md) collection that is associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="36350-114">Новая коллекция **иконтекстнодес** не является частью дерева контекста объекта **иинканализер** .</span><span class="sxs-lookup"><span data-stu-id="36350-114">The new **IContextNodes** collection is not part of the **IInkAnalyzer** object's context tree.</span></span>

## <a name="requirements"></a><span data-ttu-id="36350-115">Требования</span><span class="sxs-lookup"><span data-stu-id="36350-115">Requirements</span></span>



| <span data-ttu-id="36350-116">Требование</span><span class="sxs-lookup"><span data-stu-id="36350-116">Requirement</span></span> | <span data-ttu-id="36350-117">Значение</span><span class="sxs-lookup"><span data-stu-id="36350-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36350-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36350-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36350-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="36350-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="36350-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36350-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36350-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="36350-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="36350-122">Header</span><span class="sxs-lookup"><span data-stu-id="36350-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36350-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="36350-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="36350-124">DLL</span><span class="sxs-lookup"><span data-stu-id="36350-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36350-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36350-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="36350-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36350-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36350-127">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="36350-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="36350-128">**иконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="36350-128">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="36350-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="36350-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

