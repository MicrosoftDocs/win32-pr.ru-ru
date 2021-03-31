---
description: Регистрация ошибок
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Регистрация ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805627"
---
# <a name="logging-errors"></a><span data-ttu-id="f68dc-103">Регистрация ошибок</span><span class="sxs-lookup"><span data-stu-id="f68dc-103">Logging Errors</span></span>

<span data-ttu-id="f68dc-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="f68dc-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f68dc-105">[Службы редактирования DirectShow](directshow-editing-services.md) предоставляют встроенный механизм ведения журнала ошибок, возникающих при загрузке, построении или визуализации проекта DES.</span><span class="sxs-lookup"><span data-stu-id="f68dc-105">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides a built-in mechanism for logging errors that occur when loading, constructing, or rendering a DES project.</span></span> <span data-ttu-id="f68dc-106">В этой статье представлен пример консольного приложения, которое загружает файл XML-проекта и пытается выполнить его визуализацию.</span><span class="sxs-lookup"><span data-stu-id="f68dc-106">This article presents a sample console application that loads an XML project file and attempts to render it.</span></span> <span data-ttu-id="f68dc-107">При возникновении ошибки приложение выводит сообщение об ошибке в окне консоли.</span><span class="sxs-lookup"><span data-stu-id="f68dc-107">If an error occurs, the application prints an error message in the console window.</span></span> <span data-ttu-id="f68dc-108">Пример кода, представленный в этой статье, основан на примере, заданном при [загрузке и предварительном просмотре проекта](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="f68dc-108">The sample code presented in this article builds on the example given in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

> [!Note]  
> <span data-ttu-id="f68dc-109">Приложению не требуется реализовывать ведение журнала ошибок.</span><span class="sxs-lookup"><span data-stu-id="f68dc-109">Your application is not required to implement error logging.</span></span> <span data-ttu-id="f68dc-110">DES не регистрирует ошибки, если вы явно не запрашиваете его.</span><span class="sxs-lookup"><span data-stu-id="f68dc-110">DES does not log errors unless you explicitly request it.</span></span>

 

<span data-ttu-id="f68dc-111">В этой статье предполагается, что вы знакомы с программированием клиента COM и моделью временной шкалы DES.</span><span class="sxs-lookup"><span data-stu-id="f68dc-111">This article assumes that you understand COM client programming and the DES timeline model.</span></span> <span data-ttu-id="f68dc-112">Кроме того, необходимо ознакомиться с основами программирования объектов COM.</span><span class="sxs-lookup"><span data-stu-id="f68dc-112">In addition, you need to understand the basics of COM object programming.</span></span> <span data-ttu-id="f68dc-113">Сведения о шкалах времени в DES см. [в разделе Модель временной шкалы](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="f68dc-113">For information about timelines in DES, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="f68dc-114">Эта статья состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="f68dc-114">This article contains the following sections.</span></span>

-   [<span data-ttu-id="f68dc-115">Общие сведения о ведении журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="f68dc-115">Overview of Error Logging</span></span>](overview-of-error-logging.md)
-   [<span data-ttu-id="f68dc-116">Создание класса ведения журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="f68dc-116">Creating an Error Logging Class</span></span>](creating-an-error-logging-class.md)
-   [<span data-ttu-id="f68dc-117">Реализация Иамеррорлог</span><span class="sxs-lookup"><span data-stu-id="f68dc-117">Implementing IAMErrorLog</span></span>](implementing-iamerrorlog.md)
-   [<span data-ttu-id="f68dc-118">Настройка журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="f68dc-118">Setting the Error Log</span></span>](setting-the-error-log.md)
-   [<span data-ttu-id="f68dc-119">Ведение журнала ошибок DES: пример кода</span><span class="sxs-lookup"><span data-stu-id="f68dc-119">DES Error Logging: Example Code</span></span>](des-error-logging--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="f68dc-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f68dc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f68dc-121">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="f68dc-121">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



