---
title: Плайбаккоператион. Completed, свойство
description: Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной одним из методов воспроизведения Медиарендерер.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Плайбаккоператион
- API потоковой передачи мультимедиа интерфейса Плайбаккоператион, завершенное свойство
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105710191"
---
# <a name="playbackoperationcompleted-property"></a><span data-ttu-id="dfa46-106">Плайбаккоператион. Completed, свойство</span><span class="sxs-lookup"><span data-stu-id="dfa46-106">PlaybackOperation.Completed property</span></span>

<span data-ttu-id="dfa46-107">Возвращает или задает обработчик событий, вызываемый при завершении асинхронной операции, запущенной одним из методов воспроизведения [**медиарендерер**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="dfa46-107">Gets or sets an event handler that is invoked when the asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods is completed.</span></span>

<span data-ttu-id="dfa46-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dfa46-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa46-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfa46-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="dfa46-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dfa46-110">Property value</span></span>

<span data-ttu-id="dfa46-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="dfa46-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="dfa46-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfa46-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa46-113">**плайбаккоператион**</span><span class="sxs-lookup"><span data-stu-id="dfa46-113">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 




