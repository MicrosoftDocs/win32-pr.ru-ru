---
title: О сети Windows
description: Приложения могут использовать функции Внет для добавления и отмены сетевых подключений, а также для получения сведений о текущей конфигурации сети.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Внет сети Windows, описание
- Внет Внет, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068580"
---
# <a name="about-windows-networking"></a><span data-ttu-id="9a57f-105">О сети Windows</span><span class="sxs-lookup"><span data-stu-id="9a57f-105">About Windows Networking</span></span>

<span data-ttu-id="9a57f-106">Приложения могут использовать функции Внет для добавления и отмены сетевых подключений, а также для получения сведений о текущей конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="9a57f-106">Applications can use the WNet functions to add and cancel network connections and to retrieve information about the current configuration of the network.</span></span>

<span data-ttu-id="9a57f-107">На следующем рисунке показана структура типичной сети.</span><span class="sxs-lookup"><span data-stu-id="9a57f-107">The following figure shows the structure of a typical network.</span></span>

![Типичная структура сети](images/csnet-01.png)

<span data-ttu-id="9a57f-109">На предыдущем рисунке Иерархия для ресурсов сервера Windows NT Server/Windows 2000 представлена подробно как поставщик сети \# 1.</span><span class="sxs-lookup"><span data-stu-id="9a57f-109">In the preceding figure, the hierarchy for Windows NT Server/Windows 2000 Server resources is given in detail as Network provider \#1.</span></span> <span data-ttu-id="9a57f-110">Сетевые ресурсы других поставщиков имеют разные иерархические системы.</span><span class="sxs-lookup"><span data-stu-id="9a57f-110">Network resources from other providers have different hierarchical systems.</span></span> <span data-ttu-id="9a57f-111">Перед началом работы с сетью приложению не требуются сведения об иерархии.</span><span class="sxs-lookup"><span data-stu-id="9a57f-111">An application does not need information about the hierarchy before it begins to work with a network.</span></span> <span data-ttu-id="9a57f-112">Он может продолжать работу из корневого каталога сети (то есть самого верхнего ресурса контейнера) и получать сведения о ресурсах сети, так как эти сведения необходимы.</span><span class="sxs-lookup"><span data-stu-id="9a57f-112">It can proceed from the network root (that is, the topmost container resource) and retrieve information about the network's resources as the information is required.</span></span>

<span data-ttu-id="9a57f-113">Сетевые ресурсы, которые содержат другие ресурсы, называются *контейнерами*.</span><span class="sxs-lookup"><span data-stu-id="9a57f-113">Network resources that contain other resources are called *containers*.</span></span> <span data-ttu-id="9a57f-114">Ресурсы контейнера находятся в прямоугольниках на предыдущем рисунке.</span><span class="sxs-lookup"><span data-stu-id="9a57f-114">Container resources are in boxes in the preceding figure.</span></span>

<span data-ttu-id="9a57f-115">Ресурсы, которые не содержат другие ресурсы, называются *объектами*.</span><span class="sxs-lookup"><span data-stu-id="9a57f-115">Resources that do not contain other resources are called *objects*.</span></span> <span data-ttu-id="9a57f-116">На предыдущем рисунке SharePoint \# 1 и SharePoint \# 2 являются объектами.</span><span class="sxs-lookup"><span data-stu-id="9a57f-116">In the preceding figure, Sharepoint \#1 and Sharepoint \#2 are objects.</span></span> <span data-ttu-id="9a57f-117">*SharePoint* — это объект, доступный по сети.</span><span class="sxs-lookup"><span data-stu-id="9a57f-117">A *sharepoint* is an object that is accessible across the network.</span></span> <span data-ttu-id="9a57f-118">К примерам SharePoint относятся принтеры и общие каталоги.</span><span class="sxs-lookup"><span data-stu-id="9a57f-118">Examples of sharepoints include printers and shared directories.</span></span>

 

 




