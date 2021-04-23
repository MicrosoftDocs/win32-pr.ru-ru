---
title: Жетпоситионинформатионоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жетпоситионинформатионасинк.
ms.assetid: 144065AE-6C23-4E9D-B9D0-6849E7FB74C4
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жетпоситионинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жетпоситионинформатионоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90b4ed4a6402b8c7bfc1ee559bd0b43765a64cec
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412929"
---
# <a name="getpositioninformationoperationcompleted-property"></a><span data-ttu-id="615f9-106">Жетпоситионинформатионоператион. Completed, свойство</span><span class="sxs-lookup"><span data-stu-id="615f9-106">GetPositionInformationOperation.Completed property</span></span>

<span data-ttu-id="615f9-107">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетпоситионинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) .</span><span class="sxs-lookup"><span data-stu-id="615f9-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync) is completed.</span></span>

<span data-ttu-id="615f9-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="615f9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="615f9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="615f9-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetPositionInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetPositionInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="615f9-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="615f9-110">Property value</span></span>

<span data-ttu-id="615f9-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="615f9-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="615f9-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="615f9-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="615f9-113">**жетпоситионинформатионоператион**</span><span class="sxs-lookup"><span data-stu-id="615f9-113">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

 