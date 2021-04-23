---
description: Вычитание и операторы отрицания.
ms.assetid: b3a3da02-4fba-4f76-90d8-15f605c73f16
title: операторы operator
ms.topic: reference
ms.date: 12/06/2018
ms.openlocfilehash: 21c10490db92a335f07f298876d838f2152d17b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544050"
---
# <a name="operator---operators"></a><span data-ttu-id="29dbd-103">операторы operator</span><span class="sxs-lookup"><span data-stu-id="29dbd-103">operator - operators</span></span>

<span data-ttu-id="29dbd-104">Вычитание и операторы отрицания</span><span class="sxs-lookup"><span data-stu-id="29dbd-104">Subtraction and negation operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="29dbd-105">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="29dbd-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="29dbd-106">Оператор</span><span class="sxs-lookup"><span data-stu-id="29dbd-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="29dbd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="29dbd-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="29dbd-108"><a href="/previous-versions/windows/desktop/legacy/ee421383(v=vs.85)"><strong>КСМВЕКТОР:: operator-(КСМВЕКТОР)</strong></a></span><span class="sxs-lookup"><span data-stu-id="29dbd-108"><a href="/previous-versions/windows/desktop/legacy/ee421383(v=vs.85)"><strong>XMVECTOR::operator - (XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="29dbd-109">Вычисление отрицания <code>XMVECTOR</code> экземпляра.</span><span class="sxs-lookup"><span data-stu-id="29dbd-109">Computes the negation of an <code>XMVECTOR</code> instance.</span></span><br/> <span data-ttu-id="29dbd-110"><code>operator -</code>Метод принимает экземпляр <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> и возвращает новый экземпляр <code>XMVECTOR</code> , при котором каждый компонент имеет отрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="29dbd-110">The <code>operator -</code> takes an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> and returns a new instance of <code>XMVECTOR</code>, with each component negated.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="29dbd-111">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="29dbd-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="29dbd-112"><a href="/previous-versions/windows/desktop/legacy/ee421385(v=vs.85)"><strong>КСМВЕКТОР:: operator — (КСМВЕКТОР, КСМВЕКТОР)</strong></a></span><span class="sxs-lookup"><span data-stu-id="29dbd-112"><a href="/previous-versions/windows/desktop/legacy/ee421385(v=vs.85)"><strong>XMVECTOR::operator - (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="29dbd-113">Вычитает один экземпляр <code>XMVECTOR</code> из второго экземпляра, возвращая результат в новом экземпляре <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="29dbd-113">Subtracts one instance of <code>XMVECTOR</code> from a second instance, returning the result in a new instance of <code>XMVECTOR</code>.</span></span> <br/> <span data-ttu-id="29dbd-114"><code>operator -</code>Вычитает каждый компонент экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> из каждого компонента другого экземпляра <code>XMVECTOR</code> , возвращая новый <code>XMVECTOR</code> экземпляр, содержащий результат.</span><span class="sxs-lookup"><span data-stu-id="29dbd-114">The <code>operator -</code> subtracts each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> from each component of another instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="29dbd-115">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="29dbd-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="29dbd-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29dbd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29dbd-117">Операторы КСМВЕКТОР</span><span class="sxs-lookup"><span data-stu-id="29dbd-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="29dbd-118">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="29dbd-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29dbd-119">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="29dbd-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
