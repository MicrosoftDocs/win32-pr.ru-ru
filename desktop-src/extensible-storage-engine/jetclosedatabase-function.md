---
description: Дополнительные сведения о функции Жетклоседатабасе
title: Функция Жетклоседатабасе
TOCTitle: JetCloseDatabase Function
ms:assetid: e17a05dd-c30b-4e8f-8538-91a65e8052d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294123(v=EXCHG.10)
ms:contentKeyID: 32765737
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9088e0ebc3b4778d6968c999afc238e49fb2f48f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539986"
---
# <a name="jetclosedatabase-function"></a><span data-ttu-id="06f7f-103">Функция Жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="06f7f-103">JetCloseDatabase Function</span></span>


<span data-ttu-id="06f7f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="06f7f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosedatabase-function"></a><span data-ttu-id="06f7f-105">Функция Жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="06f7f-105">JetCloseDatabase Function</span></span>

<span data-ttu-id="06f7f-106">Функция **жетклоседатабасе** закрывает файл базы данных, который ранее был открыт с помощью [жетопендатабасе](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="06f7f-106">The **JetCloseDatabase** function closes a database file that was previously opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="06f7f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="06f7f-107">Parameters</span></span>

<span data-ttu-id="06f7f-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="06f7f-108">*sesid*</span></span>

<span data-ttu-id="06f7f-109">Контекст сеанса базы данных, который будет использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="06f7f-109">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="06f7f-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="06f7f-110">*dbid*</span></span>

<span data-ttu-id="06f7f-111">База данных, которая будет закрыта.</span><span class="sxs-lookup"><span data-stu-id="06f7f-111">The database to be closed.</span></span>

<span data-ttu-id="06f7f-112">*грбит*</span><span class="sxs-lookup"><span data-stu-id="06f7f-112">*grbit*</span></span>

<span data-ttu-id="06f7f-113">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="06f7f-113">Reserved for future use.</span></span>

### <a name="return-value"></a><span data-ttu-id="06f7f-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06f7f-114">Return Value</span></span>

<span data-ttu-id="06f7f-115">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="06f7f-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="06f7f-116">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="06f7f-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="06f7f-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="06f7f-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="06f7f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="06f7f-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06f7f-119">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="06f7f-119">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="06f7f-120">База данных не была открыта ранее.</span><span class="sxs-lookup"><span data-stu-id="06f7f-120">The database was not previously opened.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f7f-121">JET_errInvalidDatabaseId</span><span class="sxs-lookup"><span data-stu-id="06f7f-121">JET_errInvalidDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="06f7f-122">Параметр <em>DBID</em> не является допустимым идентификатором базы данных.</span><span class="sxs-lookup"><span data-stu-id="06f7f-122">The <em>dbid</em> parameter was not a valid database identifier.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f7f-123">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="06f7f-123">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="06f7f-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="06f7f-124">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="06f7f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="06f7f-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="06f7f-126"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="06f7f-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="06f7f-127">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="06f7f-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f7f-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="06f7f-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="06f7f-129">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="06f7f-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f7f-130"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="06f7f-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="06f7f-131">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="06f7f-131">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="06f7f-132"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="06f7f-132"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="06f7f-133">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="06f7f-133">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="06f7f-134"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="06f7f-134"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="06f7f-135">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="06f7f-135">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="06f7f-136">См. также:</span><span class="sxs-lookup"><span data-stu-id="06f7f-136">See Also</span></span>

[<span data-ttu-id="06f7f-137">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="06f7f-137">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="06f7f-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="06f7f-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="06f7f-139">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="06f7f-139">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="06f7f-140">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="06f7f-140">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="06f7f-141">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="06f7f-141">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="06f7f-142">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="06f7f-142">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="06f7f-143">жетопендатабасе</span><span class="sxs-lookup"><span data-stu-id="06f7f-143">JetOpenDatabase</span></span>](./jetopendatabase-function.md)
