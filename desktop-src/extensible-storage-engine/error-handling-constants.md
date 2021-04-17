---
description: 'Дополнительные сведения: обработка ошибок констант'
title: Константы обработки ошибок
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab59a8e0c721558e5c056d25798c5d1273bd86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703239"
---
# <a name="error-handling-constants"></a><span data-ttu-id="558c7-103">Константы обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="558c7-103">Error Handling Constants</span></span>


<span data-ttu-id="558c7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="558c7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-constants"></a><span data-ttu-id="558c7-105">Константы обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="558c7-105">Error Handling Constants</span></span>

<span data-ttu-id="558c7-106">Для задания диапазона [JET_paramExceptionAction](./error-handling-parameters.md) системных параметров используются следующие константы.</span><span class="sxs-lookup"><span data-stu-id="558c7-106">The following constants are used to set the range for the [JET_paramExceptionAction](./error-handling-parameters.md) system parameters.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="558c7-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="558c7-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="558c7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="558c7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="558c7-109">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="558c7-109">JET_ExceptionMsgBox</span></span><br />
<span data-ttu-id="558c7-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="558c7-110">0x0001</span></span></p></td>
<td><p><span data-ttu-id="558c7-111">Отображает окно сообщения при возникновении исключения.</span><span class="sxs-lookup"><span data-stu-id="558c7-111">Displays a message box when an exception occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="558c7-112">JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="558c7-112">JET_ExceptionNone</span></span><br />
<span data-ttu-id="558c7-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="558c7-113">0x0002</span></span></p></td>
<td><p><span data-ttu-id="558c7-114">Не выполняет никаких действий при возникновении исключения.</span><span class="sxs-lookup"><span data-stu-id="558c7-114">Does nothing when an exception occurs.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="558c7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="558c7-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="558c7-116"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="558c7-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="558c7-117">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="558c7-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="558c7-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="558c7-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="558c7-119">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="558c7-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="558c7-120"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="558c7-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="558c7-121">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="558c7-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="558c7-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="558c7-122">See Also</span></span>

[<span data-ttu-id="558c7-123">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="558c7-123">Error Handling Parameters</span></span>](./error-handling-parameters.md)
