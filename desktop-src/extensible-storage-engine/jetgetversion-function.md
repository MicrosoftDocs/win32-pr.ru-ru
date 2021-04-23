---
description: Дополнительные сведения о функции Жетжетверсион
title: Функция Жетжетверсион
TOCTitle: JetGetVersion Function
ms:assetid: f25c3639-ae2b-4357-9947-563ef3df72c6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294133(v=EXCHG.10)
ms:contentKeyID: 32765747
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetVersion
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 38128358d814ea85cf087c270a65a3fada976e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272397"
---
# <a name="jetgetversion-function"></a><span data-ttu-id="c40c5-103">Функция Жетжетверсион</span><span class="sxs-lookup"><span data-stu-id="c40c5-103">JetGetVersion Function</span></span>


<span data-ttu-id="c40c5-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c40c5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgetversion-function"></a><span data-ttu-id="c40c5-105">Функция Жетжетверсион</span><span class="sxs-lookup"><span data-stu-id="c40c5-105">JetGetVersion Function</span></span>

<span data-ttu-id="c40c5-106">Функция **жетжетверсион** извлекает версию ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c40c5-106">The **JetGetVersion** function retrieves the version of the database engine.</span></span>

```cpp
    JET_ERR JET_API JetGetVersion(
      __in          JET_SESID sesid,
      __out         unsigned long* pwVersion
    );
```

### <a name="parameters"></a><span data-ttu-id="c40c5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c40c5-107">Parameters</span></span>

<span data-ttu-id="c40c5-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="c40c5-108">*sesid*</span></span>

<span data-ttu-id="c40c5-109">Сеанс, используемый для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c40c5-109">The session to use for this call.</span></span>

<span data-ttu-id="c40c5-110">*пвверсион*</span><span class="sxs-lookup"><span data-stu-id="c40c5-110">*pwVersion*</span></span>

<span data-ttu-id="c40c5-111">Указатель на номер версии ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c40c5-111">A pointer to the version number of the database engine.</span></span>

### <a name="return-value"></a><span data-ttu-id="c40c5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c40c5-112">Return Value</span></span>

<span data-ttu-id="c40c5-113">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="c40c5-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c40c5-114">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c40c5-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c40c5-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c40c5-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="c40c5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c40c5-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c40c5-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c40c5-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c40c5-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c40c5-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c40c5-119">Если эта функция завершилась, извлекается версия ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="c40c5-119">If this function succeeds, the version of the database engine is retrieved.</span></span>

<span data-ttu-id="c40c5-120">Нет известных режимов сбоя.</span><span class="sxs-lookup"><span data-stu-id="c40c5-120">There are no known failure modes.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c40c5-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c40c5-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c40c5-122"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="c40c5-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c40c5-123">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c40c5-123">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c40c5-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c40c5-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c40c5-125">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c40c5-125">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c40c5-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c40c5-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c40c5-127">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="c40c5-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c40c5-128"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="c40c5-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c40c5-129">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c40c5-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c40c5-130"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="c40c5-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c40c5-131">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c40c5-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c40c5-132">См. также:</span><span class="sxs-lookup"><span data-stu-id="c40c5-132">See Also</span></span>

[<span data-ttu-id="c40c5-133">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="c40c5-133">Error Handling Parameters</span></span>](./error-handling-parameters.md)  
[<span data-ttu-id="c40c5-134">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="c40c5-134">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="c40c5-135">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c40c5-135">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c40c5-136">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c40c5-136">JET_SESID</span></span>](./jet-sesid.md)
