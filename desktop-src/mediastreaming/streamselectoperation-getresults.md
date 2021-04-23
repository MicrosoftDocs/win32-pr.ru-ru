---
title: Стреамселектоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Селектбестстреамасинк.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Стреамселектоператион
- API потоковой передачи мультимедиа интерфейса Стреамселектоператион, метод Results
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710269"
---
# <a name="streamselectoperationgetresults-method"></a><span data-ttu-id="2f318-106">Стреамселектоператион. results, метод</span><span class="sxs-lookup"><span data-stu-id="2f318-106">StreamSelectOperation.GetResults method</span></span>

<span data-ttu-id="2f318-107">Возвращает результаты асинхронной операции, запущенной [**селектбестстреамасинк**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f318-107">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f318-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f318-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="2f318-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f318-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f318-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2f318-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="2f318-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2f318-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="2f318-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f318-112">Return value</span></span>

<span data-ttu-id="2f318-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2f318-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2f318-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2f318-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2f318-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2f318-115">Return code</span></span>                                                                          | <span data-ttu-id="2f318-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2f318-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2f318-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2f318-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2f318-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2f318-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2f318-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f318-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f318-120">**стреамселектоператион**</span><span class="sxs-lookup"><span data-stu-id="2f318-120">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

