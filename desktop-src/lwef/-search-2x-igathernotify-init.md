---
title: Метод init Игасернотифи (не рекомендуется)
description: этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска исеарчперсистентитемсчанжедсинк в Windows SDK. | Метод init Игасернотифи (не рекомендуется)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- метод Init (не рекомендуется). устаревшие функции Windows среды
- метод Init (не рекомендуется). устаревшие функции Windows среды, интерфейс игасернотифи
- интерфейс игасернотифи устаревшие функции среды Windows, метод Init (не рекомендуется)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db5666197524afb454927036cdd68375dfb2937197ed211646b63d80a09e5b12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359306"
---
# <a name="igathernotifyinit-deprecated-method"></a>Метод Игасернотифи:: init (устарел)

\[**Инициализация** может быть изменена или недоступна в последующих версиях операционной системы или продукта.\]

этот Windowsный раздел интерфейса поиска на рабочем столе устарел и заменен Windows API поиска [**исеарчперсистентитемсчанжедсинк**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) в Windows SDK.

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

## <a name="remarks"></a>Remarks

инициализация с помощью приложения = "рсапп", Project = "миндекс".

 

 
