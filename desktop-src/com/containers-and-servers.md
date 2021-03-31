---
title: Контейнеры и серверы
description: Контейнеры и серверы
ms.assetid: 4918fa52-3598-4f4d-b2e7-7a47a37b216d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51b2cd46057c9216a1f9e29b93e1381a4d3062a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889140"
---
# <a name="containers-and-servers"></a><span data-ttu-id="09033-103">Контейнеры и серверы</span><span class="sxs-lookup"><span data-stu-id="09033-103">Containers and Servers</span></span>

<span data-ttu-id="09033-104">Приложения составного документа имеют два основных типа: контейнерные приложения и серверные приложения.</span><span class="sxs-lookup"><span data-stu-id="09033-104">Compound document applications are of two basic types: container applications and server applications.</span></span> <span data-ttu-id="09033-105">Приложения контейнера OLE предоставляют пользователям возможность создавать, изменять, сохранять и извлекать составные документы.</span><span class="sxs-lookup"><span data-stu-id="09033-105">OLE container applications provide users with the ability to create, edit, save, and retrieve compound documents.</span></span> <span data-ttu-id="09033-106">Приложения сервера OLE предоставляют пользователям средства для создания документов и других представлений данных, которые могут содержаться в виде ссылок или внедрений в приложениях контейнеров.</span><span class="sxs-lookup"><span data-stu-id="09033-106">OLE server applications provide users with the means to create documents and other data representations that can be contained as either links or embeddings in container applications.</span></span> <span data-ttu-id="09033-107">Приложение OLE может быть приложением-контейнером, серверным приложением или обоими.</span><span class="sxs-lookup"><span data-stu-id="09033-107">An OLE application can be a container application, a server application, or both.</span></span>

<span data-ttu-id="09033-108">Серверные приложения OLE также отличаются от того, реализуются ли они как *внутрипроцессный серверы* или *локальные серверы*.</span><span class="sxs-lookup"><span data-stu-id="09033-108">OLE server applications also differ in whether they are implemented as *in-process servers* or *local servers*.</span></span> <span data-ttu-id="09033-109">Внутрипроцессный сервер — это библиотека динамической компоновки (DLL), которая выполняется в пространстве процесса приложения контейнера.</span><span class="sxs-lookup"><span data-stu-id="09033-109">An in-process server is a dynamic link library (DLL) that runs in the container application's process space.</span></span> <span data-ttu-id="09033-110">Внутрипроцессный сервер можно запустить только в пределах приложения-контейнера.</span><span class="sxs-lookup"><span data-stu-id="09033-110">You can run an in-process server only from within the container application.</span></span>

> [!Note]  
> <span data-ttu-id="09033-111">Будущие выпуски OLE обеспечивают компоновку и внедрение между компьютерами, поэтому приложение-контейнер на одном компьютере сможет использовать объект составного документа, предоставляемый *удаленным сервером* , работающим на другом компьютере.</span><span class="sxs-lookup"><span data-stu-id="09033-111">Future releases of OLE will enable linking and embedding across computer boundaries, so that a container application on one computer will be able to use a compound document object provided by a *remote server* running on another computer.</span></span> <span data-ttu-id="09033-112">С точки зрения приложения-контейнера любое серверное приложение OLE, которое работает в собственном пространстве процесса, будь то тот же или удаленный компьютер, является *сервером вне процессâ*.</span><span class="sxs-lookup"><span data-stu-id="09033-112">From a container application's point of view, any OLE server application that runs in its own process space, whether on the same computer or a remote computer, is an *out-of-processÂ server*.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="09033-113">См. также</span><span class="sxs-lookup"><span data-stu-id="09033-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09033-114">Составные документы</span><span class="sxs-lookup"><span data-stu-id="09033-114">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="09033-115">Внутрипроцессный сервер</span><span class="sxs-lookup"><span data-stu-id="09033-115">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




