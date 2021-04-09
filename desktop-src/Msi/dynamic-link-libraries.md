---
description: Пользовательское действие может вызвать функцию, определенную в библиотеке динамической компоновки (DLL), написанной на языке C или C++.
ms.assetid: 605c7b97-70bd-467a-9438-47b05d8b6b5d
title: Библиотеки Dynamic-Link (установщик Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f9ff0113d97d219220a4f42030c1563f16ce7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080919"
---
# <a name="dynamic-link-libraries-windows-installer"></a><span data-ttu-id="5b224-103">Библиотеки Dynamic-Link (установщик Windows)</span><span class="sxs-lookup"><span data-stu-id="5b224-103">Dynamic-Link Libraries (Windows Installer)</span></span>

<span data-ttu-id="5b224-104">Пользовательское действие может вызвать функцию, определенную в библиотеке динамической компоновки (DLL), написанной на языке C или C++.</span><span class="sxs-lookup"><span data-stu-id="5b224-104">A custom action can call a function defined in a dynamic-link library (DLL) written in C or C++.</span></span> <span data-ttu-id="5b224-105">Библиотека DLL может существовать как файл, установленный во время текущей установки, или как временный двоичный поток, исходящий из [двоичной таблицы](binary-table.md) базы данных установки.</span><span class="sxs-lookup"><span data-stu-id="5b224-105">The DLL can exist as a file installed during the current installation or as a temporary binary stream originating from the [Binary table](binary-table.md) of the installation database.</span></span>

<span data-ttu-id="5b224-106">Обратите внимание, что все вызываемые функции, включая пользовательские действия в библиотеках DLL, должны указывать \_ \_ соглашение о вызовах STDCALL.</span><span class="sxs-lookup"><span data-stu-id="5b224-106">Note that any called functions, including custom actions in DLLs, must specify the \_\_stdcall calling convention.</span></span> <span data-ttu-id="5b224-107">Например, для вызова CustomAction используется следующее.</span><span class="sxs-lookup"><span data-stu-id="5b224-107">For example, to call CustomAction use the following.</span></span>


```C++
#include <windows.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="5b224-108">Дополнительные сведения см. [в разделе доступ к текущему сеансу установщика из пользовательского действия](accessing-the-current-installer-session-from-inside-a-custom-action.md) .</span><span class="sxs-lookup"><span data-stu-id="5b224-108">For more information see, [Accessing the Current Installer Session from Inside a Custom Action](accessing-the-current-installer-session-from-inside-a-custom-action.md)</span></span>

<span data-ttu-id="5b224-109">Следующие типы настраиваемых действий вызывают библиотеку динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="5b224-109">The following types of custom actions call a dynamic-link library.</span></span>



| <span data-ttu-id="5b224-110">Тип настраиваемого действия</span><span class="sxs-lookup"><span data-stu-id="5b224-110">Custom action type</span></span>                                 | <span data-ttu-id="5b224-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5b224-111">Description</span></span>                               |
|----------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="5b224-112">Тип настраиваемого действия 1</span><span class="sxs-lookup"><span data-stu-id="5b224-112">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="5b224-113">DLL-файл, хранящийся в потоке двоичных таблиц.</span><span class="sxs-lookup"><span data-stu-id="5b224-113">DLL file stored in a Binary table stream.</span></span> |
| [<span data-ttu-id="5b224-114">Тип настраиваемого действия 17</span><span class="sxs-lookup"><span data-stu-id="5b224-114">Custom Action Type 17</span></span>](custom-action-type-17.md) | <span data-ttu-id="5b224-115">DLL-файл, установленный с продуктом.</span><span class="sxs-lookup"><span data-stu-id="5b224-115">DLL file installed with a product.</span></span>        |



 

> [!Note]  
> <span data-ttu-id="5b224-116">Чтобы использовать COM, необходимо вызвать [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) в настраиваемом действии.</span><span class="sxs-lookup"><span data-stu-id="5b224-116">To use COM you need to call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in the custom action.</span></span> <span data-ttu-id="5b224-117">Не завершайте работу, если обнаруживается, что поток уже инициализирован.</span><span class="sxs-lookup"><span data-stu-id="5b224-117">Do not quit if you find that the thread has already been initialized.</span></span> <span data-ttu-id="5b224-118">Например, поток инициализируется в установке на компьютере, но не в установке на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="5b224-118">For example, the thread is initialized in a per-machine installation but not in a per-user installation.</span></span>

 

<span data-ttu-id="5b224-119">См. [сводный список всех типов настраиваемых действий](summary-list-of-all-custom-action-types.md) для сводки всех типов настраиваемых действий и их кодирования в [таблицу CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="5b224-119">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a summary of all types of custom actions and how they are encoded into the [CustomAction table](customaction-table.md).</span></span>

 

 
