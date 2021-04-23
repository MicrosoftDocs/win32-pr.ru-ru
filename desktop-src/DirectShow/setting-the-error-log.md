---
description: Настройка журнала ошибок
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Настройка журнала ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac96fb90570408ca41be06656f7cf1704e9f48dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672934"
---
# <a name="setting-the-error-log"></a><span data-ttu-id="472ba-103">Настройка журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="472ba-103">Setting the Error Log</span></span>

<span data-ttu-id="472ba-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="472ba-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="472ba-105">После реализации класса ведения журнала ошибок создайте новый экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="472ba-105">After you implement the error logging class, create a new instance of the class.</span></span> <span data-ttu-id="472ba-106">Затем предоставьте [службам редактирования DirectShow](directshow-editing-services.md) указатель на него, вызвав метод [**иамсетеррорлог::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) на временной шкале.</span><span class="sxs-lookup"><span data-stu-id="472ba-106">Then, give [DirectShow Editing Services](directshow-editing-services.md) a pointer to it by calling the [**IAMSetErrorLog::put\_ErrorLog**](iamseterrorlog-put-errorlog.md) method on the timeline.</span></span> <span data-ttu-id="472ba-107">Запросите временную шкалу для интерфейса **иамсетеррорлог** .</span><span class="sxs-lookup"><span data-stu-id="472ba-107">Query the timeline for the **IAMSetErrorLog** interface.</span></span> <span data-ttu-id="472ba-108">Чтобы убедиться, что все ошибки зарегистрированы, следует вызвать этот метод перед загрузкой, сохранением или визуализацией временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="472ba-108">To ensure that all errors are logged, you should call this method before you load, save, or render the timeline.</span></span>


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



<span data-ttu-id="472ba-109">Ведение журнала ошибок не влияет на возвращаемые значения, которые вы получаете при вызове методов в приложении.</span><span class="sxs-lookup"><span data-stu-id="472ba-109">Error logging has no effect on the return values that you receive when you call methods in your application.</span></span> <span data-ttu-id="472ba-110">Регистрация ошибок дополняет, но не заменяет стандартные методы обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="472ba-110">Error logging complements but does not replace the usual error handling techniques.</span></span> <span data-ttu-id="472ba-111">Чтобы создать надежное приложение, всегда проверяйте значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="472ba-111">To create a robust application, always check HRESULT values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="472ba-112">См. также</span><span class="sxs-lookup"><span data-stu-id="472ba-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="472ba-113">Регистрация ошибок</span><span class="sxs-lookup"><span data-stu-id="472ba-113">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



