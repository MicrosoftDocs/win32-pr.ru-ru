---
title: Таскфолдер. Path, свойство
description: Для создания скриптов Возвращает путь к папке, в которой хранится папка.
ms.assetid: a0b28527-4875-4fe4-b2dd-08abbdc87ccc
keywords:
- Свойство пути планировщик задач
- Свойство Path планировщик задач, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, свойство Path
topic_type:
- apiref
api_name:
- TaskFolder.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6733c79d19bbb3d55531f05412a8c9263d76eb90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988353"
---
# <a name="taskfolderpath-property"></a><span data-ttu-id="a3a37-106">Таскфолдер. Path, свойство</span><span class="sxs-lookup"><span data-stu-id="a3a37-106">TaskFolder.Path property</span></span>

<span data-ttu-id="a3a37-107">Для создания скриптов Возвращает путь к папке, в которой хранится папка.</span><span class="sxs-lookup"><span data-stu-id="a3a37-107">For scripting, gets the path to where the folder is stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a37-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3a37-108">Syntax</span></span>


```VB
TaskFolder.Path As String
```



## <a name="property-value"></a><span data-ttu-id="a3a37-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a3a37-109">Property value</span></span>

<span data-ttu-id="a3a37-110">Путь к месту хранения папки.</span><span class="sxs-lookup"><span data-stu-id="a3a37-110">The path to where the folder is stored.</span></span> <span data-ttu-id="a3a37-111">Корневая папка задач указывается с помощью обратной косой черты ( \) .</span><span class="sxs-lookup"><span data-stu-id="a3a37-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="a3a37-112">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="a3a37-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3a37-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a3a37-113">Requirements</span></span>



| <span data-ttu-id="a3a37-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a3a37-114">Requirement</span></span> | <span data-ttu-id="a3a37-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a3a37-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a37-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3a37-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a37-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3a37-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a3a37-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3a37-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a37-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3a37-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3a37-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a3a37-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3a37-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a3a37-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a3a37-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a3a37-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3a37-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3a37-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3a37-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a3a37-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3a37-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a3a37-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





