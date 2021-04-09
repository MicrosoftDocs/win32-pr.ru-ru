---
description: Расширяет приложения, написанные с помощью технологий на основе COM.
ms.assetid: b21a6b08-c17c-4fcc-bc60-39037bc9902f
title: COM+ (службы компонентов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b778c31957ddfe3f71db23b2f5be2a3ee681fde0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990543"
---
# <a name="com-component-services"></a><span data-ttu-id="8cc5a-103">COM+ (службы компонентов)</span><span class="sxs-lookup"><span data-stu-id="8cc5a-103">COM+ (Component Services)</span></span>

## <a name="purpose"></a><span data-ttu-id="8cc5a-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="8cc5a-104">Purpose</span></span>

<span data-ttu-id="8cc5a-105">COM+ — это эволюция модели COM и Microsoft Transaction Server (MTS).</span><span class="sxs-lookup"><span data-stu-id="8cc5a-105">COM+ is an evolution of Microsoft Component Object Model (COM) and Microsoft Transaction Server (MTS).</span></span> <span data-ttu-id="8cc5a-106">COM+ создает и расширяет приложения, написанные с помощью COM, MTS и других технологий на основе COM.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-106">COM+ builds on and extends applications written using COM, MTS, and other COM-based technologies.</span></span> <span data-ttu-id="8cc5a-107">COM+ обрабатывает многие задачи управления ресурсами, которые ранее приходилось программировать самостоятельно, например выделение потоков и безопасность.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-107">COM+ handles many of the resource management tasks that you previously had to program yourself, such as thread allocation and security.</span></span> <span data-ttu-id="8cc5a-108">COM+ также делает приложения более масштабируемыми, предоставляя пулы потоков, пулы объектов и JIT-активацию объектов.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-108">COM+ also makes your applications more scalable by providing thread pooling, object pooling, and just-in-time object activation.</span></span> <span data-ttu-id="8cc5a-109">COM+ также помогает защитить целостность данных, предоставляя поддержку транзакций, даже если транзакция охватывает несколько баз данных по сети.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-109">COM+ also helps protect the integrity of your data by providing transaction support, even if a transaction spans multiple databases over a network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8cc5a-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="8cc5a-110">Where applicable</span></span>

<span data-ttu-id="8cc5a-111">COM+ можно использовать для разработки критически важных распределенных приложений для Windows в масштабах предприятия.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-111">COM+ can be used to develop enterprise-wide, mission-critical, distributed applications for Windows.</span></span>

<span data-ttu-id="8cc5a-112">Если вы являетесь системным администратором, то будете устанавливать, развертывать и настраивать приложения COM+ и их компоненты.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-112">If you are a system administrator, you will be installing, deploying, and configuring COM+ applications and their components.</span></span> <span data-ttu-id="8cc5a-113">Если вы являетесь программистом приложения, вы будете писать компоненты и интегрировать их как приложения.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-113">If you are an application programmer, you will be writing components and integrating them as applications.</span></span> <span data-ttu-id="8cc5a-114">Если вы являетесь поставщиком инструментов, вы будете разрабатывать или изменять инструменты для работы в среде COM+.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-114">If you are a tools vendor, you will be developing or modifying tools to work in the COM+ environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8cc5a-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="8cc5a-115">Developer audience</span></span>

<span data-ttu-id="8cc5a-116">COM+ предназначен главным образом для Microsoft Visual C++ и разработчиков Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-116">COM+ is designed primarily for Microsoft Visual C++ and Microsoft Visual Basic developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8cc5a-117">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="8cc5a-117">Run-time requirements</span></span>

<span data-ttu-id="8cc5a-118">COM+ версии 1,5 входит в состав Windows, начиная с Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-118">COM+ version 1.5 is included in Windows starting with Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8cc5a-119">COM+ версии 1,0 входит в состав Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8cc5a-119">COM+ version 1.0 is included in Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8cc5a-120">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="8cc5a-120">In this section</span></span>

-   [<span data-ttu-id="8cc5a-121">Новые возможности COM+ 1,5</span><span class="sxs-lookup"><span data-stu-id="8cc5a-121">What's New in COM+ 1.5</span></span>](what-s-new-in-com--1-5.md)
-   [<span data-ttu-id="8cc5a-122">Обзор разработчиков COM+</span><span class="sxs-lookup"><span data-stu-id="8cc5a-122">COM+ Developers Overview</span></span>](com--developers-overview.md)
-   [<span data-ttu-id="8cc5a-123">Службы COM+</span><span class="sxs-lookup"><span data-stu-id="8cc5a-123">COM+ Services</span></span>](com--services.md)
-   [<span data-ttu-id="8cc5a-124">Общие задачи COM+</span><span class="sxs-lookup"><span data-stu-id="8cc5a-124">COM+ General Tasks</span></span>](com--general-tasks.md)
-   [<span data-ttu-id="8cc5a-125">Справочник по COM+</span><span class="sxs-lookup"><span data-stu-id="8cc5a-125">COM+ Reference</span></span>](com--reference.md)

## <a name="related-topics"></a><span data-ttu-id="8cc5a-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8cc5a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cc5a-127">COM</span><span class="sxs-lookup"><span data-stu-id="8cc5a-127">COM</span></span>](/windows/desktop/com/component-object-model--com--portal)
</dt> </dl>

 

 
