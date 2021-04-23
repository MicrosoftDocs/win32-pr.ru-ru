---
description: Операторы умножения.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: операторы operator *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155427"
---
# <a name="operator--operators"></a><span data-ttu-id="4ada9-103">\*Операторы операторов</span><span class="sxs-lookup"><span data-stu-id="4ada9-103">operator \* operators</span></span>

<span data-ttu-id="4ada9-104">Операторы умножения</span><span class="sxs-lookup"><span data-stu-id="4ada9-104">Multiplication operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="4ada9-105">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="4ada9-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4ada9-106">Оператор</span><span class="sxs-lookup"><span data-stu-id="4ada9-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4ada9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4ada9-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4ada9-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>КСМВЕКТОР:: operator \* (float, КСМВЕКТОР)</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ada9-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator \* (float,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4ada9-109">Умножьте значение с плавающей запятой на экземпляр <code>XMVECTOR</code> , возвращая результат в новый экземпляр <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="4ada9-109">Multiply a floating point value by an instance of <code>XMVECTOR</code>, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="4ada9-110">Объект <code>operator \*</code> умножает значение с плавающей запятой на каждый компонент экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a>, возвращая новый <code>XMVECTOR</code> экземпляр, компоненты которого содержат результат.</span><span class="sxs-lookup"><span data-stu-id="4ada9-110">The <code>operator \*</code> multiplies a floating point value against each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a>, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ada9-111">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="4ada9-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="4ada9-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>КСМВЕКТОР:: operator \* (КСМВЕКТОР, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ada9-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4ada9-113">Умножьте экземпляр <code>XMVECTOR</code> на значение с плавающей запятой, возвращая результат в новый экземпляр <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="4ada9-113">Multiply an instance of <code>XMVECTOR</code> by a floating point value, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="4ada9-114"><code>operator \*</code>Компонент умножает все компоненты экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на значение с плавающей запятой, возвращая новый <code>XMVECTOR</code> экземпляр, компоненты которого содержат результат.</span><span class="sxs-lookup"><span data-stu-id="4ada9-114">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a floating point value, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ada9-115">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="4ada9-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="4ada9-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>КСМВЕКТОР:: operator \* (КСМВЕКТОР, КСМВЕКТОР)</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ada9-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="4ada9-117">Умножает один экземпляр <code>XMVECTOR</code> на второй экземпляр, возвращая результат в третьем экземпляре.</span><span class="sxs-lookup"><span data-stu-id="4ada9-117">Multiplies one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.</span></span> <br/> <span data-ttu-id="4ada9-118"><code>operator \*</code>Компонент умножает все компоненты экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на соответствующий компонент во втором экземпляре <code>XMVECTOR</code> , возвращая новый <code>XMVECTOR</code> экземпляр, содержащий результат.</span><span class="sxs-lookup"><span data-stu-id="4ada9-118">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ada9-119">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="4ada9-119">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="4ada9-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ada9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ada9-121">Операторы КСМВЕКТОР</span><span class="sxs-lookup"><span data-stu-id="4ada9-121">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="4ada9-122">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="4ada9-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4ada9-123">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="4ada9-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
