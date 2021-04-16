---
description: 'Дополнительные сведения о свойстве: JET_OPENTEMPORARYTABLE. Кбкэймост'
title: Свойство JET_OPENTEMPORARYTABLE. Кбкэймост (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712879"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a><span data-ttu-id="1f2c9-103">Свойство JET_OPENTEMPORARYTABLE. Кбкэймост</span><span class="sxs-lookup"><span data-stu-id="1f2c9-103">JET_OPENTEMPORARYTABLE.cbKeyMost property</span></span>

<span data-ttu-id="1f2c9-104">Возвращает или задает максимальный размер ключа, представляющего заданную строку.</span><span class="sxs-lookup"><span data-stu-id="1f2c9-104">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="1f2c9-105">Для управления способом усечения ключей можно задать максимальный размер ключа.</span><span class="sxs-lookup"><span data-stu-id="1f2c9-105">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="1f2c9-106">Усечение ключа важно, так как это может повлиять на то, что строки считаются разными.</span><span class="sxs-lookup"><span data-stu-id="1f2c9-106">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="1f2c9-107">Если этот параметр имеет значение 0 или 255, то максимальный размер ключа и его семантика остаются идентичными максимальному размеру ключа, поддерживаемому Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f2c9-107">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="1f2c9-108">Для этого параметра также можно задать большее значение в качестве функции размера страницы базы данных для экземпляра [датабасепажесизе](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="1f2c9-108">This parameter may also be set to a larger value as a function of the database page size for the instance [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="1f2c9-109">Дополнительные сведения см. в разделе [кэймост](./vistaparam.keymost-field.md) .</span><span class="sxs-lookup"><span data-stu-id="1f2c9-109">See [KeyMost](./vistaparam.keymost-field.md) for more information.</span></span>

<span data-ttu-id="1f2c9-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f2c9-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1f2c9-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f2c9-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2c9-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f2c9-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1f2c9-113">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1f2c9-113">Property value</span></span>

<span data-ttu-id="1f2c9-114">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1f2c9-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1f2c9-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f2c9-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f2c9-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="1f2c9-116">Reference</span></span>

[<span data-ttu-id="1f2c9-117">Класс JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="1f2c9-117">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="1f2c9-118">Элементы JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="1f2c9-118">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="1f2c9-119">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="1f2c9-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
