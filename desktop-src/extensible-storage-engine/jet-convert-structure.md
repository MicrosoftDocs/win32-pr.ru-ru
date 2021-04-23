---
description: 'Дополнительные сведения: структура JET_CONVERT'
title: Структура JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897953"
---
# <a name="jet_convert-structure"></a><span data-ttu-id="34109-103">Структура JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="34109-103">JET_CONVERT Structure</span></span>


<span data-ttu-id="34109-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="34109-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_convert-structure"></a><span data-ttu-id="34109-105">Структура JET_CONVERT</span><span class="sxs-lookup"><span data-stu-id="34109-105">JET_CONVERT Structure</span></span>

<span data-ttu-id="34109-106">Структура **JET_CONVERT** содержит имя более ранней библиотеки DLL версии ESE, которая используется для чтения баз данных, созданных с использованием более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="34109-106">The **JET_CONVERT** structure contains the name of an earlier ESE version DLL that is used for reading a databases that are created with that earlier version.</span></span> <span data-ttu-id="34109-107">Кроме того, предоставляются другие флаги для управления природой преобразования.</span><span class="sxs-lookup"><span data-stu-id="34109-107">In addition, other flags are provided to control the nature of the conversion.</span></span>

<span data-ttu-id="34109-108">**Windows Server 2003:** Функция в [жеткомпакт](./jetcompact-function.md) , которая выполнила преобразование, была удалена из продукта в Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="34109-108">**Windows Server 2003:** The feature in [JetCompact](./jetcompact-function.md) that performed a conversion was removed from the product in Windows Server 2003.</span></span> <span data-ttu-id="34109-109">Она поддерживается только в Windows 2000 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="34109-109">It is only supported in Windows 2000 and Windows XP.</span></span>

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a><span data-ttu-id="34109-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="34109-110">Members</span></span>

<span data-ttu-id="34109-111">**сзолддлл**</span><span class="sxs-lookup"><span data-stu-id="34109-111">**SzOldDll**</span></span>

<span data-ttu-id="34109-112">Имя, включая сведения о пути, к более ранней версии библиотеки DLL ESE.</span><span class="sxs-lookup"><span data-stu-id="34109-112">The name, including path information, to the earlier version of the ESE DLL.</span></span>

<span data-ttu-id="34109-113">**ффлагс**</span><span class="sxs-lookup"><span data-stu-id="34109-113">**fFlags**</span></span>

<span data-ttu-id="34109-114">Зарезервировано для системного использования.</span><span class="sxs-lookup"><span data-stu-id="34109-114">Reserved for system use.</span></span>

<span data-ttu-id="34109-115">**фсчемачанжесонли**</span><span class="sxs-lookup"><span data-stu-id="34109-115">**fSchemaChangesOnly**</span></span>

<span data-ttu-id="34109-116">Зарезервировано для системного использования.</span><span class="sxs-lookup"><span data-stu-id="34109-116">Reserved for system use.</span></span>

### <a name="requirements"></a><span data-ttu-id="34109-117">Требования</span><span class="sxs-lookup"><span data-stu-id="34109-117">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34109-118"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="34109-118"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="34109-119">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="34109-119">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34109-120"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="34109-120"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="34109-121">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="34109-121">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34109-122"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="34109-122"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="34109-123">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="34109-123">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34109-124"><strong>Юникод</strong></span><span class="sxs-lookup"><span data-stu-id="34109-124"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="34109-125">Реализуется как <strong>JET_CONVERT_W</strong> (Юникод) и <strong>JET_CONVERT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="34109-125">Implemented as <strong>JET_CONVERT_W</strong> (Unicode) and <strong>JET_CONVERT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="34109-126">См. также:</span><span class="sxs-lookup"><span data-stu-id="34109-126">See Also</span></span>

[<span data-ttu-id="34109-127">жеткомпакт</span><span class="sxs-lookup"><span data-stu-id="34109-127">JetCompact</span></span>](./jetcompact-function.md)
