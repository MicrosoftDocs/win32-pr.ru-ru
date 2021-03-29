---
description: Дополнительные сведения о перечислении Легацифиленамес
title: Перечисление Легацифиленамес (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: LegacyFileNames enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.legacyfilenames(v=EXCHG.10)
ms:contentKeyID: 55104275
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.EightDotThreeSoftCompat
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames
- Microsoft.Isam.Esent.Interop.Vista.LegacyFileNames.ESE98FileNames
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f3cade11450bcfbad13dcdd114dca6701c5369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991218"
---
# <a name="legacyfilenames-enumeration"></a><span data-ttu-id="8e328-103">Перечисление Легацифиленамес</span><span class="sxs-lookup"><span data-stu-id="8e328-103">LegacyFileNames enumeration</span></span>

<span data-ttu-id="8e328-104">Параметры для Легацифиленамес</span><span class="sxs-lookup"><span data-stu-id="8e328-104">Options for LegacyFileNames</span></span>

<span data-ttu-id="8e328-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8e328-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8e328-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8e328-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8e328-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8e328-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration LegacyFileNames
'Usage
Dim instance As LegacyFileNames
```

``` csharp
public enum LegacyFileNames
```

## <a name="members"></a><span data-ttu-id="8e328-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8e328-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="8e328-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="8e328-109">Member name</span></span></th>
<th><span data-ttu-id="8e328-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8e328-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="8e328-111">ESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="8e328-111">ESE98FileNames</span></span></td>
<td><span data-ttu-id="8e328-112">При наличии этого параметра ядро СУБД будет использовать следующие соглашения об именовании файлов: o файлы журнала транзакций, которые будут использоваться. Журнал для файлов контрольных точек расширения файлов будет использовать. CHK для расширения файла</span><span class="sxs-lookup"><span data-stu-id="8e328-112">When this option is present then the database engine will use the following naming conventions for its files: o Transaction Log files will use .LOG for their file extension o Checkpoint files will use .CHK for their file extension</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="8e328-113">еигхтдотсрисофткомпат</span><span class="sxs-lookup"><span data-stu-id="8e328-113">EightDotThreeSoftCompat</span></span></td>
<td><span data-ttu-id="8e328-114">Сохраните синтаксис именования 8,3 в течение допустимого времени.</span><span class="sxs-lookup"><span data-stu-id="8e328-114">Preserve the 8.3 naming syntax for as long as possible.</span></span> <span data-ttu-id="8e328-115">(не следует изменять, т. е. нет файлов журнала)</span><span class="sxs-lookup"><span data-stu-id="8e328-115">(this should not be changed, w/o ensuring there are no log files)</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="8e328-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e328-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8e328-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="8e328-117">Reference</span></span>

[<span data-ttu-id="8e328-118">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="8e328-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
