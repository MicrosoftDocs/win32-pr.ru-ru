---
title: Креатемедиарендерероператион. Completed, свойство
description: Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной Креатемедиарендерерасинк или Креатемедиарендерерфромбасикдевицеасинк.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Креатемедиарендерероператион
- API потоковой передачи мультимедиа интерфейса Креатемедиарендерероператион, завершенное свойство
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783954"
---
# <a name="createmediarendereroperationcompleted-property"></a><span data-ttu-id="2d653-106">Креатемедиарендерероператион. Completed, свойство</span><span class="sxs-lookup"><span data-stu-id="2d653-106">CreateMediaRendererOperation.Completed property</span></span>

<span data-ttu-id="2d653-107">Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной [**креатемедиарендерерасинк**](imediarendererfactory-createmediarendererasync.md) или [**креатемедиарендерерфромбасикдевицеасинк**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) .</span><span class="sxs-lookup"><span data-stu-id="2d653-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span>

<span data-ttu-id="2d653-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="2d653-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d653-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d653-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a><span data-ttu-id="2d653-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2d653-110">Property value</span></span>

<span data-ttu-id="2d653-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="2d653-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d653-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d653-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d653-113">**креатемедиарендерероператион**</span><span class="sxs-lookup"><span data-stu-id="2d653-113">**CreateMediaRendererOperation**</span></span>](createmediarendereroperation.md)
</dt> </dl>

 

 




