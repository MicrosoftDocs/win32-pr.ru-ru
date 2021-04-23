---
description: 'Дополнительные сведения о свойстве: JET_TABLECREATE. Сзкаллбакк'
title: Свойство JET_TABLECREATE. Сзкаллбакк
TOCTitle: 'szCallback property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.szcallback(v=EXCHG.10)
ms:contentKeyID: 55103969
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a987f274cf82ebdc3c2113fd1636174c51382f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692130"
---
# <a name="jet_tablecreateszcallback-property"></a><span data-ttu-id="5a123-103">Свойство JET_TABLECREATE. Сзкаллбакк</span><span class="sxs-lookup"><span data-stu-id="5a123-103">JET_TABLECREATE.szCallback property</span></span>

<span data-ttu-id="5a123-104">Возвращает или задает функцию обратного вызова, используемую для таблицы.</span><span class="sxs-lookup"><span data-stu-id="5a123-104">Gets or sets a callback function to use for the table.</span></span> <span data-ttu-id="5a123-105">Это в формате "модуль \! FunctionName" и предполагает неуправляемый код.</span><span class="sxs-lookup"><span data-stu-id="5a123-105">This is in the form "module\!functionName", and assumes unmanaged code.</span></span> <span data-ttu-id="5a123-106">В качестве альтернативы см. **жетрегистеркаллбакк (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)** .</span><span class="sxs-lookup"><span data-stu-id="5a123-106">See **JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)** for an alternative.</span></span>

<span data-ttu-id="5a123-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a123-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a123-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a123-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a123-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a123-109">Syntax</span></span>

``` vb
'Declaration
Public Property szCallback As String
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As String

value = instance.szCallback

instance.szCallback = value
```

``` csharp
public string szCallback { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5a123-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5a123-110">Property value</span></span>

<span data-ttu-id="5a123-111">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5a123-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a123-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a123-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a123-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="5a123-113">Reference</span></span>

[<span data-ttu-id="5a123-114">Класс JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="5a123-114">JET_TABLECREATE class</span></span>](./jet-tablecreate-class.md)

[<span data-ttu-id="5a123-115">Элементы JET_TABLECREATE</span><span class="sxs-lookup"><span data-stu-id="5a123-115">JET_TABLECREATE members</span></span>](./jet-tablecreate-members.md)

[<span data-ttu-id="5a123-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5a123-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
