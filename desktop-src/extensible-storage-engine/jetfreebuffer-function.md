---
description: Дополнительные сведения о функции Жетфрибуффер
title: Функция Жетфрибуффер
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702927"
---
# <a name="jetfreebuffer-function"></a><span data-ttu-id="4f8cb-103">Функция Жетфрибуффер</span><span class="sxs-lookup"><span data-stu-id="4f8cb-103">JetFreeBuffer Function</span></span>


<span data-ttu-id="4f8cb-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4f8cb-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetfreebuffer-function"></a><span data-ttu-id="4f8cb-105">Функция Жетфрибуффер</span><span class="sxs-lookup"><span data-stu-id="4f8cb-105">JetFreeBuffer Function</span></span>

<span data-ttu-id="4f8cb-106">Функция **жетфрибуффер** освобождает память, выделенную вызовом ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-106">The **JetFreeBuffer** function frees memory that was allocated by a database engine call.</span></span>

<span data-ttu-id="4f8cb-107">**Windows XP: жетфрибуффер** появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-107">**Windows XP:  JetFreeBuffer** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a><span data-ttu-id="4f8cb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f8cb-108">Parameters</span></span>

<span data-ttu-id="4f8cb-109">*пббуф*</span><span class="sxs-lookup"><span data-stu-id="4f8cb-109">*pbBuf*</span></span>

<span data-ttu-id="4f8cb-110">Указатель на область памяти, которая была ранее выделена вызовом ядра СУБД.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-110">Pointer to a region of memory that was previously allocated by a call to the database engine.</span></span> <span data-ttu-id="4f8cb-111">**Значение NULL** допустимо и будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-111">**NULL** is acceptable, and will be ignored.</span></span>

### <a name="return-value"></a><span data-ttu-id="4f8cb-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f8cb-112">Return Value</span></span>

<span data-ttu-id="4f8cb-113">Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-113">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="4f8cb-114">Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="4f8cb-114">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f8cb-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4f8cb-115">Return code</span></span></p></th>
<th><p><span data-ttu-id="4f8cb-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4f8cb-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f8cb-117">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="4f8cb-117">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="4f8cb-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-118">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="4f8cb-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f8cb-119">Remarks</span></span>

<span data-ttu-id="4f8cb-120">Не определено поведение для передачи памяти, которая не была выделена ядром СУБД в для *пббуф*.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-120">It is undefined behavior to pass memory that was not allocated by the database engine in to *pbBuf*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="4f8cb-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4f8cb-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f8cb-122"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="4f8cb-122"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8cb-123">Требуется Windows Vista или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-123">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f8cb-124"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4f8cb-124"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8cb-125">Требуется Windows Server 2008 или Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-125">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f8cb-126"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4f8cb-126"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8cb-127">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-127">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4f8cb-128"><strong>Библиотека</strong></span><span class="sxs-lookup"><span data-stu-id="4f8cb-128"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8cb-129">Используйте ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-129">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4f8cb-130"><strong>КОМПОНОВКИ</strong></span><span class="sxs-lookup"><span data-stu-id="4f8cb-130"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="4f8cb-131">Требуется ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="4f8cb-131">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="4f8cb-132">См. также:</span><span class="sxs-lookup"><span data-stu-id="4f8cb-132">See Also</span></span>

[<span data-ttu-id="4f8cb-133">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="4f8cb-133">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="4f8cb-134">жетжетинстанцеинфо</span><span class="sxs-lookup"><span data-stu-id="4f8cb-134">JetGetInstanceInfo</span></span>](./jetgetinstanceinfo-function.md)
