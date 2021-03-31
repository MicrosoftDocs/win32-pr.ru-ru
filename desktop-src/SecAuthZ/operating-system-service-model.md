---
description: Приложение, работающее как обычный пользователь, взаимодействует со службой, работающей как система, с помощью удаленного вызова процедур (RPC).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Модель службы операционной системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998899"
---
# <a name="operating-system-service-model"></a><span data-ttu-id="38801-103">Модель службы операционной системы</span><span class="sxs-lookup"><span data-stu-id="38801-103">Operating System Service Model</span></span>

<span data-ttu-id="38801-104">В модели службы операционной системы приложение, работающее как обычный пользователь, взаимодействует со службой, работающей как **система** , с помощью [удаленного вызова процедур](/windows/desktop/Rpc/rpc-start-page) (RPC).</span><span class="sxs-lookup"><span data-stu-id="38801-104">In the operating system service model, an application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>

<span data-ttu-id="38801-105">Стандартное пользовательское приложение помечено в манифесте приложения с **RequestedExecutionLevel** **asInvoker**.</span><span class="sxs-lookup"><span data-stu-id="38801-105">The standard user application is marked in the application manifest with a **requestedExecutionLevel** of **asInvoker**.</span></span> <span data-ttu-id="38801-106">Для выполнения операции, требующей прав администратора, стандартное пользовательское приложение выполняет запрос к службе.</span><span class="sxs-lookup"><span data-stu-id="38801-106">To perform an operation that requires administrator privilege, the standard user application makes a request to the service.</span></span>

<span data-ttu-id="38801-107">Одним из способов использования модели службы операционной системы является Управление приложениями, которые могут повлиять на систему, такие как антивирусные и другие нежелательные программы и шпионские программы.</span><span class="sxs-lookup"><span data-stu-id="38801-107">One use for the operating system service model is to manage applications that could impact the system, such as antivirus or other unwanted software and spyware.</span></span> <span data-ttu-id="38801-108">Стандартное пользовательское приложение позволяет вошедшему в систему пользователю управлять некоторыми аспектами службы.</span><span class="sxs-lookup"><span data-stu-id="38801-108">The standard user application allows the logged on user to control some aspects of the service.</span></span> <span data-ttu-id="38801-109">Служба отвечает за определение того, какие операции она выполняет для стандартного пользовательского приложения.</span><span class="sxs-lookup"><span data-stu-id="38801-109">The service is responsible for determining which operations it performs for a standard user application.</span></span> <span data-ttu-id="38801-110">Например, антивирусная служба может позволить обычным пользователям запускать проверку системы, но она может не позволить обычным пользователям отключить проверку на вирусы в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="38801-110">For example, an antivirus service might allow a standard user to start a scan of the system, but it might not allow a standard user to disable real-time virus checking.</span></span>

<span data-ttu-id="38801-111">Основным преимуществом использования модели службы операционной системы является то, что запрос на повышение прав не требуется.</span><span class="sxs-lookup"><span data-stu-id="38801-111">A major benefit of using the operating system service model is that no elevation prompting is required.</span></span>

<span data-ttu-id="38801-112">Недостаток использования модели службы операционной системы состоит в том, что служба, работающая в системе, использует больше ресурсов, чем задача, а служба не может быть остановлена обычным пользователем.</span><span class="sxs-lookup"><span data-stu-id="38801-112">One drawback of using the operating system service model is that a service running on the system uses more resources than a task, and a service cannot be stopped by a standard user.</span></span> <span data-ttu-id="38801-113">Рассмотрите возможность использования [модели задач с повышенными правами](elevated-task-model.md) , если она достаточна.</span><span class="sxs-lookup"><span data-stu-id="38801-113">Consider using the [Elevated Task Model](elevated-task-model.md) if it suffices.</span></span>

<span data-ttu-id="38801-114">Чтобы реализовать модель службы операционной системы, Создайте клиентское приложение обычного пользователя и службу операционной системы.</span><span class="sxs-lookup"><span data-stu-id="38801-114">To implement the operating system service model, create a standard user client application and an operating system service.</span></span> <span data-ttu-id="38801-115">Установка службы в операционной системе во время установки продукта.</span><span class="sxs-lookup"><span data-stu-id="38801-115">Install the service in the operating system during product installation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38801-116">См. также</span><span class="sxs-lookup"><span data-stu-id="38801-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38801-117">Разработка приложений, требующих прав администратора</span><span class="sxs-lookup"><span data-stu-id="38801-117">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="38801-118">Модель брокера администратора</span><span class="sxs-lookup"><span data-stu-id="38801-118">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="38801-119">Модель COM-объектов администратора</span><span class="sxs-lookup"><span data-stu-id="38801-119">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="38801-120">Модель задач с повышенными правами</span><span class="sxs-lookup"><span data-stu-id="38801-120">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
