---
description: Новые Low-Level двоичные файлы
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: Новые Low-Level двоичные файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4640d31b115dc85ecde9f9423997468ddc8456
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088072"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="dbf09-103">Новые Low-Level двоичные файлы</span><span class="sxs-lookup"><span data-stu-id="dbf09-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="dbf09-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="dbf09-104">Affected Platforms</span></span>

<span data-ttu-id="dbf09-105">**Клиенты** — Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbf09-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="dbf09-106">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbf09-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="dbf09-107">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="dbf09-107">Feature Impact</span></span>

<span data-ttu-id="dbf09-108">**Серьезность** — средний</span><span class="sxs-lookup"><span data-stu-id="dbf09-108">**Severity** - Medium</span></span>  
<span data-ttu-id="dbf09-109">**Частота** — высокая</span><span class="sxs-lookup"><span data-stu-id="dbf09-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="dbf09-110">Описание</span><span class="sxs-lookup"><span data-stu-id="dbf09-110">Description</span></span>

<span data-ttu-id="dbf09-111">Для повышения эффективности внутреннего проектирования и улучшения основ для будущей работы мы переходили некоторые функции в новые двоичные файлы нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="dbf09-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="dbf09-112">Такой Рефакторинг позволяет будущим установкам Windows предоставлять подмножества функциональных возможностей для сокращения контактной зоны (требования к диску и памяти, Обслуживание и поверхность атак).</span><span class="sxs-lookup"><span data-stu-id="dbf09-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="dbf09-113">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="dbf09-113">Manifestation of Impact</span></span>

<span data-ttu-id="dbf09-114">В качестве примера функциональных возможностей, перемещенных в двоичные файлы нижнего уровня, kernelbase.dll получает функции kernel32.dll и advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="dbf09-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="dbf09-115">Это означает, что существующий двоичный файл теперь перенаправляет вызовы к новому двоичному файлу, вместо того чтобы обрабатывать их напрямую; Пересылка может быть статической (таблица экспорта показывает перенаправление) или во время выполнения (библиотека DLL содержит подпрограмму-заглушку, которая вызывает новый двоичный файл).</span><span class="sxs-lookup"><span data-stu-id="dbf09-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="dbf09-116">Это повлияет на низкоуровневые приложения, такие как приложения безопасности и резервного копирования, зависящие от внутренних интерфейсов API и смещений.</span><span class="sxs-lookup"><span data-stu-id="dbf09-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="dbf09-117">Решение</span><span class="sxs-lookup"><span data-stu-id="dbf09-117">Solution</span></span>

<span data-ttu-id="dbf09-118">Единственное влияние на код, который делает предположения при попытке взглянуть на kernel32.dll или advapi32.dllную таблицу экспорта в памяти, например, может делать антивирусное приложение.</span><span class="sxs-lookup"><span data-stu-id="dbf09-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="dbf09-119">Используйте опубликованные API, а не сведения о их реализации.</span><span class="sxs-lookup"><span data-stu-id="dbf09-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="dbf09-120">Это лишь один пример реализации для интерфейса API.</span><span class="sxs-lookup"><span data-stu-id="dbf09-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



