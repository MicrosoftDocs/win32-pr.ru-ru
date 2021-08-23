---
title: Метод Игасернотифи Ондатамове (не рекомендуется)
description: этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи Ондатамове (не рекомендуется)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- ондатамове (устаревший) метод устаревшие функции среды Windows
- ондатамове (устаревший) метод устаревшие функции среды Windows, интерфейс игасернотифи
- устаревшие функции Windows интерфейса игасернотифи, ондатамове (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3d4f7d91bc9e9741f227812997a820ab4180ccf438d52ae8cfea93f67dc0bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665874"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Метод Игасернотифи:: Ондатамове (не рекомендуется)

\[**Ондатамове** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]

этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

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

 

 
