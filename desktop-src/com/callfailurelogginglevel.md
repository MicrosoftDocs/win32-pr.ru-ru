---
title: каллфаилурелоггинглевел
description: Задает уровень детализации записей журнала событий о неудачных вызовах компонентов.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- COM-значение реестра Каллфаилурелоггинглевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888123"
---
# <a name="callfailurelogginglevel"></a><span data-ttu-id="ba9fd-104">каллфаилурелоггинглевел</span><span class="sxs-lookup"><span data-stu-id="ba9fd-104">CallFailureLoggingLevel</span></span>

<span data-ttu-id="ba9fd-105">Задает уровень детализации записей журнала событий о неудачных вызовах компонентов.</span><span class="sxs-lookup"><span data-stu-id="ba9fd-105">Sets the verbosity of event log entries about failed calls to components.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ba9fd-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="ba9fd-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="ba9fd-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba9fd-107">Remarks</span></span>

<span data-ttu-id="ba9fd-108">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ba9fd-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="ba9fd-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ba9fd-109">Value</span></span> | <span data-ttu-id="ba9fd-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ba9fd-110">Description</span></span>                                                                            |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9fd-111">1</span><span class="sxs-lookup"><span data-stu-id="ba9fd-111">1</span></span>     | <span data-ttu-id="ba9fd-112">Всегда заносить в журнал ошибки во время вызова в процессе COM-сервера.</span><span class="sxs-lookup"><span data-stu-id="ba9fd-112">Always log failures during a call in the COM Server process.</span></span>                           |
| <span data-ttu-id="ba9fd-113">2</span><span class="sxs-lookup"><span data-stu-id="ba9fd-113">2</span></span>     | <span data-ttu-id="ba9fd-114">Не заносить в журнал сбои во время вызова в процессе COM-сервера.</span><span class="sxs-lookup"><span data-stu-id="ba9fd-114">Never log failures during a call in the COM Server process.</span></span> <span data-ttu-id="ba9fd-115">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ba9fd-115">This is the default value.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ba9fd-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ba9fd-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba9fd-117">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="ba9fd-117">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




