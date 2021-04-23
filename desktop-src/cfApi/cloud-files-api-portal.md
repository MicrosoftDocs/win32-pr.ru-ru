---
description: API фильтра облака обеспечивает функциональность на границе между пользовательским режимом и файловой системой.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Облачные модули синхронизации
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2021
ms.locfileid: "105714074"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="360e1-103">Облачные модули синхронизации</span><span class="sxs-lookup"><span data-stu-id="360e1-103">Cloud Sync Engines</span></span>

<span data-ttu-id="360e1-104">См. также [пример зеркального отражения облака](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span><span class="sxs-lookup"><span data-stu-id="360e1-104">Also see [Cloud Mirror sample](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span></span>

<span data-ttu-id="360e1-105">Начиная с Windows 10 версии 1709, Windows предоставляет *API облачных файлов*.</span><span class="sxs-lookup"><span data-stu-id="360e1-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="360e1-106">Этот API состоит из нескольких собственных API Win32 и WinRT, которые являются формализацией поддержки для облачных механизмов синхронизации, и выполняет такие задачи, как создание файлов заполнителей и каталогов и управление ими.</span><span class="sxs-lookup"><span data-stu-id="360e1-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="360e1-107">Пользователи этого API обычно являются поставщиками синхронизации, а в некоторых экстентах — приложениями Windows.</span><span class="sxs-lookup"><span data-stu-id="360e1-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="360e1-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="360e1-108">In this section</span></span>

| <span data-ttu-id="360e1-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="360e1-109">Topic</span></span>                                                                | <span data-ttu-id="360e1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="360e1-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="360e1-111">Создание облачного модуля синхронизации, поддерживающего файлы заполнителей</span><span class="sxs-lookup"><span data-stu-id="360e1-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="360e1-112">Узнайте, как использовать API облачных файлов для создания облачного модуля синхронизации файлов, включающего файлы заполнителей и интеграцию с проводником файлов.</span><span class="sxs-lookup"><span data-stu-id="360e1-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="360e1-113">Справочник по фильтрам облака</span><span class="sxs-lookup"><span data-stu-id="360e1-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="360e1-114">API облачного фильтра — это собственный API Win32, который является частью более широкого API облачных файлов.</span><span class="sxs-lookup"><span data-stu-id="360e1-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="360e1-115">API фильтра облака обеспечивает функциональность на границе между пользовательским режимом и файловой системой.</span><span class="sxs-lookup"><span data-stu-id="360e1-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="360e1-116">Этот API обрабатывает создание и управление заполнителями файлов и каталогов.</span><span class="sxs-lookup"><span data-stu-id="360e1-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |

