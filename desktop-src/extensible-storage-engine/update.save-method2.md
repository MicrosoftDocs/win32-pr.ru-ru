---
description: Дополнительные сведения см. в статье метод обновления. Save.
title: Метод Update. Save
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57693d3952f011127e60fdfb70dd2352c2f15207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542418"
---
# <a name="updatesave-method"></a><span data-ttu-id="99e24-103">Метод Update. Save</span><span class="sxs-lookup"><span data-stu-id="99e24-103">Update.Save method</span></span>

<span data-ttu-id="99e24-104">Обновите TableID.</span><span class="sxs-lookup"><span data-stu-id="99e24-104">Update the tableid.</span></span>

<span data-ttu-id="99e24-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99e24-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99e24-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99e24-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99e24-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99e24-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a><span data-ttu-id="99e24-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="99e24-108">Remarks</span></span>

<span data-ttu-id="99e24-109">Сохранение является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="99e24-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="99e24-110">Обновление начинается с вызова метода создания объекта Update, а затем путем вызова Жетсетколумн или Жетсетколумнс один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="99e24-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="99e24-111">Наконец, для завершения операции обновления вызывается обновление.</span><span class="sxs-lookup"><span data-stu-id="99e24-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="99e24-112">Индексы обновляются только с помощью Update, а не во время Жетсетколумн или Жетсетколумнс.</span><span class="sxs-lookup"><span data-stu-id="99e24-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="99e24-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99e24-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99e24-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="99e24-114">Reference</span></span>

[<span data-ttu-id="99e24-115">Класс обновления</span><span class="sxs-lookup"><span data-stu-id="99e24-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="99e24-116">Обновить элементы</span><span class="sxs-lookup"><span data-stu-id="99e24-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="99e24-117">Сохранить перегрузку</span><span class="sxs-lookup"><span data-stu-id="99e24-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="99e24-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="99e24-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
