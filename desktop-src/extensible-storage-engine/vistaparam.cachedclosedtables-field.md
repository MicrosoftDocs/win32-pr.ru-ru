---
description: 'Дополнительные сведения о: Вистапарам. Качедклоседтаблес поле'
title: Поле Вистапарам. Качедклоседтаблес (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143501"
---
# <a name="vistaparamcachedclosedtables-field"></a><span data-ttu-id="36f01-103">Вистапарам. Качедклоседтаблес, поле</span><span class="sxs-lookup"><span data-stu-id="36f01-103">VistaParam.CachedClosedTables field</span></span>

<span data-ttu-id="36f01-104">Этот параметр определяет количество ресурсов дерева B +, кэшированных экземпляром после того, как таблицы, которые они представляют, были закрыты приложением.</span><span class="sxs-lookup"><span data-stu-id="36f01-104">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="36f01-105">Большие значения для этого параметра приведут к тому, что ядро СУБД будет использовать больше памяти, но увеличит скорость, с которой приложение может случайно открыть большое количество таблиц.</span><span class="sxs-lookup"><span data-stu-id="36f01-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="36f01-106">Это полезно для приложений, имеющих схему с очень большим количеством таблиц.</span><span class="sxs-lookup"><span data-stu-id="36f01-106">This is useful for applications that have a schema with a very large number of tables.</span></span>

<span data-ttu-id="36f01-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36f01-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="36f01-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36f01-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36f01-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36f01-109">Syntax</span></span>

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a><span data-ttu-id="36f01-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36f01-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36f01-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="36f01-111">Reference</span></span>

[<span data-ttu-id="36f01-112">Класс Вистапарам</span><span class="sxs-lookup"><span data-stu-id="36f01-112">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="36f01-113">Элементы Вистапарам</span><span class="sxs-lookup"><span data-stu-id="36f01-113">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="36f01-114">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="36f01-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
