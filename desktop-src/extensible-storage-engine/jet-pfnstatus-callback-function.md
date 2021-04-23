---
description: 'Дополнительные сведения: функция обратного вызова JET_PFNSTATUS'
title: Функция обратного вызова JET_PFNSTATUS
TOCTitle: JET_PFNSTATUS Callback Function
ms:assetid: 8b0cf5bf-a4ee-4d8f-8dd7-556c35cd269d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269326(v=EXCHG.10)
ms:contentKeyID: 32765616
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
ms.openlocfilehash: c5f3eb374580dc6bed752900434706b66c6623b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265536"
---
# <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="08a9f-103">Функция обратного вызова JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="08a9f-103">JET_PFNSTATUS Callback Function</span></span>


<span data-ttu-id="08a9f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="08a9f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pfnstatus-callback-function"></a><span data-ttu-id="08a9f-105">Функция обратного вызова JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="08a9f-105">JET_PFNSTATUS Callback Function</span></span>

<span data-ttu-id="08a9f-106">Функция обратного вызова **JET_PFNSTATUS** получает сведения о ходе выполнения длительных операций, таких как дефрагментация, операции резервного копирования или восстановления.</span><span class="sxs-lookup"><span data-stu-id="08a9f-106">The **JET_PFNSTATUS** callback function receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="08a9f-107">Во время таких операций ядро СУБД вызывает эту функцию обратного вызова, чтобы обеспечить обновление хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="08a9f-107">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

```cpp
    JET_ERR JET_API JET_PFNSTATUS(
                           JET_SESID  sesid,
                           JET_SNP snp,
                           JET_SNT snt,
                           void* pv
    );
```

### <a name="parameters"></a><span data-ttu-id="08a9f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08a9f-108">Parameters</span></span>

<span data-ttu-id="08a9f-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="08a9f-109">*sesid*</span></span>

<span data-ttu-id="08a9f-110">Сеанс типа [JET_SESID](./jet-sesid.md) , с которым была вызвана долго выполняющаяся функция.</span><span class="sxs-lookup"><span data-stu-id="08a9f-110">The session of type [JET_SESID](./jet-sesid.md) with which the long-running function was called.</span></span>

<span data-ttu-id="08a9f-111">*Network*</span><span class="sxs-lookup"><span data-stu-id="08a9f-111">*snp*</span></span>

<span data-ttu-id="08a9f-112">Тип операции, указанный в [JET_SNP](./jet-snp.md).</span><span class="sxs-lookup"><span data-stu-id="08a9f-112">The type of operation as specified in [JET_SNP](./jet-snp.md).</span></span> <span data-ttu-id="08a9f-113">К типам операций относятся исправление, сжатие, восстановление, резервное копирование, обновление, очистка и обновление формата записи.</span><span class="sxs-lookup"><span data-stu-id="08a9f-113">Types of operations include repair, compact, restore, backup, update, scrub, and update the record format.</span></span>

<span data-ttu-id="08a9f-114">*снт*</span><span class="sxs-lookup"><span data-stu-id="08a9f-114">*snt*</span></span>

<span data-ttu-id="08a9f-115">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="08a9f-115">The status of an operation.</span></span> <span data-ttu-id="08a9f-116">Типы состояния включают "начало", "выполняется", "завершение" или "сбой".</span><span class="sxs-lookup"><span data-stu-id="08a9f-116">Status types include beginning, in progress, completion, or failure.</span></span> <span data-ttu-id="08a9f-117">Состояние будет указано с помощью третьего параметра типа [JET_SNT](./jet-snt.md).</span><span class="sxs-lookup"><span data-stu-id="08a9f-117">The status will be specified with the third parameter of type [JET_SNT](./jet-snt.md).</span></span>

<span data-ttu-id="08a9f-118">*PV*</span><span class="sxs-lookup"><span data-stu-id="08a9f-118">*pv*</span></span>

<span data-ttu-id="08a9f-119">Необязательный указатель на структуру типа [JET_SNPROG](./jet-snprog-structure.md).</span><span class="sxs-lookup"><span data-stu-id="08a9f-119">An optional pointer to a structure of type [JET_SNPROG](./jet-snprog-structure.md).</span></span>

### <a name="return-value"></a><span data-ttu-id="08a9f-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08a9f-120">Return Value</span></span>

<span data-ttu-id="08a9f-121">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с помощью одного из [расширенных кодов ошибок подсистемы хранилища](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="08a9f-121">This function returns the [JET_ERR](./jet-err.md) datatype with one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="08a9f-122">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="08a9f-122">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<span data-ttu-id="08a9f-123">При успешном выполнении операция, выдала ответный вызов, может продолжать работу в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="08a9f-123">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="08a9f-124">В некоторых случаях обратный вызов может возвращать предупреждение, которое влияет на эту операцию.</span><span class="sxs-lookup"><span data-stu-id="08a9f-124">In some cases, the callback might return a warning that influences that operation.</span></span>

<span data-ttu-id="08a9f-125">В случае сбоя операция, выдала ответный вызов, может продолжаться обычным образом или не может завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="08a9f-125">On failure, the operation that issued the callback might proceed normally or might fail.</span></span>

### <a name="remarks"></a><span data-ttu-id="08a9f-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08a9f-126">Remarks</span></span>

<span data-ttu-id="08a9f-127">Эта функция обратного вызова будет использоваться в уведомлении о ходе выполнения, в которой структура будет указывать текущее состояние хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="08a9f-127">This callback function will be used in a progress notification in which the structure will indicate the current state of the progress.</span></span> <span data-ttu-id="08a9f-128">Обратите внимание, что функция обратного вызова может вызываться несколько раз для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="08a9f-128">Note that the callback function might be called multiple times for the progress of the operation.</span></span>

### <a name="requirements"></a><span data-ttu-id="08a9f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="08a9f-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08a9f-130"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="08a9f-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="08a9f-131">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="08a9f-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08a9f-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="08a9f-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="08a9f-133">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="08a9f-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08a9f-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="08a9f-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="08a9f-135">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="08a9f-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="08a9f-136">См. также:</span><span class="sxs-lookup"><span data-stu-id="08a9f-136">See Also</span></span>

[<span data-ttu-id="08a9f-137">Коды ошибок расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="08a9f-137">Extensible Storage Engine error codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="08a9f-138">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="08a9f-138">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="08a9f-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="08a9f-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="08a9f-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="08a9f-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="08a9f-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="08a9f-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="08a9f-142">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="08a9f-142">JET_SNT</span></span>](./jet-snt.md)
