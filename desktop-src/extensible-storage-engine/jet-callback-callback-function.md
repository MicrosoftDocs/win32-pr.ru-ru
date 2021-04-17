---
description: 'Дополнительные сведения: функция обратного вызова JET_CALLBACK'
title: Функция обратного вызова JET_CALLBACK
TOCTitle: JET_CALLBACK Callback Function
ms:assetid: d15d4f84-8378-4b4b-9b8b-e89a56be5ead
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294098(v=EXCHG.10)
ms:contentKeyID: 32765713
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
ms.openlocfilehash: 5e6d26bd5e347757fce270d5f2c78ab471755c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673406"
---
# <a name="jet_callback-callback-function"></a><span data-ttu-id="f0a1a-103">Функция обратного вызова JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="f0a1a-103">JET_CALLBACK Callback Function</span></span>


<span data-ttu-id="f0a1a-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f0a1a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_callback-callback-function"></a><span data-ttu-id="f0a1a-105">Функция обратного вызова JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="f0a1a-105">JET_CALLBACK Callback Function</span></span>

<span data-ttu-id="f0a1a-106">Функция **JET_CALLBACK** — это функция обратного вызова с несколькими целями, используемая ядром СУБД для информирования приложения о событии, включающем в себя уведомления о дефрагментации и состоянии курсора в оперативном режиме.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-106">The **JET_CALLBACK** function is a multi-purpose callback function used by the database engine to inform the application of an event involving online defragmentation and cursor state notifications.</span></span>

<span data-ttu-id="f0a1a-107">В разделе [JET_CBTYP](./jet-cbtyp.md) конкретные параметры, используемые для параметров этой функции, так как эти параметры будут различаться в зависимости от параметра **JET_CBTYP** , выбранного для использования в параметре *кбтип* .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-107">See [JET_CBTYP](./jet-cbtyp.md) for specific settings to use for the parameters of this function, as these settings will differ depending upon the **JET_CBTYP** option that is selected for use in the *cbtyp* parameter.</span></span>

```cpp
    JET_ERR JET_API* JET_CALLBACK(
      [in]                 JET_SESID sesid,
      [in]                 JET_DBID dbid,
      [in]                 JET_TABLEID tableid,
      [in]                 JET_CBTYP cbtyp,
      [in, out]            void* pvArg1,
      [in, out]            void* pvArg2,
      [in]                 void* pvContext,
      [in]                 JET_API_PTR ulUnused
    );
```

### <a name="parameters"></a><span data-ttu-id="f0a1a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0a1a-108">Parameters</span></span>

<span data-ttu-id="f0a1a-109">*сесид*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-109">*sesid*</span></span>

<span data-ttu-id="f0a1a-110">Сеанс, для которого выполняется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-110">The session for which the callback is being made.</span></span>

<span data-ttu-id="f0a1a-111">*DBID*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-111">*dbid*</span></span>

<span data-ttu-id="f0a1a-112">База данных, для которой выполняется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-112">The database for which the callback is being made.</span></span>

<span data-ttu-id="f0a1a-113">*TableID*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-113">*tableid*</span></span>

<span data-ttu-id="f0a1a-114">Курсор, для которого выполняется обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-114">The cursor for which the callback is being made.</span></span>

<span data-ttu-id="f0a1a-115">*кбтип*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-115">*cbtyp*</span></span>

<span data-ttu-id="f0a1a-116">Точка в операции, в которой производится обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-116">The point in the operation at which the callback is being made.</span></span> <span data-ttu-id="f0a1a-117">Список значений и значения следующих параметров в каждом случае см. в разделе [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-117">See [JET_CBTYP](./jet-cbtyp.md) for a list of values and the meaning of the following parameters in each case.</span></span>

<span data-ttu-id="f0a1a-118">*pvArg1*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-118">*pvArg1*</span></span>

<span data-ttu-id="f0a1a-119">Параметр, используемый для взаимодействия с приложением с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-119">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="f0a1a-120">Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-120">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="f0a1a-121">*pvArg2*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-121">*pvArg2*</span></span>

<span data-ttu-id="f0a1a-122">Параметр, используемый для взаимодействия с приложением с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-122">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="f0a1a-123">Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-123">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="f0a1a-124">*пвконтекст*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-124">*pvContext*</span></span>

<span data-ttu-id="f0a1a-125">Параметр, используемый для взаимодействия с приложением с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-125">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="f0a1a-126">Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-126">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

<span data-ttu-id="f0a1a-127">*улунусед*</span><span class="sxs-lookup"><span data-stu-id="f0a1a-127">*ulUnused*</span></span>

<span data-ttu-id="f0a1a-128">Параметр, используемый для взаимодействия с приложением с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-128">A parameter used to communicate with the application using the callback.</span></span> <span data-ttu-id="f0a1a-129">Сведения об использовании этого параметра для каждого обратного вызова, поддерживаемого ядром СУБД, см. в разделе [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-129">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of this parameter for each callback supported by the database engine.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f0a1a-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0a1a-130">Return Value</span></span>

<span data-ttu-id="f0a1a-131">Функция возвращает один из [кодов ошибок расширенного подсистемы хранилища](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f0a1a-131">The function returns one of the [Extensible Storage Engine error codes](./extensible-storage-engine-error-codes.md).</span></span> <span data-ttu-id="f0a1a-132">Сведения о том, как вернуть эти коды HRESULT, см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="f0a1a-132">For information about how to return these codes as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="f0a1a-133">При успешном выполнении операция, выдала ответный вызов, может продолжать работу в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-133">On success, the operation that issued the callback can proceed normally.</span></span> <span data-ttu-id="f0a1a-134">В некоторых случаях обратный вызов может возвращать предупреждение, которое влияет на эту операцию.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-134">In some cases, the callback may return a warning that influences that operation.</span></span> <span data-ttu-id="f0a1a-135">Сведения об использовании этих предупреждений в операции см. в разделе [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-135">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of these warnings by the operation.</span></span>

<span data-ttu-id="f0a1a-136">В случае сбоя операция, выдала ответный вызов, может продолжаться обычным образом или не работать.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-136">On failure, the operation that issued the callback may proceed normally or may fail.</span></span> <span data-ttu-id="f0a1a-137">Сведения об использовании кода ошибки в операции см. в разделе [JET_CBTYP](./jet-cbtyp.md) .</span><span class="sxs-lookup"><span data-stu-id="f0a1a-137">See [JET_CBTYP](./jet-cbtyp.md) for information on the use of the error code by the operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f0a1a-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0a1a-138">Remarks</span></span>

<span data-ttu-id="f0a1a-139">Если обратный вызов передает приложению курсор, то важно помнить, что этот курсор намеренно ограничен небольшим набором функций, чтобы избежать рекурсии и других углинесс.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-139">If the callback passes a cursor to the application then it is important to know that this cursor is intentionally limited to a smaller set of functionality to avoid recursion and other ugliness.</span></span> <span data-ttu-id="f0a1a-140">Допустимы следующие операции:</span><span class="sxs-lookup"><span data-stu-id="f0a1a-140">The following operations are allowed:</span></span>

  - [<span data-ttu-id="f0a1a-141">жетдупкурсор</span><span class="sxs-lookup"><span data-stu-id="f0a1a-141">JetDupCursor</span></span>](./jetdupcursor-function.md)

  - [<span data-ttu-id="f0a1a-142">жетенумератеколумнс</span><span class="sxs-lookup"><span data-stu-id="f0a1a-142">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)

  - [<span data-ttu-id="f0a1a-143">жетжетбукмарк</span><span class="sxs-lookup"><span data-stu-id="f0a1a-143">JetGetBookmark</span></span>](./jetgetbookmark-function.md)

  - [<span data-ttu-id="f0a1a-144">жетжеткуррентиндекс</span><span class="sxs-lookup"><span data-stu-id="f0a1a-144">JetGetCurrentIndex</span></span>](./jetgetcurrentindex-function.md)

  - [<span data-ttu-id="f0a1a-145">жетжеткурсоринфо</span><span class="sxs-lookup"><span data-stu-id="f0a1a-145">JetGetCursorInfo</span></span>](./jetgetcursorinfo-function.md)

  - [<span data-ttu-id="f0a1a-146">жетжетлс</span><span class="sxs-lookup"><span data-stu-id="f0a1a-146">JetGetLS</span></span>](./jetgetls-function.md)

  - [<span data-ttu-id="f0a1a-147">жетжетрекордпоситион</span><span class="sxs-lookup"><span data-stu-id="f0a1a-147">JetGetRecordPosition</span></span>](./jetgetrecordposition-function.md)

  - [<span data-ttu-id="f0a1a-148">жетжетсекондариндексбукмарк</span><span class="sxs-lookup"><span data-stu-id="f0a1a-148">JetGetSecondaryIndexBookmark</span></span>](./jetgetsecondaryindexbookmark-function.md)

  - [<span data-ttu-id="f0a1a-149">жетжеттаблеколумнинфо</span><span class="sxs-lookup"><span data-stu-id="f0a1a-149">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)

  - [<span data-ttu-id="f0a1a-150">жетжеттаблеиндексинфо</span><span class="sxs-lookup"><span data-stu-id="f0a1a-150">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)

  - [<span data-ttu-id="f0a1a-151">жетжеттаблеинфо</span><span class="sxs-lookup"><span data-stu-id="f0a1a-151">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)

  - [<span data-ttu-id="f0a1a-152">жетрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="f0a1a-152">JetRegisterCallback</span></span>](./jetregistercallback-function.md)

  - [<span data-ttu-id="f0a1a-153">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="f0a1a-153">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)

  - [<span data-ttu-id="f0a1a-154">жетретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="f0a1a-154">JetRetrieveColumns</span></span>](./jetretrievecolumns-function.md)

  - [<span data-ttu-id="f0a1a-155">жетретриевекэй</span><span class="sxs-lookup"><span data-stu-id="f0a1a-155">JetRetrieveKey</span></span>](./jetretrievekey-function.md)

  - [<span data-ttu-id="f0a1a-156">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="f0a1a-156">JetSetColumn</span></span>](./jetsetcolumn-function.md)

  - [<span data-ttu-id="f0a1a-157">жетсетколумнс</span><span class="sxs-lookup"><span data-stu-id="f0a1a-157">JetSetColumns</span></span>](./jetsetcolumns-function.md)

  - [<span data-ttu-id="f0a1a-158">жетсетлс</span><span class="sxs-lookup"><span data-stu-id="f0a1a-158">JetSetLS</span></span>](./jetsetls-function.md)

  - [<span data-ttu-id="f0a1a-159">жетунрегистеркаллбакк</span><span class="sxs-lookup"><span data-stu-id="f0a1a-159">JetUnregisterCallback</span></span>](./jetunregistercallback-function.md)

<span data-ttu-id="f0a1a-160">При проектировании обратного вызова примите во внимание, что даже с этими ограничениями по-прежнему может произойти сбой обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-160">When you design your callback, take into account that even with these restrictions, it is still possible for the callback to fail.</span></span>

#### <a name="requirements"></a><span data-ttu-id="f0a1a-161">Требования</span><span class="sxs-lookup"><span data-stu-id="f0a1a-161">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0a1a-162"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="f0a1a-162"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f0a1a-163">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-163">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0a1a-164"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f0a1a-164"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f0a1a-165">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-165">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0a1a-166"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f0a1a-166"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f0a1a-167">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="f0a1a-167">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="f0a1a-168">См. также:</span><span class="sxs-lookup"><span data-stu-id="f0a1a-168">See Also</span></span>

[<span data-ttu-id="f0a1a-169">JET_API_PTR</span><span class="sxs-lookup"><span data-stu-id="f0a1a-169">JET_API_PTR</span></span>](./jet-api-ptr.md)  
[<span data-ttu-id="f0a1a-170">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="f0a1a-170">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="f0a1a-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="f0a1a-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="f0a1a-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="f0a1a-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="f0a1a-173">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="f0a1a-173">JET_CBTYP</span></span>](./jet-cbtyp.md)
