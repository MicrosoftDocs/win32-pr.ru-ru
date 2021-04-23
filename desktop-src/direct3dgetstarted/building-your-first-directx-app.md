---
title: Создание первого приложения Windows с помощью DirectX
description: В этом разделе описывается, зачем использовать модель C++ для разработки приложений для Магазина Windows, а также приводятся основные руководства и процедуры по началу работы с разработкой приложений DirectX.
ms.assetid: b632ba9c-1c30-4d21-ac79-7f2a193956fe
keywords:
- Приложение DirectX, начало работы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5e3afed57244789c0e3e06ab71ec39e581305c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772689"
---
# <a name="create-your-first-windows-app-using-directx"></a><span data-ttu-id="fb3ce-104">Создание первого приложения Windows с помощью DirectX</span><span class="sxs-lookup"><span data-stu-id="fb3ce-104">Create your first Windows app using DirectX</span></span>

<span data-ttu-id="fb3ce-105">Если вы знакомы с DirectX, вы можете разработать приложение DirectX с помощью машинного кода C++ и HLSL, чтобы воспользоваться всеми преимуществами графического оборудования.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-105">If you know DirectX, you can develop a DirectX app using native C++ and HLSL to take full advantage of graphics hardware.</span></span>

<span data-ttu-id="fb3ce-106">Используйте это основное руководство, чтобы приступить к разработке приложений DirectX, а затем воспользуйтесь руководством, чтобы продолжить изучение DirectX.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-106">Use this basic tutorial to get started with DirectX app development, then use the roadmap to continue exploring DirectX.</span></span>

## <a name="windows-desktop-app-with-c-and-directx"></a><span data-ttu-id="fb3ce-107">Классическое приложение для Windows на C++ и DirectX</span><span class="sxs-lookup"><span data-stu-id="fb3ce-107">Windows desktop app with C++ and DirectX</span></span>

<span data-ttu-id="fb3ce-108">Классическое приложение Windows с DirectX — это приложение, разработанное с помощью собственных API-интерфейсов C++ и DirectX.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-108">A Windows desktop app with DirectX is an app developed using native C++ and DirectX APIs.</span></span> <span data-ttu-id="fb3ce-109">Эта модель сложнее, чем приложение, написанное на управляемой платформе, но оно обеспечивает большую гибкость и доступ к системным ресурсам, особенно графическим устройствам.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-109">This model is more complex than an app written in a managed framework, but it provides greater flexibility and greater access to system resources especially graphics devices.</span></span> <span data-ttu-id="fb3ce-110">Итак, это хорошая модель для опытных разработчиков.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-110">So, it is a good model for the experienced developer.</span></span>

## <a name="why-develop-a-windows-app-with-directx"></a><span data-ttu-id="fb3ce-111">Зачем разрабатывать приложения для Windows с помощью DirectX?</span><span class="sxs-lookup"><span data-stu-id="fb3ce-111">Why develop a Windows app with DirectX?</span></span>

<span data-ttu-id="fb3ce-112">Ответ прост: вы хотите сделать игру с большим объемом графики или мультимедиа, а также использовать функции, поддерживаемые многими графическими устройствами.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-112">The answer is simple: you want to make a game that is graphics- or multimedia-intensive, and can use the features that many graphics devices support.</span></span> <span data-ttu-id="fb3ce-113">Это непросто, если вы не знакомы с разработкой игр или с Windows Development и C/C++, но есть хорошие новости: DirectX 11 — это самая простая и согласованная версия Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-113">This won't be easy if you are new to game development or to Windows development and C/C++, but there's some good news: DirectX 11 is the simplest and most cohesive version of Microsoft DirectX yet.</span></span> <span data-ttu-id="fb3ce-114">Это также самый мощный и функциональный компонент.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-114">It's also the most powerful and feature-rich.</span></span> <span data-ttu-id="fb3ce-115">Если ваша цель — разработка игровых игр и изучение наиболее сложных методов рендеринга, DirectX может предоставить вам возможность.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-115">If your goal is to master game development and learn the most advanced rendering techniques, then DirectX can provide the opportunity for you to do that.</span></span>

<span data-ttu-id="fb3ce-116">С другой стороны, планирование игры (или интерактивного приложения в режиме реального времени) является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-116">That said, planning your game (or interactive, real-time app) is essential.</span></span> <span data-ttu-id="fb3ce-117">Если вы не знакомы с разработкой игр и ваша игра не требует требований к графике, рекомендуется разработать ее с помощью .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-117">If you are new to game development, and your game doesn't have demanding graphics requirements, consider developing it with the .NET framework instead.</span></span> <span data-ttu-id="fb3ce-118">Кроме того, для платформ Windows доступны многие пакеты "промежуточного слоя" и разработки игр, и некоторые из них не нуждаются в значительных навыках программирования.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-118">Also, many "middleware" graphics and game development packages are available for Windows platforms, and some do not require significant programming skills.</span></span>

<span data-ttu-id="fb3ce-119">Если вы уверены или можете просто приступить к игре с высококачественной графикой (или с приложением со сложным графическим содержимым), прочтите статью.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-119">If you are confident, or simply have a dream of making a game with high-fidelity graphics (or an app with complex graphics content), then read on!</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fb3ce-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="fb3ce-120">In this section</span></span>



| <span data-ttu-id="fb3ce-121">Раздел</span><span class="sxs-lookup"><span data-stu-id="fb3ce-121">Topic</span></span>                                                                                                                     | <span data-ttu-id="fb3ce-122">Описание</span><span class="sxs-lookup"><span data-stu-id="fb3ce-122">Description</span></span>                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb3ce-123">Необходимые условия для разработки с помощью DirectX</span><span class="sxs-lookup"><span data-stu-id="fb3ce-123">Prerequisites for developing with DirectX</span></span>](pre-requisites-for-developing-a-tailored-c---with-directx-app.md)<br/> | <span data-ttu-id="fb3ce-124">Когда вы начинаете разрабатывать приложение для Windows с помощью DirectX, не забывайте о необходимых условиях на этой странице.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-124">When you start to develop a Windows app using DirectX, keep the prerequisites on this page in mind.</span></span> <span data-ttu-id="fb3ce-125">В их число входят те технологии, которые необходимо знать перед тем, как вы попытаетесь углубиться в.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-125">This includes the technologies you need to know before you dive in.</span></span><br/>                            |
| [<span data-ttu-id="fb3ce-126">Начало работы с DirectX для Windows</span><span class="sxs-lookup"><span data-stu-id="fb3ce-126">Get started with DirectX for Windows</span></span>](getting-started-with-a-directx-game.md)<br/>                                | <span data-ttu-id="fb3ce-127">Создание игры DirectX для Windows — это задача нового разработчика.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-127">Creating a DirectX game for Windows is a challenge for a new developer.</span></span> <span data-ttu-id="fb3ce-128">Здесь мы быстро рассмотрим связанные понятия и действия, которые необходимо предпринять, чтобы начать разработку игры с помощью DirectX и C++.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-128">Here we quickly review the concepts involved and the steps you must take to begin developing a game using DirectX and C++.</span></span><br/> |
| [<span data-ttu-id="fb3ce-129">Дорожная карта для классических приложений DirectX</span><span class="sxs-lookup"><span data-stu-id="fb3ce-129">Roadmap for Desktop DirectX apps</span></span>](roadmap-for-metro-style-apps-using-directx.md)<br/>                             | <span data-ttu-id="fb3ce-130">Ниже приведены основные ресурсы, которые помогут вам приступить к использованию DirectX и C++ для разработки настольных приложений с большим объемом графики, таких как игры.</span><span class="sxs-lookup"><span data-stu-id="fb3ce-130">Here are key resources to help you get started with using DirectX and C++ to develop graphics-intensive Desktop apps, like games.</span></span> <br/>                                                                 |



 

 

 





