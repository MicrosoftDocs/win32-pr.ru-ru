---
description: Метод «, помечающий» Возвращает флаги контекста, связанные с отложенной командой.
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: Метод Кдеферредкомманд. «flags» (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680012"
---
# <a name="cdeferredcommandgetflags-method"></a><span data-ttu-id="01fd2-103">Кдеферредкомманд... flags, метод</span><span class="sxs-lookup"><span data-stu-id="01fd2-103">CDeferredCommand.GetFlags method</span></span>

<span data-ttu-id="01fd2-104">`GetFlags`Метод получает флаги контекста, связанные с отложенной командой.</span><span class="sxs-lookup"><span data-stu-id="01fd2-104">The `GetFlags` method retrieves the context flags associated with the deferred command.</span></span>

## <a name="syntax"></a><span data-ttu-id="01fd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01fd2-105">Syntax</span></span>


```C++
short GetFlags();
```



## <a name="parameters"></a><span data-ttu-id="01fd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01fd2-106">Parameters</span></span>

<span data-ttu-id="01fd2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="01fd2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01fd2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01fd2-108">Return value</span></span>

<span data-ttu-id="01fd2-109">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="01fd2-109">Returns one of the following:</span></span>



| <span data-ttu-id="01fd2-110">Код возврата</span><span class="sxs-lookup"><span data-stu-id="01fd2-110">Return code</span></span>                                                                                             | <span data-ttu-id="01fd2-111">Описание</span><span class="sxs-lookup"><span data-stu-id="01fd2-111">Description</span></span>                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01fd2-112"><dt>**\_метод Dispatch**</dt></span><span class="sxs-lookup"><span data-stu-id="01fd2-112"><dt>**DISPATCH\_METHOD**</dt></span></span> </dl>         | <span data-ttu-id="01fd2-113">Запустите член как метод.</span><span class="sxs-lookup"><span data-stu-id="01fd2-113">Run the member as a method.</span></span> <span data-ttu-id="01fd2-114">Если свойство имеет такое же имя, \_ можно задать и флаг диспетчеризации пропертижет.</span><span class="sxs-lookup"><span data-stu-id="01fd2-114">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span><br/>                                               |
| <dl> <span data-ttu-id="01fd2-115"><dt>**\_ПРОПЕРТИЖЕТ диспетчеризации**</dt></span><span class="sxs-lookup"><span data-stu-id="01fd2-115"><dt>**DISPATCH\_PROPERTYGET**</dt></span></span> </dl>    | <span data-ttu-id="01fd2-116">Элемент извлекается как свойство или элемент данных.</span><span class="sxs-lookup"><span data-stu-id="01fd2-116">The member is being retrieved as a property or data member.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="01fd2-117"><dt>**\_ПРОПЕРТИПУТ диспетчеризации**</dt></span><span class="sxs-lookup"><span data-stu-id="01fd2-117"><dt>**DISPATCH\_PROPERTYPUT**</dt></span></span> </dl>    | <span data-ttu-id="01fd2-118">Элемент изменяется как свойство или элемент данных.</span><span class="sxs-lookup"><span data-stu-id="01fd2-118">The member is being changed as a property or data member.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="01fd2-119"><dt>**\_ПРОПЕРТИПУТРЕФ диспетчеризации**</dt></span><span class="sxs-lookup"><span data-stu-id="01fd2-119"><dt>**DISPATCH\_PROPERTYPUTREF**</dt></span></span> </dl> | <span data-ttu-id="01fd2-120">Элемент изменяется с помощью ссылочного назначения, а не назначения значения.</span><span class="sxs-lookup"><span data-stu-id="01fd2-120">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="01fd2-121">Этот флаг допустим, только если свойство принимает ссылку на объект.</span><span class="sxs-lookup"><span data-stu-id="01fd2-121">This flag is valid only when the property accepts a reference to an object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="01fd2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="01fd2-122">Requirements</span></span>



| <span data-ttu-id="01fd2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="01fd2-123">Requirement</span></span> | <span data-ttu-id="01fd2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="01fd2-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01fd2-125">Header</span><span class="sxs-lookup"><span data-stu-id="01fd2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="01fd2-126"><dt>Ктлутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01fd2-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01fd2-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="01fd2-127">Library</span></span><br/> | <dl> <span data-ttu-id="01fd2-128"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="01fd2-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01fd2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="01fd2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01fd2-130">**Класс Кдеферредкомманд**</span><span class="sxs-lookup"><span data-stu-id="01fd2-130">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




