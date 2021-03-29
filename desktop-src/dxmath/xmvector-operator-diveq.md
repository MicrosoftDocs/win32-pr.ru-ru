---
description: Оператор присваивания деления.
ms.assetid: 59dee8a1-48c5-4748-8eca-1d0939e90fe0
title: операторы operator/=
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4d0c20975a93215a62bdb6b08dedc839ca8d079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991441"
---
# <a name="operator--operators"></a><span data-ttu-id="aa23c-103">операторы operator/=</span><span class="sxs-lookup"><span data-stu-id="aa23c-103">operator /= operators</span></span>

<span data-ttu-id="aa23c-104">Оператор присваивания деления.</span><span class="sxs-lookup"><span data-stu-id="aa23c-104">Division Assignment operator.</span></span>

### <a name="overload-list"></a><span data-ttu-id="aa23c-105">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="aa23c-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="aa23c-106">Оператор</span><span class="sxs-lookup"><span data-stu-id="aa23c-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="aa23c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="aa23c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="aa23c-108"><a href="/previous-versions/windows/desktop/legacy/ee421377(v=vs.85)"><strong>КСМВЕКТОР:: operator/= (КСМВЕКТОР&, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa23c-108"><a href="/previous-versions/windows/desktop/legacy/ee421377(v=vs.85)"><strong>XMVECTOR::operator /= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="aa23c-109">Делит экземпляр на <code>XMVECTOR</code> значение с плавающей запятой и возвращает ссылку на обновленный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="aa23c-109">Divides an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="aa23c-110"><code>operator /=</code>Компонент делит все компоненты текущего экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на заданное значение с плавающей запятой, возвращая ссылку на обновленный текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="aa23c-110">The <code>operator /=</code> divides each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa23c-111">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="aa23c-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="aa23c-112"><a href="/previous-versions/windows/desktop/legacy/ee421378(v=vs.85)"><strong>КСМВЕКТОР:: operator/= (КСМВЕКТОР&, КСМВЕКТОР)</strong></a></span><span class="sxs-lookup"><span data-stu-id="aa23c-112"><a href="/previous-versions/windows/desktop/legacy/ee421378(v=vs.85)"><strong>XMVECTOR::operator /= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="aa23c-113">Делит один <code>XMVECTOR</code> экземпляр на второй экземпляр, возвращая ссылку на обновленный первоначальный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="aa23c-113">Divides one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="aa23c-114"><code>operator /=</code>Компонент делит все компоненты текущего экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на соответствующий компонент во втором указанном экземпляре <code>XMVECTOR</code> , возвращая ссылку на обновленный первоначальный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="aa23c-114">The <code>operator /=</code> divides each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa23c-115">Этот оператор доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="aa23c-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="aa23c-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa23c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa23c-117">Операторы КСМВЕКТОР</span><span class="sxs-lookup"><span data-stu-id="aa23c-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="aa23c-118">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="aa23c-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aa23c-119">**Тип данных КСМВЕКТОР**</span><span class="sxs-lookup"><span data-stu-id="aa23c-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
