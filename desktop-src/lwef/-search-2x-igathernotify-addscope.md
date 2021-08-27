---
title: Метод Игасернотифи AddScope (не рекомендуется)
description: этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи AddScope (не рекомендуется)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- AddScope (устаревший) метод устаревшие функции среды Windows
- AddScope (устаревший) метод устаревшие функции среды Windows, интерфейс игасернотифи
- устаревшие функции Windows интерфейса игасернотифи, AddScope (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a49c0cf652b0cfde59167fa98498a978d3c2c41d3a886ee092b8f4a28d35f61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755595"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Метод Игасернотифи:: AddScope (не рекомендуется)

\[**AddScope** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]

этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

Добавляет начальную страницу или URL-адрес, который вы отслеживаете. Это инициирует добавочное сканирование при подключении, а затем предполагает, что все дальнейшие изменения URL-адреса обрабатываются уведомлением.

## <a name="syntax"></a>Синтаксис


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрскопе* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Строка, указывающая начальную страницу или Урлсат, которые вы отслеживаете.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Вызов этого метода запускает добавочное сканирование при подключении к хранилищу. После этого предполагается, что все изменения URL-адресов задаются уведомлением после первоначального обновления.

 

 
