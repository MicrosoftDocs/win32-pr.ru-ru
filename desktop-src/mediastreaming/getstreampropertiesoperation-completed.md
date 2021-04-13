---
title: Жетстреампропертиесоператион. Completed, свойство
description: Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной Жетстреампропертиесасинк.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- Законченное свойство потоковой передачи мультимедиа API
- Завершенное свойство потоковой передачи мультимедиа API, интерфейс Жетстреампропертиесоператион
- API потоковой передачи мультимедиа интерфейса Жетстреампропертиесоператион, завершенное свойство
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412861"
---
# <a name="getstreampropertiesoperationcompleted-property"></a><span data-ttu-id="4c3e3-106">Жетстреампропертиесоператион. Completed, свойство</span><span class="sxs-lookup"><span data-stu-id="4c3e3-106">GetStreamPropertiesOperation.Completed property</span></span>

<span data-ttu-id="4c3e3-107">Возвращает или задает обработчик событий, который вызывается при завершении асинхронной операции, запущенной [**жетстреампропертиесасинк**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4c3e3-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) is completed.</span></span>

<span data-ttu-id="4c3e3-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3e3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c3e3-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="4c3e3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4c3e3-110">Property value</span></span>

<span data-ttu-id="4c3e3-111">Обработчик событий.</span><span class="sxs-lookup"><span data-stu-id="4c3e3-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c3e3-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c3e3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3e3-113">**жетстреампропертиесоператион**</span><span class="sxs-lookup"><span data-stu-id="4c3e3-113">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

 