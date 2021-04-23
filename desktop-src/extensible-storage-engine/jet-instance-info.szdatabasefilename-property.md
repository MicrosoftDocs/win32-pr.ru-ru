---
description: 'Дополнительные сведения о свойстве: JET_INSTANCE_INFO. Сздатабасефиленаме'
title: Свойство JET_INSTANCE_INFO. Сздатабасефиленаме
TOCTitle: 'szDatabaseFileName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szdatabasefilename(v=EXCHG.10)
ms:contentKeyID: 55103711
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szDatabaseFileName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szDatabaseFileName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55414184fd25a90f3fbb57be8fb5d84264fde5dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684430"
---
# <a name="jet_instance_infoszdatabasefilename-property"></a><span data-ttu-id="dab35-103">Свойство JET_INSTANCE_INFO. Сздатабасефиленаме</span><span class="sxs-lookup"><span data-stu-id="dab35-103">JET_INSTANCE_INFO.szDatabaseFileName property</span></span>

<span data-ttu-id="dab35-104">Возвращает коллекцию строк, содержащую имя файла базы данных, присоединенной к экземпляру базы данных.</span><span class="sxs-lookup"><span data-stu-id="dab35-104">Gets a collection of strings, each holding the file name of a database that is attached to the database instance.</span></span> <span data-ttu-id="dab35-105">Массив содержит элементы cDatabase.</span><span class="sxs-lookup"><span data-stu-id="dab35-105">The array has cDatabases elements.</span></span>

<span data-ttu-id="dab35-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dab35-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dab35-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dab35-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dab35-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dab35-108">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property szDatabaseFileName As IList(Of String)
    Get
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As IList(Of String)

value = instance.szDatabaseFileName
```

``` csharp
public IList<string> szDatabaseFileName { get; }
```

#### <a name="property-value"></a><span data-ttu-id="dab35-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dab35-109">Property value</span></span>

<span data-ttu-id="dab35-110">Тип: [System. Collections. Generic. IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span><span class="sxs-lookup"><span data-stu-id="dab35-110">Type: [System.Collections.Generic.IList](/dotnet/api/system.collections.generic.ilist-1)\<[String](/dotnet/api/system.string)\></span></span>  

## <a name="see-also"></a><span data-ttu-id="dab35-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dab35-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dab35-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="dab35-112">Reference</span></span>

[<span data-ttu-id="dab35-113">Класс JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="dab35-113">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="dab35-114">Элементы JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="dab35-114">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="dab35-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dab35-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
