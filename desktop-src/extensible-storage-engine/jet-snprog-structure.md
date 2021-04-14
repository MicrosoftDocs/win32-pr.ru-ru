---
description: 'Дополнительные сведения: структура JET_SNPROG'
title: Структура JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 961e9cf264652924cfb1d870fa1a04aabc7fb61a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496953"
---
# <a name="jet_snprog-structure"></a><span data-ttu-id="9e73c-103">Структура JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="9e73c-103">JET_SNPROG Structure</span></span>


<span data-ttu-id="9e73c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9e73c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snprog-structure"></a><span data-ttu-id="9e73c-105">Структура JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="9e73c-105">JET_SNPROG Structure</span></span>

<span data-ttu-id="9e73c-106">Структура **JET_SNPROG** содержит сведения о ходе выполнения длительной операции.</span><span class="sxs-lookup"><span data-stu-id="9e73c-106">The **JET_SNPROG** structure contains information about the progress of a long-running operation.</span></span> <span data-ttu-id="9e73c-107">Когда вызывается функция обратного вызова для уведомления о состоянии операции, и операция все еще выполняется, последний параметр функции обратного вызова является указателем на структуру **JET_SNPROG** .</span><span class="sxs-lookup"><span data-stu-id="9e73c-107">When the callback function is called to notify the status of the operation and the operation is still in progress, the last parameter of the callback function is a pointer to a **JET_SNPROG** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a><span data-ttu-id="9e73c-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="9e73c-108">Members</span></span>

<span data-ttu-id="9e73c-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="9e73c-109">**cbStruct**</span></span>

<span data-ttu-id="9e73c-110">Размер структуры **JET_SNPROG** в байтах.</span><span class="sxs-lookup"><span data-stu-id="9e73c-110">The size of the **JET_SNPROG** structure, in bytes.</span></span> <span data-ttu-id="9e73c-111">Это значение подтверждает наличие следующих полей.</span><span class="sxs-lookup"><span data-stu-id="9e73c-111">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="9e73c-112">**кунитдоне**</span><span class="sxs-lookup"><span data-stu-id="9e73c-112">**cunitDone**</span></span>

<span data-ttu-id="9e73c-113">Количество рабочих единиц, уже выполненных во время выполнения длительной функции.</span><span class="sxs-lookup"><span data-stu-id="9e73c-113">The number of work units that are already completed during the long running function.</span></span>

<span data-ttu-id="9e73c-114">**куниттотал**</span><span class="sxs-lookup"><span data-stu-id="9e73c-114">**cunitTotal**</span></span>

<span data-ttu-id="9e73c-115">Количество единиц работы, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="9e73c-115">The number of work units that need to be completed.</span></span> <span data-ttu-id="9e73c-116">Это значение всегда должно быть больше или равно **кунитдоне**.</span><span class="sxs-lookup"><span data-stu-id="9e73c-116">This value should always be bigger than or equal to **cunitDone**.</span></span>

### <a name="requirements"></a><span data-ttu-id="9e73c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9e73c-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e73c-118"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9e73c-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9e73c-119">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9e73c-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e73c-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9e73c-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9e73c-121">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9e73c-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e73c-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9e73c-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9e73c-123">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9e73c-123">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

