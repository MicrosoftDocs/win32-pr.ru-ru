---
title: Жетмутеоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жетмутеасинк.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жетмутеоператион
- API потоковой передачи мультимедиа интерфейса Жетмутеоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791083"
---
# <a name="getmuteoperationcompleted-property"></a><span data-ttu-id="0edaf-106">Жетмутеоператион. Completed, свойство</span><span class="sxs-lookup"><span data-stu-id="0edaf-106">GetMuteOperation.Completed property</span></span>

<span data-ttu-id="0edaf-107">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетмутеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) .</span><span class="sxs-lookup"><span data-stu-id="0edaf-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span>

<span data-ttu-id="0edaf-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0edaf-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0edaf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0edaf-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="0edaf-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0edaf-110">Property value</span></span>

<span data-ttu-id="0edaf-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="0edaf-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="0edaf-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0edaf-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0edaf-113">**жетмутеоператион**</span><span class="sxs-lookup"><span data-stu-id="0edaf-113">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

 