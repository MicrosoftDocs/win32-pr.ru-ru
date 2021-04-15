---
description: Обращается к конкретным элементам матрицы, на которые ссылается строка и столбец из текущего экземпляра КСММАТРИКС.
ms.assetid: 917d44b0-4625-412f-b3ad-5955856689d5
title: Операторы КСММАТРИКС operator ()
ms.topic: reference
ms.date: 12/06/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 900af391208505d862bc1861534c8e3f1c34faf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701844"
---
# <a name="xmmatrix-operator--operators"></a><span data-ttu-id="933d2-103">Операторы КСММАТРИКС operator ()</span><span class="sxs-lookup"><span data-stu-id="933d2-103">XMMATRIX operator () operators</span></span>

<span data-ttu-id="933d2-104">Обращается к конкретным элементам матрицы, на которые ссылается строка и столбец из текущего экземпляра `XMMATRIX` .</span><span class="sxs-lookup"><span data-stu-id="933d2-104">Accesses specific matrix elements referenced by row and column from the current instance of `XMMATRIX`.</span></span>

<span data-ttu-id="933d2-105">Обращается к конкретным элементам матрицы, на которые ссылается строка и столбец из текущего экземпляра [ **ксмматрикс**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)</span><span class="sxs-lookup"><span data-stu-id="933d2-105">Accesses specific matrix elements referenced by row and column from the current instance of [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)</span></span>

### <a name="overload-list"></a><span data-ttu-id="933d2-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="933d2-106">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="933d2-107">Оператор</span><span class="sxs-lookup"><span data-stu-id="933d2-107">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="933d2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="933d2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="933d2-109"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>КСММАТРИКС:: operator () (size_t, size_t)</strong></a></span><span class="sxs-lookup"><span data-stu-id="933d2-109"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>XMMATRIX::operator () (size_t,size_t)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="933d2-110">Возвращает объект <code>reference</code> матрицы экземпляра в <code>XMMATRIX</code> соответствии с аргументами строки и столбца.</span><span class="sxs-lookup"><span data-stu-id="933d2-110">Returns a <code>reference</code> to a matrix element of an instance <code>XMMATRIX</code> as specified by row and column arguments.</span></span><br/> <span data-ttu-id="933d2-111">Этот оператор возвращает <code>reference</code> в элемент Matrix экземпляра <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>ксмматрикс</strong></a> , как указано в аргументах строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="933d2-111">This operator returns a <code>reference</code> to a matrix element of an instance <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> as specified by row and column arguments.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="933d2-112">Этот оператор доступен только при разработке с использованием C++.</span><span class="sxs-lookup"><span data-stu-id="933d2-112">This operator is only available when developing with C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="933d2-113"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>КСММАТРИКС:: operator () (size_t, size_t)</strong></a></span><span class="sxs-lookup"><span data-stu-id="933d2-113"><a href="/windows/desktop/api/directxmath/nf-directxmath-xmmatrix-operator-function-call(size_t_size_t)"><strong>XMMATRIX::operator () (size_t,size_t)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="933d2-114">Возвращает значение элемента Matrix в экземпляре в <code>XMMATRIX</code> соответствии с аргументами строки и столбца.</span><span class="sxs-lookup"><span data-stu-id="933d2-114">Return the value of a matrix element in an instance <code>XMMATRIX</code> as specified by row and column arguments.</span></span><br/> <span data-ttu-id="933d2-115">Этот оператор возвращает значение элемента Matrix экземпляра <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>ксмматрикс</strong></a> , как указано в аргументах строк и столбцов.</span><span class="sxs-lookup"><span data-stu-id="933d2-115">This operator returns the value of a matrix element of an instance <a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>XMMATRIX</strong></a> as specified by row and column arguments.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="933d2-116">Этот оператор доступен только при разработке с использованием C++.</span><span class="sxs-lookup"><span data-stu-id="933d2-116">This operator is only available when developing with C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="933d2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="933d2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933d2-118">Операторы КСММАТРИКС</span><span class="sxs-lookup"><span data-stu-id="933d2-118">XMMATRIX Operators</span></span>](ovw-xmmatrix-operators.md)
</dt> <dt>

<span data-ttu-id="933d2-119">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="933d2-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="933d2-120">**ксмматрикс**</span><span class="sxs-lookup"><span data-stu-id="933d2-120">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)
</dt> </dl>

 

 
