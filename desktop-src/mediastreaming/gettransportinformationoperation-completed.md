---
title: Жеттранспортинформатионоператион завершенное свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жеттранспортинформатионасинк.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жеттранспортинформатионоператион
- API потоковой передачи мультимедиа интерфейса Жеттранспортинформатионоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700853"
---
# <a name="gettransportinformationoperationcompleted-property"></a><span data-ttu-id="e2db8-106">Свойство Жеттранспортинформатионоператион:: Completed</span><span class="sxs-lookup"><span data-stu-id="e2db8-106">GetTransportInformationOperation::Completed property</span></span>

<span data-ttu-id="e2db8-107">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жеттранспортинформатионасинк**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) .</span><span class="sxs-lookup"><span data-stu-id="e2db8-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span>

<span data-ttu-id="e2db8-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="e2db8-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2db8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2db8-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="e2db8-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e2db8-110">Property value</span></span>

<span data-ttu-id="e2db8-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="e2db8-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2db8-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2db8-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2db8-113">**жеттранспортинформатионоператион**</span><span class="sxs-lookup"><span data-stu-id="e2db8-113">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

 