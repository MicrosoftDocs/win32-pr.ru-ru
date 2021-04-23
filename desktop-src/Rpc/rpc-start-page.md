---
title: Удаленный вызов процедур
description: Удаленный вызов процедур (RPC) (Майкрософт) определяет мощную технологию для создания распределенных программ клиента/сервера.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC (см. раздел удаленный вызов процедур)
- RPC, начальная страница удаленного вызова процедуры
- RPC удаленного вызова процедур
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413477"
---
# <a name="remote-procedure-call"></a><span data-ttu-id="92c82-107">Удаленный вызов процедур</span><span class="sxs-lookup"><span data-stu-id="92c82-107">Remote Procedure Call</span></span>

## <a name="purpose"></a><span data-ttu-id="92c82-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="92c82-108">Purpose</span></span>

<span data-ttu-id="92c82-109">Удаленный вызов процедур (RPC) (Майкрософт) определяет мощную технологию для создания распределенных программ клиента/сервера.</span><span class="sxs-lookup"><span data-stu-id="92c82-109">Microsoft Remote Procedure Call (RPC) defines a powerful technology for creating distributed client/server programs.</span></span> <span data-ttu-id="92c82-110">Заглушки и библиотеки времени выполнения RPC управляют большинством процессов, связанных с сетевыми протоколами и связью.</span><span class="sxs-lookup"><span data-stu-id="92c82-110">The RPC run-time stubs and libraries manage most of the processes relating to network protocols and communication.</span></span> <span data-ttu-id="92c82-111">Это позволяет сосредоточиться на деталях приложения, а не на деталях сети.</span><span class="sxs-lookup"><span data-stu-id="92c82-111">This enables you to focus on the details of the application rather than the details of the network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="92c82-112">Где применимо</span><span class="sxs-lookup"><span data-stu-id="92c82-112">Where applicable</span></span>

<span data-ttu-id="92c82-113">RPC можно использовать во всех клиентских и серверных приложениях на основе операционных систем Windows.</span><span class="sxs-lookup"><span data-stu-id="92c82-113">RPC can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="92c82-114">Его также можно использовать для создания клиентских и серверных программ для разнородных сетевых сред, включающих такие операционные системы, как UNIX и Apple.</span><span class="sxs-lookup"><span data-stu-id="92c82-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="92c82-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="92c82-115">Developer audience</span></span>

<span data-ttu-id="92c82-116">RPC предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="92c82-116">RPC is designed to be used by C/C++ programmers.</span></span> <span data-ttu-id="92c82-117">Знакомство с язык MIDL (MIDL) и компилятором MIDL является обязательным.</span><span class="sxs-lookup"><span data-stu-id="92c82-117">Familiarity with the Microsoft Interface Definition Language (MIDL) and the MIDL compiler are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="92c82-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="92c82-118">Run-time requirements</span></span>

<span data-ttu-id="92c82-119">Библиотеки времени выполнения RPC входят в состав Windows.</span><span class="sxs-lookup"><span data-stu-id="92c82-119">The RPC run-time libraries are included with Windows.</span></span> <span data-ttu-id="92c82-120">Компоненты среды разработки RPC устанавливаются при установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="92c82-120">The components of the RPC development environment are installed when you install the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="92c82-121">Дополнительные сведения см. [в разделе Установка среды программирования RPC](installing-the-rpc-programming-environment.md).</span><span class="sxs-lookup"><span data-stu-id="92c82-121">For details, see [Installing the RPC Programming Environment](installing-the-rpc-programming-environment.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="92c82-122">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="92c82-122">In this section</span></span>



| <span data-ttu-id="92c82-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="92c82-123">Topic</span></span>                                                                           | <span data-ttu-id="92c82-124">Описание</span><span class="sxs-lookup"><span data-stu-id="92c82-124">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92c82-125">Лучшие методики программирования RPC</span><span class="sxs-lookup"><span data-stu-id="92c82-125">Best RPC Programming Practices</span></span>](best-rpc-programming-practices.md)<br/> | <span data-ttu-id="92c82-126">Рекомендации по методикам программирования RPC, которые помогают создавать лучшие приложения RPC.</span><span class="sxs-lookup"><span data-stu-id="92c82-126">Guidance on RPC programming practices that help create the best possible RPC applications.</span></span><br/>                            |
| [<span data-ttu-id="92c82-127">Обзор</span><span class="sxs-lookup"><span data-stu-id="92c82-127">Overview</span></span>](overviews.md)<br/>                                            | <span data-ttu-id="92c82-128">Общие сведения о внедрении RPC в клиентские и серверные приложения.</span><span class="sxs-lookup"><span data-stu-id="92c82-128">General information about incorporating RPC into your client/server applications.</span></span><br/>                                     |
| [<span data-ttu-id="92c82-129">Ссылки</span><span class="sxs-lookup"><span data-stu-id="92c82-129">Reference</span></span>](reference.md)<br/>                                           | <span data-ttu-id="92c82-130">Документация по типам, функциям и константам RPC.</span><span class="sxs-lookup"><span data-stu-id="92c82-130">Documentation of RPC types, functions, and constants.</span></span><br/>                                                                 |
| [<span data-ttu-id="92c82-131">Подсистема доставки оповещений RPC</span><span class="sxs-lookup"><span data-stu-id="92c82-131">RPC NDR Engine</span></span>](rpc-ndr-engine.md)<br/>                                 | <span data-ttu-id="92c82-132">Документация по модулю упаковки для компонентов RPC и DCOM, подсистема представления данных сети RPC.</span><span class="sxs-lookup"><span data-stu-id="92c82-132">Documentation of the marshaling engine for RPC and DCOM components, the RPC Network Data Representation (NDR) Engine.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="92c82-133">См. также</span><span class="sxs-lookup"><span data-stu-id="92c82-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92c82-134">Язык MIDL (MIDL)</span><span class="sxs-lookup"><span data-stu-id="92c82-134">Microsoft Interface Definition Language (MIDL)</span></span>](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

