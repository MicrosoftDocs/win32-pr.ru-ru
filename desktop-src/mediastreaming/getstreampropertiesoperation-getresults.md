---
title: Жетстреампропертиесоператион. results, метод
description: Возвращает результаты асинхронной операции, запущенной Жетстреампропертиесасинк.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- API потоковой передачи мультимедиа метода
- API потоковой передачи мультимедиа, интерфейс Жетстреампропертиесоператион
- API потоковой передачи мультимедиа интерфейса Жетстреампропертиесоператион, метод Results
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412880"
---
# <a name="getstreampropertiesoperationgetresults-method"></a><span data-ttu-id="a3e38-106">Жетстреампропертиесоператион. results, метод</span><span class="sxs-lookup"><span data-stu-id="a3e38-106">GetStreamPropertiesOperation.GetResults method</span></span>

<span data-ttu-id="a3e38-107">Возвращает результаты асинхронной операции, запущенной [**жетстреампропертиесасинк**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a3e38-107">Returns the results of the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e38-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3e38-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="a3e38-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a3e38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e38-110">*значение* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a3e38-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="a3e38-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a3e38-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="a3e38-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a3e38-112">Return value</span></span>

<span data-ttu-id="a3e38-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a3e38-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a3e38-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a3e38-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a3e38-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a3e38-115">Return code</span></span>                                                                          | <span data-ttu-id="a3e38-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a3e38-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a3e38-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a3e38-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a3e38-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a3e38-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a3e38-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3e38-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e38-120">**жетстреампропертиесоператион**</span><span class="sxs-lookup"><span data-stu-id="a3e38-120">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

