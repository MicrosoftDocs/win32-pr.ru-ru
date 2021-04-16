---
title: Каунтеритем. Скалефактор, свойство
description: Возвращает или задает коэффициент масштабирования, используемый для отображения значения счетчика.
ms.assetid: 8589c0e6-b1c1-4d85-a21e-3e76afee67b1
keywords:
- Сисмон свойство Скалефактор
- Скалефактор Property Сисмон, класс Каунтеритем
- Класс Каунтеритем Сисмон, свойство Скалефактор
topic_type:
- apiref
api_name:
- CounterItem.ScaleFactor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9a04df634fe54c82230ade679afb3259519173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661921"
---
# <a name="counteritemscalefactor-property"></a><span data-ttu-id="5e88e-106">Каунтеритем. Скалефактор, свойство</span><span class="sxs-lookup"><span data-stu-id="5e88e-106">CounterItem.ScaleFactor property</span></span>

<span data-ttu-id="5e88e-107">Возвращает или задает коэффициент масштабирования, используемый для отображения значения счетчика.</span><span class="sxs-lookup"><span data-stu-id="5e88e-107">Retrieves or sets the scale factor used to graph the counter value.</span></span>

<span data-ttu-id="5e88e-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5e88e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e88e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e88e-109">Syntax</span></span>


```VB
Property ScaleFactor As Long
```



## <a name="property-value"></a><span data-ttu-id="5e88e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5e88e-110">Property value</span></span>

<span data-ttu-id="5e88e-111">Коэффициент масштабирования, используемый при отображении значений счетчиков на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="5e88e-111">Scale factor used in displaying the graphed counter values.</span></span> <span data-ttu-id="5e88e-112">Допустимы значения в диапазоне от-9 до 9 (значения соответствуют 0,000000001-100000000,0).</span><span class="sxs-lookup"><span data-stu-id="5e88e-112">Valid values range from -9 to 9 (the values correspond to 0.000000001 - 100000000.0).</span></span>

<span data-ttu-id="5e88e-113">**До Windows Vista:** Допустимы значения в диапазоне от-7 до 7 (значения соответствуют 0,0000001-1000000,0).</span><span class="sxs-lookup"><span data-stu-id="5e88e-113">**Prior to Windows Vista:** Valid values range from -7 to 7 (the values correspond to 0.0000001 - 1000000.0).</span></span>

## <a name="remarks"></a><span data-ttu-id="5e88e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5e88e-114">Remarks</span></span>

<span data-ttu-id="5e88e-115">Это свойство следует задавать только в том случае, если требуется изменить коэффициент масштабирования по умолчанию счетчика (каждый счетчик определяет свой собственный коэффициент масштабирования).</span><span class="sxs-lookup"><span data-stu-id="5e88e-115">Only set this property if you want to change the counter's default scale factor (each counter defines its own scale factor).</span></span> <span data-ttu-id="5e88e-116">Значение этого свойства равно Integer. MaxValue, если счетчик использует коэффициент масштабирования по умолчанию для отображения значений.</span><span class="sxs-lookup"><span data-stu-id="5e88e-116">The value of this property is set to Integer.MaxValue if the counter is using its default scale factor to graph the values.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e88e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5e88e-117">Requirements</span></span>



| <span data-ttu-id="5e88e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5e88e-118">Requirement</span></span> | <span data-ttu-id="5e88e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5e88e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e88e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5e88e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5e88e-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5e88e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5e88e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5e88e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5e88e-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5e88e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e88e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5e88e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e88e-125"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="5e88e-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e88e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e88e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e88e-127">**каунтеритем**</span><span class="sxs-lookup"><span data-stu-id="5e88e-127">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="5e88e-128">**Системмонитор. Скалетофит**</span><span class="sxs-lookup"><span data-stu-id="5e88e-128">**SystemMonitor.ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
</dt> </dl>

 

 





