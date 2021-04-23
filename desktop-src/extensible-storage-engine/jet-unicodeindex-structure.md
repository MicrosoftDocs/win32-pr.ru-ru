---
description: 'Дополнительные сведения: структура JET_UNICODEINDEX'
title: Структура JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
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
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104424546"
---
# <a name="jet_unicodeindex-structure"></a><span data-ttu-id="59c46-103">Структура JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="59c46-103">JET_UNICODEINDEX Structure</span></span>


<span data-ttu-id="59c46-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="59c46-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_unicodeindex-structure"></a><span data-ttu-id="59c46-105">Структура JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="59c46-105">JET_UNICODEINDEX Structure</span></span>

<span data-ttu-id="59c46-106">Структура **JET_UNICODEINDEX** настроена для нормализации данных в Юникоде при создании индекса на основе столбца в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="59c46-106">The **JET_UNICODEINDEX** structure customizes how Unicode data gets normalized when an index is created over a Unicode column.</span></span>

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a><span data-ttu-id="59c46-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="59c46-107">Members</span></span>

<span data-ttu-id="59c46-108">**lcid**</span><span class="sxs-lookup"><span data-stu-id="59c46-108">**lcid**</span></span>

<span data-ttu-id="59c46-109">КОД локали, используемый при нормализации данных.</span><span class="sxs-lookup"><span data-stu-id="59c46-109">The Locale ID to use when normalizing the data.</span></span> <span data-ttu-id="59c46-110">Любой языковой стандарт может использоваться при условии, что на компьютере установлен соответствующий языковой пакет.</span><span class="sxs-lookup"><span data-stu-id="59c46-110">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="59c46-111">Единственное исключение заключается в том, что независимый от языка языковой стандарт (LCID 0) является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="59c46-111">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="59c46-112">**dwMapFlags**</span><span class="sxs-lookup"><span data-stu-id="59c46-112">**dwMapFlags**</span></span>

<span data-ttu-id="59c46-113">Эти флаги передаются в [LCMapString завершилось ошибкой](/windows/win32/api/winnls/nf-winnls-lcmapstringa) , когда данные в Юникоде нормализуются к ключу, что позволяет определяемым пользователем флагам переопределять значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59c46-113">These flags get passed to [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) when Unicode data gets normalized to a key, which enables user-defined flags to override the default.</span></span>

<span data-ttu-id="59c46-114">**Windows 2000**: только два допустимых значения для **dwFlags** :</span><span class="sxs-lookup"><span data-stu-id="59c46-114">**Windows 2000**:  The only two legal values for **dwFlags** are:</span></span>

  - <span data-ttu-id="59c46-115">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)</span><span class="sxs-lookup"><span data-stu-id="59c46-115">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )</span></span>

<!-- end list -->

  - <span data-ttu-id="59c46-116">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)</span><span class="sxs-lookup"><span data-stu-id="59c46-116">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )</span></span>

<span data-ttu-id="59c46-117">**двмапфлагс** имеет следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="59c46-117">**dwMapFlags** has the following restrictions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="59c46-118">Значение</span><span class="sxs-lookup"><span data-stu-id="59c46-118">Value</span></span></p></th>
<th><p><span data-ttu-id="59c46-119">Значение</span><span class="sxs-lookup"><span data-stu-id="59c46-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59c46-120">LCMAP_SORTKEY</span><span class="sxs-lookup"><span data-stu-id="59c46-120">LCMAP_SORTKEY</span></span></p></td>
<td><p><span data-ttu-id="59c46-121">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="59c46-121">Mandatory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c46-122">LCMAP_BYTEREV</span><span class="sxs-lookup"><span data-stu-id="59c46-122">LCMAP_BYTEREV</span></span></p></td>
<td><p><span data-ttu-id="59c46-123">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="59c46-123">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c46-124">NORM_IGNORECASE</span><span class="sxs-lookup"><span data-stu-id="59c46-124">NORM_IGNORECASE</span></span></p></td>
<td><p><span data-ttu-id="59c46-125">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="59c46-125">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c46-126">NORM_IGNORENONSPACE</span><span class="sxs-lookup"><span data-stu-id="59c46-126">NORM_IGNORENONSPACE</span></span></p></td>
<td><p><span data-ttu-id="59c46-127">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="59c46-127">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c46-128">NORM_IGNORESYMBOLS</span><span class="sxs-lookup"><span data-stu-id="59c46-128">NORM_IGNORESYMBOLS</span></span></p></td>
<td><p><span data-ttu-id="59c46-129">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="59c46-129">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c46-130">NORM_IGNOREKANATYPE</span><span class="sxs-lookup"><span data-stu-id="59c46-130">NORM_IGNOREKANATYPE</span></span></p></td>
<td><p><span data-ttu-id="59c46-131">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="59c46-131">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c46-132">NORM_IGNOREWIDTH</span><span class="sxs-lookup"><span data-stu-id="59c46-132">NORM_IGNOREWIDTH</span></span></p></td>
<td><p><span data-ttu-id="59c46-133">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="59c46-133">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c46-134">SORT_STRINGSORT</span><span class="sxs-lookup"><span data-stu-id="59c46-134">SORT_STRINGSORT</span></span></p></td>
<td><p><span data-ttu-id="59c46-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="59c46-135">Optional.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="59c46-136">Требования</span><span class="sxs-lookup"><span data-stu-id="59c46-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59c46-137"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="59c46-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="59c46-138">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="59c46-138">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="59c46-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="59c46-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="59c46-140">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="59c46-140">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="59c46-141"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="59c46-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="59c46-142">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="59c46-142">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="59c46-143">См. также:</span><span class="sxs-lookup"><span data-stu-id="59c46-143">See Also</span></span>

[<span data-ttu-id="59c46-144">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="59c46-144">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="59c46-145">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="59c46-145">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="59c46-146">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="59c46-146">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)
