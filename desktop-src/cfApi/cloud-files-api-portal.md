---
description: API фильтра облака обеспечивает функциональность на границе между пользовательским режимом и файловой системой.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Облачные модули синхронизации
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549599"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="9b59d-103">Облачные модули синхронизации</span><span class="sxs-lookup"><span data-stu-id="9b59d-103">Cloud Sync Engines</span></span>

<span data-ttu-id="9b59d-104">См. также [пример зеркального отражения облака](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span><span class="sxs-lookup"><span data-stu-id="9b59d-104">Also see [Cloud Mirror sample](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span></span>

<span data-ttu-id="9b59d-105">Начиная с Windows 10 версии 1709, Windows предоставляет *API облачных файлов*.</span><span class="sxs-lookup"><span data-stu-id="9b59d-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="9b59d-106">Этот API состоит из нескольких собственных API Win32 и WinRT, которые являются формализацией поддержки для облачных механизмов синхронизации, и выполняет такие задачи, как создание файлов заполнителей и каталогов и управление ими.</span><span class="sxs-lookup"><span data-stu-id="9b59d-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="9b59d-107">Пользователи этого API обычно являются поставщиками синхронизации, а в некоторых экстентах — приложениями Windows.</span><span class="sxs-lookup"><span data-stu-id="9b59d-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b59d-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9b59d-108">In this section</span></span>

| <span data-ttu-id="9b59d-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="9b59d-109">Topic</span></span>                                                                | <span data-ttu-id="9b59d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9b59d-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b59d-111">Создание облачного модуля синхронизации, поддерживающего файлы заполнителей</span><span class="sxs-lookup"><span data-stu-id="9b59d-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="9b59d-112">Узнайте, как использовать API облачных файлов для создания облачного модуля синхронизации файлов, включающего файлы заполнителей и интеграцию с проводником файлов.</span><span class="sxs-lookup"><span data-stu-id="9b59d-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="9b59d-113">Справочник по фильтрам облака</span><span class="sxs-lookup"><span data-stu-id="9b59d-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="9b59d-114">API облачного фильтра — это собственный API Win32, который является частью более широкого API облачных файлов.</span><span class="sxs-lookup"><span data-stu-id="9b59d-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="9b59d-115">API фильтра облака обеспечивает функциональность на границе между пользовательским режимом и файловой системой.</span><span class="sxs-lookup"><span data-stu-id="9b59d-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="9b59d-116">Этот API обрабатывает создание и управление заполнителями файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="9b59d-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |