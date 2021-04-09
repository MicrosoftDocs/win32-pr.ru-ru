---
description: Дополнительные сведения о перечислении Креатедатабасегрбит
title: Перечисление Креатедатабасегрбит
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080386"
---
# <a name="createdatabasegrbit-enumeration"></a><span data-ttu-id="d086d-103">Перечисление Креатедатабасегрбит</span><span class="sxs-lookup"><span data-stu-id="d086d-103">CreateDatabaseGrbit enumeration</span></span>

<span data-ttu-id="d086d-104">Параметры для [жеткреатедатабасе (JET_SESID, String, String, JET_DBID, креатедатабасегрбит)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="d086d-104">Options for [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="d086d-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="d086d-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="d086d-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d086d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d086d-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d086d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d086d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d086d-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="d086d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d086d-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d086d-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="d086d-110">Member name</span></span></th>
<th><span data-ttu-id="d086d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d086d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d086d-112">Нет</span><span class="sxs-lookup"><span data-stu-id="d086d-112">None</span></span></td>
<td><span data-ttu-id="d086d-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d086d-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="d086d-114">овервритиксистинг</span><span class="sxs-lookup"><span data-stu-id="d086d-114">OverwriteExisting</span></span></td>
<td><span data-ttu-id="d086d-115">По умолчанию, если вызывается Жеткреатедатабасе и база данных уже существует, вызов API завершится ошибкой и исходная база данных не будет перезаписана.</span><span class="sxs-lookup"><span data-stu-id="d086d-115">By default, if JetCreateDatabase is called and the database already exists, the Api call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="d086d-116">Овервритиксистинг изменяет это поведение, и старая база данных будет перезаписана новой.</span><span class="sxs-lookup"><span data-stu-id="d086d-116">OverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="d086d-117">рековерйофф</span><span class="sxs-lookup"><span data-stu-id="d086d-117">RecoveryOff</span></span></td>
<td><span data-ttu-id="d086d-118">Отключает ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="d086d-118">Turns off logging.</span></span> <span data-ttu-id="d086d-119">Установка этого бита теряет возможность воспроизведения файлов журнала и восстановления базы данных до стабильного работоспособного состояния после сбоя.</span><span class="sxs-lookup"><span data-stu-id="d086d-119">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="d086d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d086d-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d086d-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="d086d-121">Reference</span></span>

[<span data-ttu-id="d086d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d086d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
