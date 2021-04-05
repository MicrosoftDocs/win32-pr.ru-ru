---
description: 'Дополнительные сведения: структура JET_ERRINFOBASIC_W'
title: Структура JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000542"
---
# <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="d300c-103">Структура JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="d300c-103">JET_ERRINFOBASIC_W Structure</span></span>


<span data-ttu-id="d300c-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d300c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="d300c-105">Структура JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="d300c-105">JET_ERRINFOBASIC_W Structure</span></span>

<span data-ttu-id="d300c-106">Структура **JET_ERRINFOBASIC_W** определяет данные, возвращаемые методом [жетжетерроринфо ()](./jetgeterrorinfow-function.md) при передаче JET_ErrorInfoSpecificErr инфолевел.</span><span class="sxs-lookup"><span data-stu-id="d300c-106">The **JET_ERRINFOBASIC_W** structure defines the data that is returned from the [JetGetErrorInfo()](./jetgeterrorinfow-function.md) method when the JET_ErrorInfoSpecificErr InfoLevel is passed in.</span></span>

<span data-ttu-id="d300c-107">Примечание. Эта документация основана на предварительном выпуске расширяемой подсистемы хранилища.</span><span class="sxs-lookup"><span data-stu-id="d300c-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="d300c-108">Эта информация может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="d300c-108">This information is subject to change.</span></span>

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a><span data-ttu-id="d300c-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="d300c-109">Members</span></span>

<span data-ttu-id="d300c-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="d300c-110">**cbStruct**</span></span>

<span data-ttu-id="d300c-111">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="d300c-111">The size of the structure, in bytes.</span></span> <span data-ttu-id="d300c-112">Он должен иметь значение sizeof (JET_ERRINFOBASIC).</span><span class="sxs-lookup"><span data-stu-id="d300c-112">It must be set to sizeof( JET_ERRINFOBASIC ).</span></span>

<span data-ttu-id="d300c-113">**еррвалуе**</span><span class="sxs-lookup"><span data-stu-id="d300c-113">**errValue**</span></span>

<span data-ttu-id="d300c-114">Вычисленное значение ошибки, переданное для аргумента *пвресулт* в [жетжетерроринфо ()](./jetgeterrorinfow-function.md).</span><span class="sxs-lookup"><span data-stu-id="d300c-114">The error value that was evaluated, as passed in for the *pvResult* argument to [JetGetErrorInfo()](./jetgeterrorinfow-function.md).</span></span>

<span data-ttu-id="d300c-115">**ерркатмостспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="d300c-115">**errcatMostSpecific**</span></span>

<span data-ttu-id="d300c-116">Константа нижнего уровня [JET_ERRCAT](./jet-errcat.md) , связанная с ошибкой; Это значит, что категория конечного уровня в иерархии категорий задокументирована в [JET_ERRCAT](./jet-errcat.md).</span><span class="sxs-lookup"><span data-stu-id="d300c-116">The lowest-level [JET_ERRCAT](./jet-errcat.md) constant that is associated with the error; that is, the leaf-level category in the category hierarchy documented in [JET_ERRCAT](./jet-errcat.md).</span></span>

<span data-ttu-id="d300c-117">**Ргкатегорикалхиерарчи \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="d300c-117">**rgCategoricalHierarchy\[8\]**</span></span>

<span data-ttu-id="d300c-118">Иерархия категорий ошибок, связанных с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="d300c-118">The hierarchy of error categories that is associated with the error.</span></span> <span data-ttu-id="d300c-119">Расположение 0 является самым высоким уровнем в иерархии [JET_ERRCAT](./jet-errcat.md), а остальные являются подкатегориями до тех пор, пока не будет задана наиболее конкретная категория, после чего все категории будут JET_errcatUnknownы.</span><span class="sxs-lookup"><span data-stu-id="d300c-119">Position 0 is the highest level in the hierarchy of [JET_ERRCAT](./jet-errcat.md), and the rest are subcategories until the most specific category is set, after which all categories are JET_errcatUnknown.</span></span>

<span data-ttu-id="d300c-120">**лсаурцелине**</span><span class="sxs-lookup"><span data-stu-id="d300c-120">**lSourceLine**</span></span>

<span data-ttu-id="d300c-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d300c-121">Reserved.</span></span>

<span data-ttu-id="d300c-122">**Ргсзсаурцефиле \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="d300c-122">**rgszSourceFile\[64\]**</span></span>

<span data-ttu-id="d300c-123">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d300c-123">Reserved.</span></span>

### <a name="requirements"></a><span data-ttu-id="d300c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d300c-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d300c-125"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="d300c-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d300c-126">Требуется Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d300c-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d300c-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d300c-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d300c-128">Требуется Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="d300c-128">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d300c-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d300c-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d300c-130">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="d300c-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
