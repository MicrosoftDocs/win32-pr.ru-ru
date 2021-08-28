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
ms.openlocfilehash: 99f584bac1e31773a5264d4bf3a37931ba9ae793
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482020"
---
# <a name="operator--operators"></a>\*Операторы операторов

Операторы умножения

### <a name="overload-list"></a>Список перегрузок




| Оператор | Описание | 
|----------|-------------|
| <a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>КСМВЕКТОР:: operator * (float, КСМВЕКТОР)</strong></a> | Умножьте значение с плавающей запятой на экземпляр <code>XMVECTOR</code> , возвращая результат в новый экземпляр <code>XMVECTOR</code> .<br /> Объект <code>operator *</code> умножает значение с плавающей запятой на каждый компонент экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a>, возвращая новый <code>XMVECTOR</code> экземпляр, компоненты которого содержат результат. <br /><blockquote>[!Note]<br />Этот оператор доступен только в C++.</blockquote><br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>КСМВЕКТОР:: operator * (КСМВЕКТОР, float)</strong></a> | Умножьте экземпляр <code>XMVECTOR</code> на значение с плавающей запятой, возвращая результат в новый экземпляр <code>XMVECTOR</code> .<br /> <code>operator *</code>Компонент умножает все компоненты экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на значение с плавающей запятой, возвращая новый <code>XMVECTOR</code> экземпляр, компоненты которого содержат результат. <br /><blockquote>[!Note]<br />Этот оператор доступен только в C++.</blockquote><br /> | 
| <a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>КСМВЕКТОР:: operator * (КСМВЕКТОР, КСМВЕКТОР)</strong></a> | Умножает один экземпляр <code>XMVECTOR</code> на второй экземпляр, возвращая результат в третьем экземпляре. <br /> <code>operator *</code>Компонент умножает все компоненты экземпляра <a href="xmvector-data-type.md"><strong>типа данных ксмвектор</strong></a> на соответствующий компонент во втором экземпляре <code>XMVECTOR</code> , возвращая новый <code>XMVECTOR</code> экземпляр, содержащий результат. <br /><blockquote>[!Note]<br />Этот оператор доступен только в C++.</blockquote><br /> | 




## <a name="see-also"></a>См. также

<dl> <dt>

[Операторы КСМВЕКТОР](ovw-xmvector-operators.md)
</dt> <dt>

**Ссылки**
</dt> <dt>

[**Тип данных КСМВЕКТОР**](xmvector-data-type.md)
</dt> </dl>

 

 
