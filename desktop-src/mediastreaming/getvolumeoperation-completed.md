---
title: Жетволумеоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жетволумеасинк.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жетволумеоператион
- API потоковой передачи мультимедиа интерфейса Жетволумеоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21577d57e1e29aff1d2b12b92bcbef58a529eba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133746"
---
# <a name="getvolumeoperationcompleted-property"></a><span data-ttu-id="4f628-106">Жетволумеоператион. Completed, свойство</span><span class="sxs-lookup"><span data-stu-id="4f628-106">GetVolumeOperation.Completed property</span></span>

<span data-ttu-id="4f628-107">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетволумеасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) .</span><span class="sxs-lookup"><span data-stu-id="4f628-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span>

<span data-ttu-id="4f628-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4f628-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f628-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f628-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="4f628-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4f628-110">Property value</span></span>

<span data-ttu-id="4f628-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="4f628-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f628-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f628-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f628-113">**жетволумеоператион**</span><span class="sxs-lookup"><span data-stu-id="4f628-113">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

 