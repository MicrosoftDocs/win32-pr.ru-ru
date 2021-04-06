---
description: 'Дополнительные сведения о свойстве: JET_INDEXCREATE. Кбкэймост'
title: Свойство JET_INDEXCREATE. Кбкэймост
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911464"
---
# <a name="jet_indexcreatecbkeymost-property"></a><span data-ttu-id="82af7-103">Свойство JET_INDEXCREATE. Кбкэймост</span><span class="sxs-lookup"><span data-stu-id="82af7-103">JET_INDEXCREATE.cbKeyMost property</span></span>

<span data-ttu-id="82af7-104">Возвращает или задает максимально допустимый размер (в байтах) для ключей в индексе.</span><span class="sxs-lookup"><span data-stu-id="82af7-104">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="82af7-105">Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа.</span><span class="sxs-lookup"><span data-stu-id="82af7-105">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="82af7-106">Максимальный размер ключа зависит от размера страницы базы данных [датабасепажесизе](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="82af7-106">The maximum key size is dependent on the database page size [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="82af7-107">Максимальный размер ключа можно получить с помощью [кэймост](./systemparameters.keymost-property.md).</span><span class="sxs-lookup"><span data-stu-id="82af7-107">The maximum key size can be retrieved with [KeyMost](./systemparameters.keymost-property.md).</span></span> <span data-ttu-id="82af7-108">Этот параметр не учитывается в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="82af7-108">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="82af7-109">В отличие от неуправляемого API, **индекскэймост ()** (JET_bitIndexKeyMost) не требуется, он будет добавлен автоматически.</span><span class="sxs-lookup"><span data-stu-id="82af7-109">Unlike the unmanaged API, **IndexKeyMost()** (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span>

<span data-ttu-id="82af7-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82af7-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82af7-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82af7-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82af7-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82af7-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="82af7-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="82af7-113">Property value</span></span>

<span data-ttu-id="82af7-114">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="82af7-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="82af7-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82af7-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82af7-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="82af7-116">Reference</span></span>

[<span data-ttu-id="82af7-117">Класс JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="82af7-117">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="82af7-118">Элементы JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="82af7-118">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="82af7-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="82af7-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
