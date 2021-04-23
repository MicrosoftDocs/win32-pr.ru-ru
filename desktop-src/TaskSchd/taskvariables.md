---
title: Объект Тасквариаблес
description: Объект скрипта, который определяет переменные задачи, которые могут передаваться в качестве параметров обработчикам задач и внешним исполняемым файлам, запускаемым задачами.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- планировщик задач объекта Тасквариаблес
- Планировщик задач объекта Тасквариаблес, описание
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492243"
---
# <a name="taskvariables-object"></a><span data-ttu-id="c2660-105">Объект Тасквариаблес</span><span class="sxs-lookup"><span data-stu-id="c2660-105">TaskVariables object</span></span>

<span data-ttu-id="c2660-106">Объект скрипта, который определяет переменные задачи, которые могут передаваться в качестве параметров обработчикам задач и внешним исполняемым файлам, запускаемым задачами.</span><span class="sxs-lookup"><span data-stu-id="c2660-106">Scripting object that defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.</span></span>

## <a name="members"></a><span data-ttu-id="c2660-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="c2660-107">Members</span></span>

<span data-ttu-id="c2660-108">Объект **тасквариаблес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c2660-108">The **TaskVariables** object has these types of members:</span></span>

-   [<span data-ttu-id="c2660-109">Методы</span><span class="sxs-lookup"><span data-stu-id="c2660-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c2660-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c2660-110">Methods</span></span>

<span data-ttu-id="c2660-111">Объект **тасквариаблес** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="c2660-111">The **TaskVariables** object has these methods.</span></span>



| <span data-ttu-id="c2660-112">Метод</span><span class="sxs-lookup"><span data-stu-id="c2660-112">Method</span></span>                                         | <span data-ttu-id="c2660-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c2660-113">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2660-114">**GetContext**</span><span class="sxs-lookup"><span data-stu-id="c2660-114">**GetContext**</span></span>](taskvariables-getcontext.md) | <span data-ttu-id="c2660-115">Используется для совместного использования контекста разными шагами и задачами, которые находятся в одном и том же экземпляре задания.</span><span class="sxs-lookup"><span data-stu-id="c2660-115">Used to share the context between different steps and tasks that are in the same job instance.</span></span><br/> |
| [<span data-ttu-id="c2660-116">**GetInput**</span><span class="sxs-lookup"><span data-stu-id="c2660-116">**GetInput**</span></span>](taskvariables-getinput.md)     | <span data-ttu-id="c2660-117">Возвращает входные переменные для задачи.</span><span class="sxs-lookup"><span data-stu-id="c2660-117">Gets the input variables for a task.</span></span><br/>                                                           |
| [<span data-ttu-id="c2660-118">**сетаутпут**</span><span class="sxs-lookup"><span data-stu-id="c2660-118">**SetOutput**</span></span>](taskvariables-setoutput.md)   | <span data-ttu-id="c2660-119">Задает выходные переменные для задачи.</span><span class="sxs-lookup"><span data-stu-id="c2660-119">Sets the output variables for a task.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="c2660-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c2660-120">Requirements</span></span>



| <span data-ttu-id="c2660-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c2660-121">Requirement</span></span> | <span data-ttu-id="c2660-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c2660-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2660-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2660-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c2660-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2660-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c2660-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2660-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c2660-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2660-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2660-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c2660-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="c2660-128"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c2660-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c2660-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c2660-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2660-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2660-130"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





