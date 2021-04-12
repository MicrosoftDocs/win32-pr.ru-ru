---
title: Метод Игасернотифи AddScope (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод Игасернотифи AddScope (не рекомендуется)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- AddScope (устаревший) метод устаревших функций среды Windows
- AddScope (устаревший) метод устаревших функций среды Windows, интерфейс Игасернотифи
- Устаревшие функции среды Windows интерфейса Игасернотифи, AddScope (устаревший метод)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353012"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Метод Игасернотифи:: AddScope (не рекомендуется)

\[**AddScope** может быть изменен или недоступен в последующих версиях операционной системы или продукта.\]

Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

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

## <a name="remarks"></a>Комментарии

Вызов этого метода запускает добавочное сканирование при подключении к хранилищу. После этого предполагается, что все изменения URL-адресов задаются уведомлением после первоначального обновления.

 

 
