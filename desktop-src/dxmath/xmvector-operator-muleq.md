---
description: Операторы присваивания умножения.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: operator * = операторы
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 486e85ae8f541c802e50c38d29cd16beb746b587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692610"
---
# <a name="operator--operators"></a><span data-ttu-id="e2253-103">operator \* = операторы</span><span class="sxs-lookup"><span data-stu-id="e2253-103">operator \*= operators</span></span>

<span data-ttu-id="e2253-104">Операторы присваивания умножения</span><span class="sxs-lookup"><span data-stu-id="e2253-104">Multiplication assignment operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="e2253-105">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="e2253-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e2253-106">Оператор</span><span class="sxs-lookup"><span data-stu-id="e2253-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e2253-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e2253-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="e2253-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>КСМВЕКТОР:: operator \* = (КСМВЕКТОР&, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2253-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e2253-109">Умножает <code>XMVECTOR</code> экземпляр на значение с плавающей запятой и возвращает ссылку на обновленный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e2253-109">Multiplies an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="e2253-110"><code>operator \*=</code>Компонент умножает все компоненты текущего экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на заданное значение с плавающей запятой, возвращая ссылку на обновленный текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e2253-110">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e2253-111">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="e2253-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="e2253-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>КСМВЕКТОР:: operator \* = (КСМВЕКТОР&, КСМВЕКТОР)</strong></a></span><span class="sxs-lookup"><span data-stu-id="e2253-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="e2253-113">Умножает один <code>XMVECTOR</code> экземпляр на второй экземпляр, возвращая ссылку на обновленный первоначальный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e2253-113">Multiplies one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="e2253-114"><code>operator \*=</code>Компонент умножает все компоненты текущего экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на соответствующий компонент во втором указанном экземпляре <code>XMVECTOR</code> , возвращая ссылку на обновленный первоначальный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e2253-114">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e2253-115">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="e2253-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="e2253-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2253-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2253-117">Операторы КСМВЕКТОР</span><span class="sxs-lookup"><span data-stu-id="e2253-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="e2253-118">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e2253-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2253-119">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="e2253-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
