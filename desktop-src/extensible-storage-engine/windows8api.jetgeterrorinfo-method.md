---
description: 'Дополнительные сведения о методе: Windows8Api. Жетжетерроринфо'
title: Windows8Api. Жетжетерроринфо, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetGetErrorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo(Microsoft.Isam.Esent.Interop.JET_err,Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetgeterrorinfo(v=EXCHG.10)
ms:contentKeyID: 55104459
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetGetErrorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c94e6594c2d52769f5034bdf1c7253bee838edaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701769"
---
# <a name="windows8apijetgeterrorinfo-method"></a><span data-ttu-id="9cff3-103">Windows8Api. Жетжетерроринфо, метод</span><span class="sxs-lookup"><span data-stu-id="9cff3-103">Windows8Api.JetGetErrorInfo method</span></span>

<span data-ttu-id="9cff3-104">Получает расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9cff3-104">Gets extended information about an error.</span></span>

<span data-ttu-id="9cff3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9cff3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="9cff3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9cff3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9cff3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9cff3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetErrorInfo ( _
    error As JET_err, _
    <OutAttribute> ByRef errinfo As JET_ERRINFOBASIC _
)
'Usage
Dim error As JET_err
Dim errinfo As JET_ERRINFOBASICWindows8Api.JetGetErrorInfo(error, errinfo)
```

``` csharp
public static void JetGetErrorInfo(
    JET_err error,
    out JET_ERRINFOBASIC errinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="9cff3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9cff3-108">Parameters</span></span>

  - <span data-ttu-id="9cff3-109">error</span><span class="sxs-lookup"><span data-stu-id="9cff3-109">error</span></span>  
    <span data-ttu-id="9cff3-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9cff3-110">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="9cff3-111">Код ошибки, сведения о которой необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="9cff3-111">The error code about which to retrieve information.</span></span>

<!-- end list -->

  - <span data-ttu-id="9cff3-112">ерринфо</span><span class="sxs-lookup"><span data-stu-id="9cff3-112">errinfo</span></span>  
    <span data-ttu-id="9cff3-113">Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span><span class="sxs-lookup"><span data-stu-id="9cff3-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_ERRINFOBASIC](./jet-errinfobasic-class.md)</span></span>  
    
    <span data-ttu-id="9cff3-114">Сведения об указанном коде ошибки.</span><span class="sxs-lookup"><span data-stu-id="9cff3-114">Information about the specified error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="9cff3-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cff3-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9cff3-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="9cff3-116">Reference</span></span>

[<span data-ttu-id="9cff3-117">Класс Windows8Api</span><span class="sxs-lookup"><span data-stu-id="9cff3-117">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="9cff3-118">Элементы Windows8Api</span><span class="sxs-lookup"><span data-stu-id="9cff3-118">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="9cff3-119">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="9cff3-119">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
