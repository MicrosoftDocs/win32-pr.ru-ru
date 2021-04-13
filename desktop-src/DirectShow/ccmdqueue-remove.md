---
description: Метод Remove удаляет объект Кдеферредкомманд из очереди.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Метод Ккмдкуеуе. Remove (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657969"
---
# <a name="ccmdqueueremove-method"></a><span data-ttu-id="d9c0b-103">Ккмдкуеуе. Remove, метод</span><span class="sxs-lookup"><span data-stu-id="d9c0b-103">CCmdQueue.Remove method</span></span>

<span data-ttu-id="d9c0b-104">`Remove`Метод удаляет объект [**кдеферредкомманд**](cdeferredcommand.md) из очереди.</span><span class="sxs-lookup"><span data-stu-id="d9c0b-104">The `Remove` method removes the [**CDeferredCommand**](cdeferredcommand.md) object from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9c0b-105">Syntax</span></span>


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="d9c0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9c0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9c0b-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="d9c0b-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="d9c0b-108">Указатель на объект **кдеферредкомманд** , который необходимо удалить из очереди.</span><span class="sxs-lookup"><span data-stu-id="d9c0b-108">Pointer to the **CDeferredCommand** object to remove from the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9c0b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9c0b-109">Return value</span></span>

<span data-ttu-id="d9c0b-110">Возвращает VFW \_ E \_ не \_ найден, если объект не найден в очереди.</span><span class="sxs-lookup"><span data-stu-id="d9c0b-110">Returns VFW\_E\_NOT\_FOUND if the object is not found in the queue.</span></span> <span data-ttu-id="d9c0b-111">В противном случае возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d9c0b-111">Otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c0b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="d9c0b-112">Requirements</span></span>



| <span data-ttu-id="d9c0b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d9c0b-113">Requirement</span></span> | <span data-ttu-id="d9c0b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d9c0b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c0b-115">Header</span><span class="sxs-lookup"><span data-stu-id="d9c0b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d9c0b-116"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9c0b-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d9c0b-117">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9c0b-117">Library</span></span><br/> | <dl> <span data-ttu-id="d9c0b-118"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="d9c0b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9c0b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9c0b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c0b-120">**Класс Ккмдкуеуе**</span><span class="sxs-lookup"><span data-stu-id="d9c0b-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




