---
description: 'Дополнительные сведения: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809682"
---
# <a name="jet_dbid"></a><span data-ttu-id="256f7-103">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="256f7-103">JET_DBID</span></span>


<span data-ttu-id="256f7-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="256f7-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbid"></a><span data-ttu-id="256f7-105">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="256f7-105">JET_DBID</span></span>

<span data-ttu-id="256f7-106">Тип данных **JET_DBID** содержит обработчик для базы данных.</span><span class="sxs-lookup"><span data-stu-id="256f7-106">The **JET_DBID** data type contains the handle to the database.</span></span> <span data-ttu-id="256f7-107">Для управления схемой базы данных используется маркер базы данных.</span><span class="sxs-lookup"><span data-stu-id="256f7-107">A database handle is used to manage the schema of a database.</span></span> <span data-ttu-id="256f7-108">Его также можно использовать для управления таблицами в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="256f7-108">It can also be used to manage the tables inside of that database.</span></span>

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a><span data-ttu-id="256f7-109">Типы данных</span><span class="sxs-lookup"><span data-stu-id="256f7-109">Data Types</span></span>

<span data-ttu-id="256f7-110">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="256f7-110">JET_DBID</span></span>

<span data-ttu-id="256f7-111">Обработчик для базы данных.</span><span class="sxs-lookup"><span data-stu-id="256f7-111">Handle to the database.</span></span>

<span data-ttu-id="256f7-112">Значение JET_dbidNil указывает, что маркер является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="256f7-112">A value of JET_dbidNil indicates that the handle is invalid.</span></span>

### <a name="remarks"></a><span data-ttu-id="256f7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="256f7-113">Remarks</span></span>

<span data-ttu-id="256f7-114">Маркер базы данных создается с помощью вызова [жеткреатедатабасе](./jetcreatedatabase-function.md) или [жетопендатабасе](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="256f7-114">A database handle is created by means of a call to [JetCreateDatabase](./jetcreatedatabase-function.md) or [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

<span data-ttu-id="256f7-115">Маркер базы данных может быть явно закрыт [жетклоседатабасе](./jetclosedatabase-function.md) или неявно закрыт [жетендсессион](./jetendsession-function.md) или [жеттерм](./jetterm-function.md).</span><span class="sxs-lookup"><span data-stu-id="256f7-115">A database handle can be explicitly closed by [JetCloseDatabase](./jetclosedatabase-function.md) or implicitly closed by [JetEndSession](./jetendsession-function.md) or [JetTerm](./jetterm-function.md).</span></span>

<span data-ttu-id="256f7-116">Маркер базы данных может использоваться только в том сеансе, в котором он был создан.</span><span class="sxs-lookup"><span data-stu-id="256f7-116">A database handle can be used only within the session in which it was created.</span></span> <span data-ttu-id="256f7-117">Наличие маркера базы данных соответствует логическому открытию базы данных.</span><span class="sxs-lookup"><span data-stu-id="256f7-117">The existence of a database handle corresponds to the logical open of a database.</span></span> <span data-ttu-id="256f7-118">Логическое открытие отличается от физического открытия базы данных, что происходит при присоединении базы данных к системе.</span><span class="sxs-lookup"><span data-stu-id="256f7-118">A logical open is different from the physical open of a database, which happens when a database is attached to the system.</span></span>

### <a name="requirements"></a><span data-ttu-id="256f7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="256f7-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="256f7-120"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="256f7-120"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="256f7-121">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="256f7-121">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="256f7-122"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="256f7-122"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="256f7-123">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="256f7-123">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="256f7-124"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="256f7-124"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="256f7-125">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="256f7-125">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="256f7-126">См. также:</span><span class="sxs-lookup"><span data-stu-id="256f7-126">See Also</span></span>

[<span data-ttu-id="256f7-127">жеткреатедатабасе</span><span class="sxs-lookup"><span data-stu-id="256f7-127">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="256f7-128">жетопендатабасе</span><span class="sxs-lookup"><span data-stu-id="256f7-128">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="256f7-129">жетклоседатабасе</span><span class="sxs-lookup"><span data-stu-id="256f7-129">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="256f7-130">жетендсессион</span><span class="sxs-lookup"><span data-stu-id="256f7-130">JetEndSession</span></span>](./jetendsession-function.md)
