---
title: Метод Игасернотифи Ондатачанже (не рекомендуется)
description: этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи Ондатачанже (не рекомендуется)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- ондатачанже (устаревший) метод устаревшие функции среды Windows
- ондатачанже (устаревший) метод устаревшие функции среды Windows, интерфейс игасернотифи
- устаревшие функции Windows интерфейса игасернотифи, ондатачанже (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95533a7937136a0f828a292efe7e398258e3c880974e031d9d7d2797f721f2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481598"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Метод Игасернотифи:: Ондатачанже (не рекомендуется)

\[**Ондатачанже** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]

этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

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

 

 
