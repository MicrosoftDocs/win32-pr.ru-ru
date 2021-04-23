---
title: Каунтеритем. Value, свойство
description: Извлекает Последнее значение выборки счетчика.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Значение свойства Сисмон
- Свойство Value Сисмон, класс Каунтеритем
- Класс Каунтеритем Сисмон, свойство Value
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661920"
---
# <a name="counteritemvalue-property"></a><span data-ttu-id="2089e-106">Каунтеритем. Value, свойство</span><span class="sxs-lookup"><span data-stu-id="2089e-106">CounterItem.Value property</span></span>

<span data-ttu-id="2089e-107">Извлекает Последнее значение выборки счетчика.</span><span class="sxs-lookup"><span data-stu-id="2089e-107">Retrieves the last sampled value of the counter.</span></span>

<span data-ttu-id="2089e-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2089e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2089e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2089e-109">Syntax</span></span>


```VB
Property Value As Double
```



## <a name="property-value"></a><span data-ttu-id="2089e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2089e-110">Property value</span></span>

<span data-ttu-id="2089e-111">Последнее значение выборки счетчика.</span><span class="sxs-lookup"><span data-stu-id="2089e-111">Last sampled value of the counter.</span></span> <span data-ttu-id="2089e-112">При возникновении ошибки значение-1.</span><span class="sxs-lookup"><span data-stu-id="2089e-112">The value is -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="2089e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2089e-113">Remarks</span></span>

<span data-ttu-id="2089e-114">Это свойство по умолчанию объекта [**каунтеритем**](counteritem.md) .</span><span class="sxs-lookup"><span data-stu-id="2089e-114">This is the default property of the [**CounterItem**](counteritem.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2089e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2089e-115">Requirements</span></span>



| <span data-ttu-id="2089e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2089e-116">Requirement</span></span> | <span data-ttu-id="2089e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2089e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2089e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2089e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2089e-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2089e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2089e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2089e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2089e-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2089e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2089e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2089e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2089e-123"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="2089e-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2089e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2089e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2089e-125">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="2089e-125">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="2089e-126">**Каунтеритем. GetValue**</span><span class="sxs-lookup"><span data-stu-id="2089e-126">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





