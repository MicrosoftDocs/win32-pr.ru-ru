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
ms.openlocfilehash: 13280fd5da109012ac90ff55a778f8f5cd6a5b95
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627731"
---
# <a name="operator--operators"></a>operator \* = операторы

Операторы присваивания умножения

### <a name="overload-list"></a>Список перегрузок



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Оператор</th>
<th >Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>КСМВЕКТОР:: operator * = (КСМВЕКТОР&, float)</strong></a></td>
<td >Умножает <code>XMVECTOR</code> экземпляр на значение с плавающей запятой и возвращает ссылку на обновленный экземпляр. <br/> <code>operator *=</code>Компонент умножает все компоненты текущего экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на заданное значение с плавающей запятой, возвращая ссылку на обновленный текущий экземпляр. <br/>
<blockquote>
[!Note]<br />
Этот оператор доступен только в C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td ><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>КСМВЕКТОР:: operator * = (КСМВЕКТОР&, КСМВЕКТОР)</strong></a></td>
<td >Умножает один <code>XMVECTOR</code> экземпляр на второй экземпляр, возвращая ссылку на обновленный первоначальный экземпляр. <br/> <code>operator *=</code>Компонент умножает все компоненты текущего экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на соответствующий компонент во втором указанном экземпляре <code>XMVECTOR</code> , возвращая ссылку на обновленный первоначальный экземпляр. <br/>
<blockquote>
[!Note]<br />
Этот оператор доступен только в C++.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>См. также

<dl> <dt>

[Операторы КСМВЕКТОР](ovw-xmvector-operators.md)
</dt> <dt>

**Ссылки**
</dt> <dt>

[**Тип данных КСМВЕКТОР**](xmvector-data-type.md)
</dt> </dl>

 

 
