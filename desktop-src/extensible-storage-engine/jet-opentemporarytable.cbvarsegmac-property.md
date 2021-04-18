---
description: 'Дополнительные сведения о свойстве: JET_OPENTEMPORARYTABLE. Кбварсегмак'
title: Свойство JET_OPENTEMPORARYTABLE. Кбварсегмак (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702352"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a><span data-ttu-id="570d6-103">Свойство JET_OPENTEMPORARYTABLE. Кбварсегмак</span><span class="sxs-lookup"><span data-stu-id="570d6-103">JET_OPENTEMPORARYTABLE.cbVarSegMac property</span></span>

<span data-ttu-id="570d6-104">Возвращает или задает максимальный объем данных, который будет использоваться из любой переменной ленгсколумн для создания ключа для данной строки.</span><span class="sxs-lookup"><span data-stu-id="570d6-104">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="570d6-105">Этот параметр может использоваться для управления объемом ключевого пространства, используемого любым ключевым столбцом.</span><span class="sxs-lookup"><span data-stu-id="570d6-105">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="570d6-106">Это ограничение указано в байтах.</span><span class="sxs-lookup"><span data-stu-id="570d6-106">This limit is in bytes.</span></span> <span data-ttu-id="570d6-107">Если этот параметр равен нулю или имеет то же значение, что и свойство [кбкэймост](./jet-opentemporarytable.cbkeymost-property.md) , ограничение не действует.</span><span class="sxs-lookup"><span data-stu-id="570d6-107">If this parameter is zero or is the same as the [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) property then no limit is in effect.</span></span>

<span data-ttu-id="570d6-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="570d6-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="570d6-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="570d6-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="570d6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="570d6-110">Syntax</span></span>

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="570d6-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="570d6-111">Property value</span></span>

<span data-ttu-id="570d6-112">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="570d6-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="570d6-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="570d6-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="570d6-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="570d6-114">Reference</span></span>

[<span data-ttu-id="570d6-115">Класс JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="570d6-115">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="570d6-116">Элементы JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="570d6-116">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="570d6-117">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="570d6-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
