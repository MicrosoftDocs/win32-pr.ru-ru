---
description: Дополнительные сведения о функции Жетсеткурсорфилтер
title: Функция Жетсеткурсорфилтер
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad589fecb190ad0f0676325b78adc7c96028a3fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144227"
---
# <a name="jetsetcursorfilter-function"></a><span data-ttu-id="a2dd7-103">Функция Жетсеткурсорфилтер</span><span class="sxs-lookup"><span data-stu-id="a2dd7-103">JetSetCursorFilter Function</span></span>


<span data-ttu-id="a2dd7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a2dd7-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="a2dd7-105">Функция **жетсеткурсорфилтер** задает массив простых фильтров для функции [жетмове](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="a2dd7-105">The **JetSetCursorFilter** function sets an array of simple filters for the [JetMove](./jetmove-function.md) function.</span></span>

<span data-ttu-id="a2dd7-106">Функция **жетсеткурсорфилтер** была введена в операционной системе Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-106">The **JetSetCursorFilter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="a2dd7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2dd7-107">Parameters</span></span>

<span data-ttu-id="a2dd7-108">*сесид*</span><span class="sxs-lookup"><span data-stu-id="a2dd7-108">*sesid*</span></span>

<span data-ttu-id="a2dd7-109">Контекст сеанса базы данных, используемый для вызова API.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="a2dd7-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="a2dd7-110">*tableid*</span></span>

<span data-ttu-id="a2dd7-111">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-111">The cursor to position.</span></span>

<span data-ttu-id="a2dd7-112">*ргфилтерс*</span><span class="sxs-lookup"><span data-stu-id="a2dd7-112">*rgFilters*</span></span>

<span data-ttu-id="a2dd7-113">Простые фильтры записей.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-113">The simple record filters.</span></span>

<span data-ttu-id="a2dd7-114">*кфилтерс*</span><span class="sxs-lookup"><span data-stu-id="a2dd7-114">*cFilters*</span></span>

<span data-ttu-id="a2dd7-115">Число фильтров.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-115">The number of filters.</span></span>

<span data-ttu-id="a2dd7-116">*грбит*</span><span class="sxs-lookup"><span data-stu-id="a2dd7-116">*grbit*</span></span>

<span data-ttu-id="a2dd7-117">Группа битов, указывающая ноль или более параметров перемещения, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-117">A group of bits that specifies zero or more of the move options listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2dd7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a2dd7-118">Value</span></span></p></th>
<th><p><span data-ttu-id="a2dd7-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a2dd7-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2dd7-120">Нет</span><span class="sxs-lookup"><span data-stu-id="a2dd7-120">None</span></span></p></td>
<td><p><span data-ttu-id="a2dd7-121">Параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-121">Default option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="a2dd7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2dd7-122">Return value</span></span>

<span data-ttu-id="a2dd7-123">Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-123">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="a2dd7-124">Дополнительные сведения о возможных ошибках ESE см. в разделе [Расширенные ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a2dd7-124">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2dd7-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a2dd7-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="a2dd7-126">Описание</span><span class="sxs-lookup"><span data-stu-id="a2dd7-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2dd7-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="a2dd7-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="a2dd7-128">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-128">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="a2dd7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a2dd7-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2dd7-130"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="a2dd7-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="a2dd7-131">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-131">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2dd7-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="a2dd7-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="a2dd7-133">Требуется Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-133">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2dd7-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="a2dd7-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="a2dd7-135">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2dd7-136"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="a2dd7-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="a2dd7-137">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2dd7-138"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="a2dd7-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="a2dd7-139">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="a2dd7-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="a2dd7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2dd7-140">See also</span></span>

[<span data-ttu-id="a2dd7-141">жетмове</span><span class="sxs-lookup"><span data-stu-id="a2dd7-141">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="a2dd7-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="a2dd7-142">JET_ERR</span></span>](./jet-err.md)
