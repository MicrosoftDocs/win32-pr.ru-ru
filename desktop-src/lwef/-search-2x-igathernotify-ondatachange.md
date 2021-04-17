---
title: Метод Игасернотифи Ондатачанже (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи Ондатачанже (не рекомендуется)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Ондатачанже (устаревший) метод устаревших функций среды Windows
- Ондатачанже (устаревший) метод устаревших функций среды Windows, интерфейс Игасернотифи
- Устаревшие функции среды Windows интерфейса Игасернотифи, Ондатачанже (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694020"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Метод Игасернотифи:: Ондатачанже (не рекомендуется)

\[**Ондатачанже** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]

Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

Этот метод уведомляет индексатор измененных данных. При отправке уведомления индексатору он включает тип изменения, физический адрес и логический адрес.

## <a name="syntax"></a>Синтаксис


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ечанжеадвисе* \[ окне\]
</dt> <dd>

Тип: **Long**

Перечислимое значение, указывающее тип изменения.

</dd> <dt>

*бстрфисикаладдресс* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Физический адрес изменяемого элемента.

</dd> <dt>

*бстрлогикаладдресс* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Логический адрес элемента, который изменился.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

 

 
