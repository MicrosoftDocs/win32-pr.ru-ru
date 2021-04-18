---
title: Ивмпкдромбурн Бурнпрогресс, свойство
description: Свойство Бурнпрогресс возвращает ход выполнения записи компакт-диска в процентах завершения.
ms.assetid: 831cc55d-bd26-4328-a715-1a1fa48d7a40
keywords:
- Проигрыватель Windows Media для свойства Бурнпрогресс
- Бурнпрогресс свойство проигрывателя Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, свойство Бурнпрогресс
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnProgress
- IWMPCdromBurn.get_burnProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 835c8c1091941437c226427ddb3ef53e8c577b5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717991"
---
# <a name="iwmpcdromburnburnprogress-property"></a><span data-ttu-id="c6a68-106">Свойство Ивмпкдромбурн:: Бурнпрогресс</span><span class="sxs-lookup"><span data-stu-id="c6a68-106">IWMPCdromBurn::burnProgress property</span></span>

<span data-ttu-id="c6a68-107">Свойство **бурнпрогресс** возвращает ход выполнения записи компакт-диска в процентах завершения.</span><span class="sxs-lookup"><span data-stu-id="c6a68-107">The **burnProgress** property gets the CD burning progress as percent complete.</span></span>

<span data-ttu-id="c6a68-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c6a68-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6a68-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6a68-109">Syntax</span></span>


```CSharp
public System.Int32 burnProgress {get;}
```


```VB

Public ReadOnly Property burnProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="c6a68-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c6a68-110">Property value</span></span>

<span data-ttu-id="c6a68-111">Значение **System. Int32** , которое является значением хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c6a68-111">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="c6a68-112">Значения хода выполнения находятся в диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="c6a68-112">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a68-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6a68-113">Remarks</span></span>

<span data-ttu-id="c6a68-114">Значение Progress представляет завершенный процент всего процесса записи, включая все промежуточные операции.</span><span class="sxs-lookup"><span data-stu-id="c6a68-114">The progress value represents the completed percentage of the entire burning process, including any staging operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a68-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c6a68-115">Requirements</span></span>



| <span data-ttu-id="c6a68-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c6a68-116">Requirement</span></span> | <span data-ttu-id="c6a68-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c6a68-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a68-118">Версия</span><span class="sxs-lookup"><span data-stu-id="c6a68-118">Version</span></span><br/>   | <span data-ttu-id="c6a68-119">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="c6a68-119">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="c6a68-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c6a68-120">Namespace</span></span><br/> | <span data-ttu-id="c6a68-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="c6a68-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c6a68-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="c6a68-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c6a68-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c6a68-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a68-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6a68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a68-125">**Интерфейс Ивмпкдромбурн (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="c6a68-125">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





