---
description: Освобождает \_ контекст цепочки пкцерт, \_ полученный через свойство чаинконтекст.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Метод Ичаинконтекст:: Фриконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688943"
---
# <a name="ichaincontextfreecontext-method"></a><span data-ttu-id="69fd2-103">Метод Ичаинконтекст:: Фриконтекст</span><span class="sxs-lookup"><span data-stu-id="69fd2-103">IChainContext::FreeContext method</span></span>

<span data-ttu-id="69fd2-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="69fd2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="69fd2-105">Метод **фриконтекст** освобождает \_ контекст цепочки пкцерт, \_ полученный через свойство [**чаинконтекст**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="69fd2-105">The **FreeContext** method releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="69fd2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69fd2-106">Syntax</span></span>


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a><span data-ttu-id="69fd2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="69fd2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69fd2-108">*пчаинконтекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="69fd2-108">*pChainContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69fd2-109">\_Освобождаемый контекст цепочки пкцерт \_ .</span><span class="sxs-lookup"><span data-stu-id="69fd2-109">The PCCERT\_CHAIN\_CONTEXT to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69fd2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69fd2-110">Return value</span></span>

<span data-ttu-id="69fd2-111">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="69fd2-111">The return value is an **HRESULT**.</span></span> <span data-ttu-id="69fd2-112">Значение S \_ ОК указывает на успешное выполнение.</span><span class="sxs-lookup"><span data-stu-id="69fd2-112">A value of S\_OK indicates success.</span></span> <span data-ttu-id="69fd2-113">Любое другое значение указывает на сбой операции.</span><span class="sxs-lookup"><span data-stu-id="69fd2-113">Any other value indicates that the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="69fd2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69fd2-114">Remarks</span></span>

<span data-ttu-id="69fd2-115">Этот метод не освобождает \_ контекст цепочки пкцерт, \_ содержащийся в объекте [**цепочки**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="69fd2-115">This method does not release the PCCERT\_CHAIN\_CONTEXT contained within a [**Chain**](chain.md) object.</span></span> <span data-ttu-id="69fd2-116">Он должен использоваться только для освобождения \_ контекста цепочки пкцерт, \_ полученного через свойство [**чаинконтекст**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="69fd2-116">It should be used only to release a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="69fd2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="69fd2-117">Requirements</span></span>



| <span data-ttu-id="69fd2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="69fd2-118">Requirement</span></span> | <span data-ttu-id="69fd2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="69fd2-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69fd2-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="69fd2-120">Redistributable</span></span><br/> | <span data-ttu-id="69fd2-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="69fd2-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="69fd2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="69fd2-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="69fd2-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69fd2-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69fd2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69fd2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69fd2-125">**ичаинконтекст**</span><span class="sxs-lookup"><span data-stu-id="69fd2-125">**IChainContext**</span></span>](ichaincontext.md)
</dt> </dl>

 

 




