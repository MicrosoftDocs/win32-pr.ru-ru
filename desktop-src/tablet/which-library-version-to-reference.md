---
description: В этом разделе описываются различия между двоичными версиями библиотеки для планшетных ПК.
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: Версия библиотеки для ссылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692238"
---
# <a name="which-library-version-to-reference"></a><span data-ttu-id="ed6e8-103">Версия библиотеки для ссылки</span><span class="sxs-lookup"><span data-stu-id="ed6e8-103">Which Library Version to Reference</span></span>

<span data-ttu-id="ed6e8-104">В этом разделе описываются различия между двоичными версиями библиотеки для планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="ed6e8-104">This topic describes the differences between the Tablet PC library binary versions.</span></span>

## <a name="tablet-pc-library-versions"></a><span data-ttu-id="ed6e8-105">Версии библиотеки для планшетных ПК</span><span class="sxs-lookup"><span data-stu-id="ed6e8-105">Tablet PC Library Versions</span></span>

<span data-ttu-id="ed6e8-106">Двоичные файлы библиотеки Tablet PC (Microsoft.Ink.dll) были обновлены в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed6e8-106">The Tablet PC library binaries (Microsoft.Ink.dll) have been updated in Windows Vista.</span></span> <span data-ttu-id="ed6e8-107">Эти двоичные файлы называются "версия 6,0" для совместного инЦиде с версией Windows, в которой они освобождаются.</span><span class="sxs-lookup"><span data-stu-id="ed6e8-107">Theses binaries are referred to as "version 6.0" to co-incide with the version of Windows in which they are being released.</span></span>

<span data-ttu-id="ed6e8-108">Последний выпуск двоичных файлов, совместимых с Windows XP, называется "версия 1,7".</span><span class="sxs-lookup"><span data-stu-id="ed6e8-108">The most recent release of the binaries that are compatible with Windows XP is referred to as "version 1.7".</span></span>

<span data-ttu-id="ed6e8-109">Windows SDK можно установить на компьютерах Vista и XP, а Windows SDK включает обе версии Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="ed6e8-109">The Windows SDK can be installed on both Vista and XP machines, and the Windows SDK includes both versions of Microsoft.Ink.dll.</span></span>

<span data-ttu-id="ed6e8-110">Они устанавливаются в:</span><span class="sxs-lookup"><span data-stu-id="ed6e8-110">These are installed in:</span></span>

1. <span data-ttu-id="ed6e8-111">% ProgramFiles% \\ эталонных сборок \\ Microsoft \\ Tablet PC \\ v 1.7 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="ed6e8-111">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v1.7\\Microsoft.Ink.dll</span></span>

2. <span data-ttu-id="ed6e8-112">% ProgramFiles% \\ эталонных сборок \\ Microsoft \\ Tablet PC \\ v 6.0 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="ed6e8-112">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v6.0\\Microsoft.Ink.dll</span></span>

<span data-ttu-id="ed6e8-113">Двоичные файлы версии 6,0 совместимы только с Windows Vista, и приложения, написанные на них, должны выполняться только в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed6e8-113">The version 6.0 binaries are only compatible with Windows Vista, and applications written against them should only ever be run on Windows Vista.</span></span>

<span data-ttu-id="ed6e8-114">Приложение, написанное для двоичных файлов версии 1,7, должно выполняться без изменений при установке в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed6e8-114">An application written against the version 1.7 binaries should run without modification when installed on Windows Vista.</span></span>

 

 



