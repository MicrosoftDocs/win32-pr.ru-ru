---
title: активатионфаилурелоггинглевел
description: Задает уровень детализации записей журнала событий о неудачных запросах для запуска и активации компонента.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- COM-значение реестра Активатионфаилурелоггинглевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411393"
---
# <a name="activationfailurelogginglevel"></a><span data-ttu-id="c6f95-104">активатионфаилурелоггинглевел</span><span class="sxs-lookup"><span data-stu-id="c6f95-104">ActivationFailureLoggingLevel</span></span>

<span data-ttu-id="c6f95-105">Задает уровень детализации записей журнала событий о неудачных запросах для запуска и активации компонента.</span><span class="sxs-lookup"><span data-stu-id="c6f95-105">Sets the verbosity of event log entries about failed requests for component launch and activation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c6f95-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="c6f95-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="c6f95-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6f95-107">Remarks</span></span>

<span data-ttu-id="c6f95-108">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c6f95-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="c6f95-109">Значение</span><span class="sxs-lookup"><span data-stu-id="c6f95-109">Value</span></span> | <span data-ttu-id="c6f95-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c6f95-110">Description</span></span>                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f95-111">0</span><span class="sxs-lookup"><span data-stu-id="c6f95-111">0</span></span>     | <span data-ttu-id="c6f95-112">Используйте ведение журнала на уровне пользователей.</span><span class="sxs-lookup"><span data-stu-id="c6f95-112">Use discretionary logging.</span></span> <span data-ttu-id="c6f95-113">Заносить в журнал ошибки по умолчанию, но клиенты могут переопределить это поведение, указав КЛСКТКС \_ без \_ \_ журнала сбоев в [**кокреатеинстанцеекс**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span><span class="sxs-lookup"><span data-stu-id="c6f95-113">Log failures by default, but clients can override this behavior by specifying CLSCTX\_NO\_FAILURE\_LOG in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex).</span></span> <span data-ttu-id="c6f95-114">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6f95-114">This is the default value.</span></span> |
| <span data-ttu-id="c6f95-115">1</span><span class="sxs-lookup"><span data-stu-id="c6f95-115">1</span></span>     | <span data-ttu-id="c6f95-116">Всегда регистрировать все сбои независимо от указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="c6f95-116">Always log all failures no matter what the client specified.</span></span>                                                                                                                                                      |
| <span data-ttu-id="c6f95-117">2</span><span class="sxs-lookup"><span data-stu-id="c6f95-117">2</span></span>     | <span data-ttu-id="c6f95-118">Никогда не заносить в журнал все сбои вне зависимости от указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="c6f95-118">Never log any failures no matter what the client specified.</span></span>                                                                                                                                                       |



 

<span data-ttu-id="c6f95-119">Если требуется приложение для управления ведением журнала событий, рекомендуется присвоить этому параметру значение 0 и написать клиентский код для его переопределения при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c6f95-119">If you need an application to control event logging, it is recommended that you set this value to 0 and write the client code to override it when needed.</span></span> <span data-ttu-id="c6f95-120">Настоятельно рекомендуется не задавать значение 2.</span><span class="sxs-lookup"><span data-stu-id="c6f95-120">It is strongly recommended that you do not set the value to 2.</span></span> <span data-ttu-id="c6f95-121">Если ведение журнала событий отключено, трудно диагностировать проблемы.</span><span class="sxs-lookup"><span data-stu-id="c6f95-121">If event logging is disabled, it is more difficult to diagnose problems.</span></span> <span data-ttu-id="c6f95-122">Для сбоев разрешений на компьютеры, где в COM нет битов КЛСКТКС, COM будет рассматривать значение 0 как 1.</span><span class="sxs-lookup"><span data-stu-id="c6f95-122">For machine restrictions permission failures, where COM does not have the CLSCTX bits, COM will treat a value of 0 as 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6f95-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c6f95-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6f95-124">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="c6f95-124">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




