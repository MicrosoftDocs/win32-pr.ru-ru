---
description: Программа FhManagew.exe удаляет версии файлов, превышающие указанный возраст, из текущего назначенного целевого устройства истории файлов.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496185"
---
# <a name="fhmanagewexe"></a><span data-ttu-id="dfd0e-103">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="dfd0e-103">FhManagew.exe</span></span>

<span data-ttu-id="dfd0e-104">Программа FhManagew.exe удаляет версии файлов, превышающие указанный возраст, из текущего назначенного целевого устройства истории файлов.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-104">The FhManagew.exe program deletes file versions that exceed a specified age from the currently assigned File History target device.</span></span>

<span data-ttu-id="dfd0e-105">Эта программа доступна в Windows 8 и Windows Server 2012 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-105">This program is available in Windows 8 and Windows Server 2012 and later.</span></span>

<span data-ttu-id="dfd0e-106">Чтобы выполнить эту программу, перейдите в меню " **Пуск** ", выберите команду " **выполнить**" и введите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-106">To execute this program, go to the **Start** menu, click **Run**, and type the following command.</span></span>

<span data-ttu-id="dfd0e-107">**FhManagew.exe-** *возраст* очистки</span><span class="sxs-lookup"><span data-stu-id="dfd0e-107">**FhManagew.exe -cleanup** *age*</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dfd0e-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="dfd0e-108">Parameter</span></span></th>
<th><span data-ttu-id="dfd0e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="dfd0e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfd0e-110"><span id="age"></span><span id="AGE"></span><em>интервал</em></span><span class="sxs-lookup"><span data-stu-id="dfd0e-110"><span id="age"></span><span id="AGE"></span><em>age</em></span></span><br/></td>
<td><span data-ttu-id="dfd0e-111">Этот параметр указывает минимальный возраст (в днях) версий файлов, которые могут быть удалены.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-111">This parameter specifies the minimum age, in days, of file versions that can be deleted.</span></span> <span data-ttu-id="dfd0e-112">Версия файла удаляется, если выполняются оба следующих условия.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-112">A file version is deleted if both of the following conditions are true:</span></span><br/>
<ul>
<li><span data-ttu-id="dfd0e-113">Версия файла старше указанного срока.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-113">The file version is older than the specified age.</span></span></li>
<li><span data-ttu-id="dfd0e-114">Файл больше не включается в область защиты, или на целевом устройстве имеется более новая версия этого же файла.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-114">The file is no longer included in the protection scope, or there is a newer version of the same file on the target device.</span></span></li>
</ul>
<span data-ttu-id="dfd0e-115">Если параметр <em>Age</em> имеет значение 0, все версии файлов удаляются, за исключением последней версии каждого файла, который в данный момент находится в области защиты.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-115">If the <em>age</em> parameter is set to zero, all file versions are deleted, except for the newest version of each file that is currently present in the protection scope.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="dfd0e-116">Чтобы отключить все выходные данные этой программы, используйте параметр командной строки **-quiet** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-116">To suppress all output from this program, use the **-quiet** command-line option as follows.</span></span>

<span data-ttu-id="dfd0e-117">**FhManagew.exe-** *возраст* очистки **-тихий**</span><span class="sxs-lookup"><span data-stu-id="dfd0e-117">**FhManagew.exe -cleanup** *age* **-quiet**</span></span>

## <a name="examples"></a><span data-ttu-id="dfd0e-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="dfd0e-118">Examples</span></span>



| <span data-ttu-id="dfd0e-119">Пример</span><span class="sxs-lookup"><span data-stu-id="dfd0e-119">Example</span></span>                                                                                                                                                                                                      | <span data-ttu-id="dfd0e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="dfd0e-120">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd0e-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe — очистка 30**</span><span class="sxs-lookup"><span data-stu-id="dfd0e-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**</span></span><br/>                                 | <span data-ttu-id="dfd0e-122">Удалите все версии файлов старше одного месяца.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-122">Delete all file versions that are older than one month.</span></span><br/>                        |
| <span data-ttu-id="dfd0e-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe — очистка 365-quiet**</span><span class="sxs-lookup"><span data-stu-id="dfd0e-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**</span></span><br/> | <span data-ttu-id="dfd0e-124">Удалить все версии файлов старше одного года и отключить все выходные данные.</span><span class="sxs-lookup"><span data-stu-id="dfd0e-124">Delete all file versions that are older than one year and suppress all output.</span></span><br/> |



 

 

 




