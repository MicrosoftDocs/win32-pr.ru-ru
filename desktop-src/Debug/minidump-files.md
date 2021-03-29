---
description: Приложения могут создавать файлы минидампа пользовательского режима, которые содержат полезное подмножество данных, содержащихся в файле аварийного дампа.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Файлы минидампа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141026"
---
# <a name="minidump-files"></a><span data-ttu-id="74567-103">Файлы минидампа</span><span class="sxs-lookup"><span data-stu-id="74567-103">Minidump Files</span></span>

<span data-ttu-id="74567-104">Приложения могут создавать файлы минидампа пользовательского режима, которые содержат полезное подмножество данных, содержащихся в файле аварийного дампа.</span><span class="sxs-lookup"><span data-stu-id="74567-104">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="74567-105">Приложения могут быстро и эффективно создавать файлы минидампа.</span><span class="sxs-lookup"><span data-stu-id="74567-105">Applications can create minidump files very quickly and efficiently.</span></span> <span data-ttu-id="74567-106">Так как файлы минидампа невелики, их можно легко отправить через Интернет в службу технической поддержки для приложения.</span><span class="sxs-lookup"><span data-stu-id="74567-106">Because minidump files are small, they can be easily sent over the internet to technical support for the application.</span></span>

<span data-ttu-id="74567-107">Файл минидампа не содержит столько сведений, сколько полный файл дампа, но содержит достаточно сведений для выполнения основных операций отладки.</span><span class="sxs-lookup"><span data-stu-id="74567-107">A minidump file does not contain as much information as a full crash dump file, but it contains enough information to perform basic debugging operations.</span></span> <span data-ttu-id="74567-108">Для чтения файла минидампа необходимы двоичные файлы и файл символов, доступные для отладчика.</span><span class="sxs-lookup"><span data-stu-id="74567-108">To read a minidump file, you must have the binaries and symbol files available for the debugger.</span></span>

<span data-ttu-id="74567-109">Текущие версии Microsoft Office и Microsoft Windows создают файлы минидампа с целью анализа сбоев на компьютерах клиентов.</span><span class="sxs-lookup"><span data-stu-id="74567-109">Current versions of Microsoft Office and Microsoft Windows create minidump files for the purpose of analyzing failures on customers' computers.</span></span>

<span data-ttu-id="74567-110">Для файлов минидампа используются следующие функции DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="74567-110">The following DbgHelp functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="74567-111">**минидумпкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="74567-111">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="74567-112">**минидумпреаддумпстреам**</span><span class="sxs-lookup"><span data-stu-id="74567-112">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="74567-113">**минидумпвритедумп**</span><span class="sxs-lookup"><span data-stu-id="74567-113">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



