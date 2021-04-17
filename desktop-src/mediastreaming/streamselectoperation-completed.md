---
title: Стреамселектоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Селектбестстреамасинк.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Стреамселектоператион
- API потоковой передачи мультимедиа интерфейса Стреамселектоператион, завершенное свойство
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710270"
---
# <a name="streamselectoperationcompleted-property"></a><span data-ttu-id="888d1-106">Стреамселектоператион. Completed, свойство</span><span class="sxs-lookup"><span data-stu-id="888d1-106">StreamSelectOperation.Completed property</span></span>

<span data-ttu-id="888d1-107">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**селектбестстреамасинк**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="888d1-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span>

<span data-ttu-id="888d1-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="888d1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="888d1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="888d1-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="888d1-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="888d1-110">Property value</span></span>

<span data-ttu-id="888d1-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="888d1-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="888d1-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="888d1-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888d1-113">**стреамселектоператион**</span><span class="sxs-lookup"><span data-stu-id="888d1-113">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

 