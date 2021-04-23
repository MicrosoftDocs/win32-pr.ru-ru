---
title: Об WER
description: Отчеты об ошибках Windows (WER) — это гибкая инфраструктура обратной связи на основе событий, предназначенная для сбора сведений о проблемах с оборудованием и программным обеспечением, которые Windows может обнаружить, сообщить о них в корпорацию Майкрософт и предоставить пользователям все доступные решения. Сведения об улучшениях в WER см. в статье новые возможности WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Отчеты об ошибках Windows отчетов об ошибках Windows, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330904"
---
# <a name="about-wer"></a><span data-ttu-id="ae38c-105">Об WER</span><span class="sxs-lookup"><span data-stu-id="ae38c-105">About WER</span></span>

<span data-ttu-id="ae38c-106">Отчеты об ошибках Windows (WER) — это гибкая инфраструктура обратной связи на основе событий, предназначенная для сбора сведений о проблемах с оборудованием и программным обеспечением, которые Windows может обнаружить, сообщить о них в корпорацию Майкрософт и предоставить пользователям все доступные решения.</span><span class="sxs-lookup"><span data-stu-id="ae38c-106">Windows Error Reporting (WER) is a flexible event-based feedback infrastructure designed to gather information about the hardware and software problems that Windows can detect, report the information to Microsoft, and provide users with any available solutions.</span></span> <span data-ttu-id="ae38c-107">Сведения об улучшениях в WER см. в статье [новые возможности WER](what-s-new-in-wer.md).</span><span class="sxs-lookup"><span data-stu-id="ae38c-107">For information about the improvements to WER, see [What's New in WER](what-s-new-in-wer.md).</span></span>

<span data-ttu-id="ae38c-108">Начиная с Windows Vista, Windows обеспечивает аварийное завершение, отсутствие ответа и отчеты об ошибках сбоев ядра по умолчанию, не требуя внесения изменений в приложение.</span><span class="sxs-lookup"><span data-stu-id="ae38c-108">Beginning with Windows Vista, Windows provides crash, no response, and kernel fault error reporting by default without requiring changes to your application.</span></span> <span data-ttu-id="ae38c-109">Вместо этого приложения используют API WER для создания отчетов об ошибках, связанных с конкретными приложениями, которые не связаны со сбоями, неответными сообщениями или сбоями ядра.</span><span class="sxs-lookup"><span data-stu-id="ae38c-109">Applications instead use the WER API to generate error reports for application-specific issues that are not related to crashes, non-responses, or kernel faults.</span></span>

<span data-ttu-id="ae38c-110">Для создания отчетов об ошибках, связанных с конкретным приложением, приложение должно создать краткое описание проблемы, используя несколько основных фрагментов информации, которые называются *параметрами отчета*.</span><span class="sxs-lookup"><span data-stu-id="ae38c-110">To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called *report parameters*.</span></span> <span data-ttu-id="ae38c-111">Параметры отчета включают такие сведения, как имя приложения, версия приложения, имя модуля, версия модуля и код ошибки.</span><span class="sxs-lookup"><span data-stu-id="ae38c-111">Report parameters include information such as the application name, application version, module name, module version, and error code.</span></span> <span data-ttu-id="ae38c-112">Сочетание этих параметров отчета описывает уникальную проблему.</span><span class="sxs-lookup"><span data-stu-id="ae38c-112">The combination of these report parameters describes a unique problem.</span></span>

<span data-ttu-id="ae38c-113">Когда программа WER проверяет наличие решения, она взаимодействует с сервером WER в корпорации Майкрософт, выдавая сначала запрос о том, что проблема уже известна.</span><span class="sxs-lookup"><span data-stu-id="ae38c-113">When WER checks for a solution, it communicates with the WER server at Microsoft by first asking if the problem is already known.</span></span> <span data-ttu-id="ae38c-114">Сервер отвечает одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="ae38c-114">The server responds in one of the following ways:</span></span>

-   <span data-ttu-id="ae38c-115">Если проблема известна и существует решение, сервер отправляет решение на клиентский компьютер, и WER отображает эти сведения пользователю.</span><span class="sxs-lookup"><span data-stu-id="ae38c-115">If the problem is known and there is a solution, the server sends the solution to the client computer and WER displays this information to the user.</span></span>
-   <span data-ttu-id="ae38c-116">При исследовании проблемы сервер может отправить ответ, указывающий на состояние.</span><span class="sxs-lookup"><span data-stu-id="ae38c-116">If the problem is being investigated, the server may send a response that indicates the status.</span></span> <span data-ttu-id="ae38c-117">Если разработчику требуются дополнительные сведения для решения проблемы, сервер запрашивает дополнительные сведения от WER и WER запрашивает у пользователя разрешение на отправку этих сведений.</span><span class="sxs-lookup"><span data-stu-id="ae38c-117">If the developer needs more information to solve the problem, the server requests additional information from WER and WER asks the user for permission to send this information.</span></span>
-   <span data-ttu-id="ae38c-118">Если проблема неизвестна, сервер создает проблему, с которой разработчик может исследовать и отправлять в WER ответ, указывающий состояние.</span><span class="sxs-lookup"><span data-stu-id="ae38c-118">If the problem is not known, the server creates an issue for a developer to investigate and sends WER a response that indicates the status.</span></span>

<span data-ttu-id="ae38c-119">При использовании этого процесса WER собирает дополнительные сведения, если это необходимо, или отправляет пользователю решение, если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="ae38c-119">Using this process, WER gathers more information if needed or sends a solution to the user when available.</span></span> <span data-ttu-id="ae38c-120">В Windows Vista пользователь может в любое время перейти к **отчетам о проблемах и решениям** , чтобы просмотреть доступные решения, проверить, доступны ли новые решения, или управлять другими отчетами и параметрами WER.</span><span class="sxs-lookup"><span data-stu-id="ae38c-120">On Windows Vista, the user can go to **Problem Reports and Solutions** at any time to view available solutions, check whether new solutions are available, or manage their other WER reports and settings.</span></span> <span data-ttu-id="ae38c-121">В Windows 7 **отчеты о проблемах и решения** теперь называются **центром действий**.</span><span class="sxs-lookup"><span data-stu-id="ae38c-121">On Windows 7, the **Problem Reports and Solutions** is now called the **Action Center**.</span></span> <span data-ttu-id="ae38c-122">Нажмите кнопку " **Пуск** " и введите "View" в окне **поиска программы и файлы** , а затем выберите **Просмотреть все отчеты о проблемах**, **Просмотреть журнал надежности** или **Просмотреть решения для проблем**.</span><span class="sxs-lookup"><span data-stu-id="ae38c-122">Click **Start** and enter "view" in **Search programs and files** and then select **View all problem reports**, **View reliability history**, or **View solutions to problems**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae38c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="ae38c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae38c-124">Отчеты об ошибках Windows</span><span class="sxs-lookup"><span data-stu-id="ae38c-124">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 




