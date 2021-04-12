---
title: Метод Игасернотифи Ондатамове (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи Ондатамове (не рекомендуется)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Ондатамове (устаревший) метод устаревших функций среды Windows
- Ондатамове (устаревший) метод устаревших функций среды Windows, интерфейс Игасернотифи
- Устаревшие функции среды Windows интерфейса Игасернотифи, Ондатамове (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353005"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Метод Игасернотифи:: Ондатамове (не рекомендуется)

\[**Ондатамове** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]

Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

Этот метод уведомляет индексатор о перемещенных данных. При отправке уведомления индексатору он включает старый адрес, новый адрес и логический адрес.

## <a name="syntax"></a>Синтаксис


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ечанжеадвисесемантикс* \[ окне\]
</dt> <dd>

Тип: **Long**

Перечислимый параметр, описывающий тип произошедшего перемещения.

</dd> <dt>

*бстролдаддресс* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Старый адрес элемента, который был перемещен. Для обычных файлов *ечанжеадвисесематикс* имеет **значение NULL**. Для папки или каталога задайте для *ечанжеадвисесематикс* \_ \_ Каталог семантики ЦС ГСР \_ .

</dd> <dt>

*бстрневаддресс* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Новый адрес элемента, который был перемещен.

</dd> <dt>

*бстрлогикаладдресс* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Логический адрес перемещенного элемента.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

 

 
