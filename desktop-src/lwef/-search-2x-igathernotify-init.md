---
title: Метод init Игасернотифи (не рекомендуется)
description: Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search Исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод init Игасернотифи (не рекомендуется)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Метод init (не рекомендуется). устаревшие функции среды Windows
- Метод init (не рекомендуется). устаревшие функции среды Windows, интерфейс Игасернотифи
- Интерфейс Игасернотифи устаревшие функции среды Windows, метод init (устарел)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694021"
---
# <a name="igathernotifyinit-deprecated-method"></a>Метод Игасернотифи:: init (устарел)

\[**Инициализация** может быть изменена или недоступна в последующих версиях операционной системы или продукта.\]

Этот раздел интерфейса поиска на рабочем столе Windows устарел и заменен API-интерфейсом Windows Search [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

Инициализирует интерфейс средства сбора данных. Также указывает индекс для уведомления и хранилище приложений для отслеживания.

## <a name="syntax"></a>Синтаксис


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраппликатион* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Строка, указывающая целевое приложение.

</dd> <dt>

*бстрпрожект* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Строка, указывающая имя индексатора, в который передаются сведения о сборщике.

</dd> <dt>

*варскопесбстраррай* \[ окне\]
</dt> <dd>

Тип: **Variant**

Необязательный параметр, который позволяет передать массив областей для инициализации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Инициализация с помощью приложения = "Рсапп", Project = "Миндекс".

 

 
