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
ms.openlocfilehash: ad933c9601dc1a20932550aef363e067458ff79e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389033"
---
# <a name="updatesave-method"></a><span data-ttu-id="76451-103">Метод Update. Save</span><span class="sxs-lookup"><span data-stu-id="76451-103">Update.Save method</span></span>

<span data-ttu-id="76451-104">Обновите TableID.</span><span class="sxs-lookup"><span data-stu-id="76451-104">Update the tableid.</span></span>

<span data-ttu-id="76451-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="76451-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="76451-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="76451-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="76451-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76451-107">Syntax</span></span>

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

## <a name="remarks"></a><span data-ttu-id="76451-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="76451-108">Remarks</span></span>

<span data-ttu-id="76451-109">Сохранение является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="76451-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="76451-110">Обновление начинается с вызова метода создания объекта Update, а затем путем вызова Жетсетколумн или Жетсетколумнс один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="76451-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="76451-111">Наконец, для завершения операции обновления вызывается обновление.</span><span class="sxs-lookup"><span data-stu-id="76451-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="76451-112">Индексы обновляются только с помощью Update, а не во время Жетсетколумн или Жетсетколумнс.</span><span class="sxs-lookup"><span data-stu-id="76451-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="76451-113">См. также</span><span class="sxs-lookup"><span data-stu-id="76451-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="76451-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="76451-114">Reference</span></span>

[<span data-ttu-id="76451-115">Класс обновления</span><span class="sxs-lookup"><span data-stu-id="76451-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="76451-116">Обновить элементы</span><span class="sxs-lookup"><span data-stu-id="76451-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="76451-117">Сохранить перегрузку</span><span class="sxs-lookup"><span data-stu-id="76451-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="76451-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="76451-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
