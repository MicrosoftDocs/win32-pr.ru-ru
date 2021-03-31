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
# <a name="operator--operators"></a>\*Операторы операторов

Операторы умножения

### <a name="overload-list"></a>Список перегрузок



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Оператор</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>КСМВЕКТОР:: operator * (float, КСМВЕКТОР)</strong></a></td>
<td style="text-align: left;">Умножьте значение с плавающей запятой на экземпляр <code>XMVECTOR</code> , возвращая результат в новый экземпляр <code>XMVECTOR</code> .<br/> Объект <code>operator *</code> умножает значение с плавающей запятой на каждый компонент экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a>, возвращая новый <code>XMVECTOR</code> экземпляр, компоненты которого содержат результат. <br/>
<blockquote>
[!Note]<br />
Этот оператор доступен только в C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>КСМВЕКТОР:: operator * (КСМВЕКТОР, float)</strong></a></td>
<td style="text-align: left;">Умножьте экземпляр <code>XMVECTOR</code> на значение с плавающей запятой, возвращая результат в новый экземпляр <code>XMVECTOR</code> .<br/> <code>operator *</code>Компонент умножает все компоненты экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на значение с плавающей запятой, возвращая новый <code>XMVECTOR</code> экземпляр, компоненты которого содержат результат. <br/>
<blockquote>
[!Note]<br />
Этот оператор доступен только в C++.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>КСМВЕКТОР:: operator * (КСМВЕКТОР, КСМВЕКТОР)</strong></a></td>
<td style="text-align: left;">Умножает один экземпляр <code>XMVECTOR</code> на второй экземпляр, возвращая результат в третьем экземпляре. <br/> <code>operator *</code>Компонент умножает все компоненты экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на соответствующий компонент во втором экземпляре <code>XMVECTOR</code> , возвращая новый <code>XMVECTOR</code> экземпляр, содержащий результат. <br/>
<blockquote>
[!Note]<br />
Этот оператор доступен только в C++.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Операторы КСМВЕКТОР](ovw-xmvector-operators.md)
</dt> <dt>

**Ссылки**
</dt> <dt>

[**Тип данных КСМВЕКТОР**](xmvector-data-type.md)
</dt> </dl>

 

 
