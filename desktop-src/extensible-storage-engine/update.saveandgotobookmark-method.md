---
description: 'Дополнительные сведения: метод Update. Савеандготобукмарк'
title: Метод Update. Савеандготобукмарк
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711195"
---
# <a name="updatesaveandgotobookmark-method"></a><span data-ttu-id="6c37e-103">Метод Update. Савеандготобукмарк</span><span class="sxs-lookup"><span data-stu-id="6c37e-103">Update.SaveAndGotoBookmark method</span></span>

<span data-ttu-id="6c37e-104">Обновите TableID и разместите TableID на записи, которая была изменена.</span><span class="sxs-lookup"><span data-stu-id="6c37e-104">Update the tableid and position the tableid on the record that was modified.</span></span> <span data-ttu-id="6c37e-105">Это может быть полезно при вставке записи, так как по умолчанию TableID остается в старом расположении.</span><span class="sxs-lookup"><span data-stu-id="6c37e-105">This can be useful when inserting a record because by default the tableid remains in its old location.</span></span>

<span data-ttu-id="6c37e-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c37e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c37e-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c37e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c37e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c37e-108">Syntax</span></span>

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a><span data-ttu-id="6c37e-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c37e-109">Remarks</span></span>

<span data-ttu-id="6c37e-110">Сохранение является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="6c37e-110">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="6c37e-111">Обновление начинается с вызова метода создания объекта Update, а затем путем вызова Жетсетколумн или Жетсетколумнс один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="6c37e-111">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="6c37e-112">Наконец, для завершения операции обновления вызывается обновление.</span><span class="sxs-lookup"><span data-stu-id="6c37e-112">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="6c37e-113">Индексы обновляются только с помощью Update, а не во время Жетсетколумн или Жетсетколумнс.</span><span class="sxs-lookup"><span data-stu-id="6c37e-113">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c37e-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c37e-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c37e-115">Справочник</span><span class="sxs-lookup"><span data-stu-id="6c37e-115">Reference</span></span>

[<span data-ttu-id="6c37e-116">Класс обновления</span><span class="sxs-lookup"><span data-stu-id="6c37e-116">Update class</span></span>](./update-class.md)

[<span data-ttu-id="6c37e-117">Обновить элементы</span><span class="sxs-lookup"><span data-stu-id="6c37e-117">Update members</span></span>](./update-members.md)

[<span data-ttu-id="6c37e-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6c37e-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
