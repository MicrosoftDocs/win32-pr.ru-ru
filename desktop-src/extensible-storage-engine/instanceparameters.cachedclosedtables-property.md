---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Качедклоседтаблес'
title: Инстанцепараметерс. Качедклоседтаблес, свойство
TOCTitle: 'CachedClosedTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55103293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachedClosedTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2465de2df3d25293f5298d40700512b6a086d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811632"
---
# <a name="instanceparameterscachedclosedtables-property"></a><span data-ttu-id="18b56-103">Инстанцепараметерс. Качедклоседтаблес, свойство</span><span class="sxs-lookup"><span data-stu-id="18b56-103">InstanceParameters.CachedClosedTables property</span></span>

<span data-ttu-id="18b56-104">Возвращает или задает значение, определяющее количество ресурсов дерева B +, кэшированных экземпляром после того, как таблицы, которые они представляют, были закрыты приложением.</span><span class="sxs-lookup"><span data-stu-id="18b56-104">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="18b56-105">Большие значения для этого параметра приведут к тому, что ядро СУБД будет использовать больше памяти, но увеличит скорость, с которой приложение может случайно открыть большое количество таблиц.</span><span class="sxs-lookup"><span data-stu-id="18b56-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="18b56-106">Это полезно для приложений, имеющих схему с очень большим количеством таблиц.</span><span class="sxs-lookup"><span data-stu-id="18b56-106">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="18b56-107">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="18b56-107">Supported on Windows Vista and up.</span></span> <span data-ttu-id="18b56-108">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="18b56-108">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="18b56-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="18b56-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="18b56-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="18b56-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="18b56-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18b56-111">Syntax</span></span>

``` vb
'Declaration
Public Property CachedClosedTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachedClosedTables

instance.CachedClosedTables = value
```

``` csharp
public int CachedClosedTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="18b56-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="18b56-112">Property value</span></span>

<span data-ttu-id="18b56-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="18b56-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="18b56-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18b56-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="18b56-115">Справочник</span><span class="sxs-lookup"><span data-stu-id="18b56-115">Reference</span></span>

[<span data-ttu-id="18b56-116">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="18b56-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="18b56-117">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="18b56-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="18b56-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="18b56-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
