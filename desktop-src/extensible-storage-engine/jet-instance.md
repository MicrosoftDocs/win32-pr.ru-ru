---
description: 'Дополнительные сведения: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999059"
---
# <a name="jet_instance"></a><span data-ttu-id="bfcd6-103">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bfcd6-103">JET_INSTANCE</span></span>


<span data-ttu-id="bfcd6-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bfcd6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance"></a><span data-ttu-id="bfcd6-105">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bfcd6-105">JET_INSTANCE</span></span>

<span data-ttu-id="bfcd6-106">Тип данных **JET_INSTANCE** содержит обработчик для экземпляра базы данных, который используется для вызова API Jet.</span><span class="sxs-lookup"><span data-stu-id="bfcd6-106">The **JET_INSTANCE** data type contains a handle to the instance of the database to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a><span data-ttu-id="bfcd6-107">Типы данных</span><span class="sxs-lookup"><span data-stu-id="bfcd6-107">Data Types</span></span>

<span data-ttu-id="bfcd6-108">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="bfcd6-108">JET_INSTANCE</span></span>

<span data-ttu-id="bfcd6-109">Для указания недопустимого обработчика экземпляра можно использовать **значение NULL** или [JET_instanceNil](./invalid-handle-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="bfcd6-109">Either **NULL** or [JET_instanceNil](./invalid-handle-constants.md) can be used to indicate an invalid instance handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="bfcd6-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfcd6-110">Remarks</span></span>

<span data-ttu-id="bfcd6-111">Этот маркер получается при создании экземпляра базы данных путем вызова функций [жеткреатеинстанце](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [жетинит](./jetinit-function.md)или [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="bfcd6-111">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="bfcd6-112">**Windows XP:**  Явное использование экземпляров поддерживается только в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="bfcd6-112">**Windows XP:**  The explicit use of instances is only supported on Windows XP and later releases.</span></span>

<span data-ttu-id="bfcd6-113">**Windows 2000:**  Для каждого процесса поддерживается только один глобальный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="bfcd6-113">**Windows 2000:**  Only one global instance is supported per process.</span></span>

### <a name="requirements"></a><span data-ttu-id="bfcd6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bfcd6-114">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfcd6-115"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="bfcd6-115"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bfcd6-116">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bfcd6-116">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfcd6-117"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bfcd6-117"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bfcd6-118">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bfcd6-118">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfcd6-119"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bfcd6-119"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bfcd6-120">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bfcd6-120">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bfcd6-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="bfcd6-121">See Also</span></span>

[<span data-ttu-id="bfcd6-122">жеткреатеинстанце</span><span class="sxs-lookup"><span data-stu-id="bfcd6-122">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="bfcd6-123">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="bfcd6-123">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="bfcd6-124">жетинит</span><span class="sxs-lookup"><span data-stu-id="bfcd6-124">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="bfcd6-125">JetInit2</span><span class="sxs-lookup"><span data-stu-id="bfcd6-125">JetInit2</span></span>](./jetinit2-function.md)
